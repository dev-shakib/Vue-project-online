<template>
	<div :class="addClass">
		<div class="heading heading-flex align-items-center">
			<div class="heading-left">
				<h2 class="title mb-0 font-weight-bold">{{title}}</h2>

			</div>

			<div class="heading-right mt-0">
				<nuxt-link
					to="/shop/sidebar/3cols"
					class="title-link font-size-normal text-uppercase font-weight-normal shadow-none"
				>View
					More
					<i class="icon-long-arrow-right"></i>
				</nuxt-link>
			</div>

		</div>
		<div class="products d-flex flex-column justify-content-between bg-white mt-2 mt-xl-0">
			<product-list
				v-for="(product, index) in products"
				:key="index"
				:product="product"
			></product-list>
		</div>
	</div>
</template>
<script>
import ProductList from '~/components/partial/home/ProductList';

export default {
	components: {
		ProductList
	},
	data: function() {
		return {};
	},
	props: {
		products: Array,
		addClass: '',
		title: ''
	}
};
</script>