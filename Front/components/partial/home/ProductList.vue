<template>
	<div class="product d-flex flex-row overflow-hidden mb-0 p-0 shadow-none">
		<figure class="mb-0 product-media bg-white d-flex justify-content-center align-items-center">
			<nuxt-link :to="'/product/default/'+ product.slug">
				<img
					v-lazy="`${baseUrl}${product.sm_pictures[0].url}`"
					alt="Product"
					:width="product.sm_pictures[0].width"
					:height="product.sm_pictures[0].height"
					class="product-image bg-white"
				/>
				<img
					v-lazy="`${baseUrl}${product.sm_pictures[1].url}`"
					alt="Product"
					:width="product.sm_pictures[1].width"
					:height="product.sm_pictures[1].height"
					class="product-image-hover bg-white"
					v-if="product.sm_pictures[1]"
				/>
			</nuxt-link>
		</figure>

		<div class="product-body">
			<div class="product-cat text-left">
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
				class="product-price mb-1 text-dark"
				v-if="product.stock==0"
				key="outPrice"
			>
				<span class="out-price">${{ product.price.toFixed(2) }}</span>
			</div>

			<template v-else>
				<div
					class="product-price"
					v-if="minPrice == maxPrice"
				>${{ minPrice.toFixed(2) }}</div>
				<template v-else>
					<div
						class="product-price"
						v-if="product.variants.length == 0"
					>
						<span class="new-price">${{ minPrice.toFixed(2) }}</span>
						<span class="old-price">${{ maxPrice.toFixed(2) }}</span>
					</div>
					<div
						class="product-price"
						v-else
					>${{minPrice.toFixed(2)}}&ndash;${{maxPrice.toFixed(2)}}</div>
				</template>
			</template>

			<div class="ratings-container mb-0">
				<div class="ratings font-size-normal">
					<div
						class="ratings-val font-size-normal"
						:style="{width: product.ratings * 20 + '%'}"
					></div>
					<span class="tooltip-text">{{ product.ratings.toFixed(2) }}</span>
				</div>
				<span class="ratings-text ml-2">( {{ product.review }} Reviews )</span>
			</div>
		</div>
	</div>
</template>
<script>
import { baseUrl } from '~/repositories/repository';
export default {
	props: {
		product: Object
	},
	data: function() {
		return {
			baseUrl: baseUrl,
			maxPrice: 0,
			minPrice: 99999
		};
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
	}
};
</script>