<template>
	<div class="product d-flex flex-column overflow-hidden">
		<figure class="mb-0 product-media bg-white d-flex justify-content-center align-items-center">
			<span
				class="product-label label-new"
				v-if="product.new"
			>New</span>
			<span
				class="product-label label-sale"
				v-if="product.sale_price"
			>Sale</span>
			<span
				class="product-label label-top"
				v-if="product.top"
			>Top</span>
			<span
				class="product-label label-out"
				v-if="product.stock === 0"
			>Out Of Stock</span>

			<nuxt-link
				:to="'/product/default/'+ product.slug"
				class="w-100"
			>
				<img
					v-lazy="`${baseUrl}${product.pictures[0].url}`"
					alt="Product"
					:width="product.pictures[0].width"
					:height="product.pictures[0].height"
					class="product-image bg-white"
				/>
				<img
					v-lazy="`${baseUrl}${product.pictures[1].url}`"
					alt="Product"
					:width="product.pictures[1].width"
					:height="product.pictures[1].height"
					class="product-image-hover bg-white"
					v-if="product.pictures[1]"
				/>
			</nuxt-link>
			<count-down
				v-if="product.until"
				wrap="product-countdown bg-light"
				:until="product.until"
				format="DHMS"
				:relative="true"
				:labelsShort="true"
			></count-down>
			<div
				class="product-action-vertical"
				v-if="product.stock !== 0"
			>
				<nuxt-link
					to="/shop/wishlist"
					class="btn-product-icon text-dark btn-wishlist added-to-wishlist"
					v-if="isInWishlist(product)"
					key="inWishlist"
				>
					<span>go to wishlist</span>
				</nuxt-link>
				<a
					href="javascript:;"
					class="btn-product-icon text-dark btn-wishlist"
					@click.prevent="addToWishlist({product: product})"
					v-else
					key="notInWishlist"
				>
					<span>add to wishlist</span>
				</a>
				<a
					href="#"
					class="btn-product-icon text-dark btn-quickview"
					title="Quick view"
					@click.prevent="quickView({product: product})"
				>
					<span>Quick view</span>
				</a>
				<a
					href="#"
					class="btn-product-icon text-dark btn-compare"
					title="Compare"
					key="inCompare"
					v-if="isInCompare(product)"
				>
					<span>Compare</span>
				</a>
				<button
					class="btn-product-icon text-dark btn-compare"
					title="Compare"
					@click.prevent="addToCompare({product: product})"
					v-else
					key="notInCompare"
				>
					<span>compare</span>
				</button>
			</div>
		</figure>

		<div class="product-body pb-3">
			<div class="text-left product-cat font-weight-normal text-light mb-0">
				<span
					v-for="(cat, index) of product.category"
					:key="index"
				>
					<nuxt-link :to="{path: '/shop/sidebar/list', query: {category: cat.slug}}">{{ cat.name }}</nuxt-link>
					{{ index < product.category.length - 1 ? ',' : '' }}
				</span>
			</div>
			<h3 class="product-title letter-spacing-normal font-size-normal text-left mb-0">
				<nuxt-link :to="'/product/default/'+ product.slug">{{ product.name }}</nuxt-link>
			</h3>

			<div
				class="product-price mb-1"
				v-if="product.stock==0"
				key="outPrice"
			>
				<span class="out-price">${{ product.price.toFixed(2) }}</span>
			</div>

			<template v-else>
				<div
					class="product-price mb-1"
					v-if="minPrice == maxPrice"
				>${{ minPrice.toFixed(2) }}</div>
				<template v-else>
					<div
						class="product-price mb-1"
						v-if="product.variants.length == 0"
					>
						<span class="new-price">${{ minPrice.toFixed(2) }}</span>
						<span class="old-price font-size-normal font-weight-normal">${{ maxPrice.toFixed(2) }}</span>
					</div>
					<div
						class="product-price"
						v-else
					>${{minPrice.toFixed(2)}}&ndash;${{maxPrice.toFixed(2)}}</div>
				</template>
			</template>

			<div class="ratings-container">
				<div class="ratings">
					<div
						class="ratings-val"
						:style="{width: product.ratings * 20 + '%'}"
					></div>
					<span class="tooltip-text">{{ product.ratings.toFixed(2) }}</span>
				</div>
				<span class="ratings-text ml-2">( {{ product.review }} Reviews )</span>
			</div>
		</div>

		<div
			class="product-action position-relative visible"
			v-if="product.stock !== 0"
		>
			<nuxt-link
				:to="'/product/default/' + product.slug"
				class="btn-product btn-cart text-uppercase text-dark text-decoration-none"
				v-if="product.variants.length > 0"
			>
				<span>select options</span>
			</nuxt-link>
			<button
				class="btn-product btn-cart text-uppercase text-dark text-decoration-none"
				@click.prevent="addToCart( {product: product} )"
				v-else
			>
				<span class="text-dark shadow-none">add to cart</span>
			</button>
		</div>
		<div
			class="product-sold"
			v-if="isShownSold"
		>
			<div class="sold position-relative w-100">
				<div
					class="sold-val position-absolute"
					:style="{width: soldRate  + '%'}"
				></div>
				<span class="sold-text font-size-normal second-primary-color">Sold: {{product.sold}}</span>
			</div>
		</div>
	</div>
</template>
<script>
import CountDown from '~/components/elements/CountDown';

import { mapGetters, mapActions } from 'vuex';
import { baseUrl } from '~/repositories/repository';
export default {
	components: {
		CountDown
	},
	props: {
		product: Object,
		isShownSold: {
			type: Boolean,
			default: function() {
				return true;
			}
		}
	},
	data: function() {
		return {
			baseUrl: baseUrl,
			maxPrice: 0,
			minPrice: 99999
		};
	},
	computed: {
		...mapGetters('cart', ['canAddToCart']),
		...mapGetters('wishlist', ['isInWishlist']),
		...mapGetters('compare', ['isInCompare'])
	},

	created: function() {
		let min = this.minPrice;
		let max = this.maxPrice;
		this.product.variants.map(item => {
			if (min > item.price) min = item.price;
			if (max < item.price) max = item.price;
		}, []);

		if (this.product.variants.length == 0) {
			min = this.product.sale_price
				? this.product.sale_price
				: this.product.price;
			max = this.product.price;
		}

		this.minPrice = min;
		this.maxPrice = max;

		this.soldRate =
			(this.product.sold / (this.product.sold + this.product.stock)) *
			100;
	},
	methods: {
		...mapActions('cart', ['addToCart']),
		...mapActions('wishlist', ['addToWishlist']),
		...mapActions('compare', ['addToCompare']),
		quickView: function() {
			this.$modal.show(
				() => import('~/components/elements/modals/QuickViewModal'),
				{
					product: this.product
				},
				{ width: '1030', height: 'auto', adaptive: true }
			);
		}
	}
};
</script>