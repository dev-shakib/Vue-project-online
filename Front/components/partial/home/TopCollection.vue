<template>
	<div class="container deal-section">
		<h3 class="title text-center mt-5 font-weight-bold">Today's Best Deal</h3>

		<div class="swiper-carousel deal-carousel swiper-3">
			<div v-swiper:swiper3="carouselSetting3">
				<div class="swiper-wrapper">
					<div
						class="swiper-slide"
						v-for="(product,index) in topProducts"
						:key="index"
					>
						<product-twelve :product="product"></product-twelve>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
import ProductTwelve from '~/components/elements/products/ProductTwelve';
import { carouselSettingDefault } from '~/utilities/carousel';

export default {
	components: {
		ProductTwelve
	},
	data: function() {
		return {
			carouselSetting3: {
				...carouselSettingDefault,
				slidesPerView: 5,
				spaceBetween: 0,
				breakpoints: {
					1200: {
						slidesPerView: 5
					},
					992: {
						slidesPerView: 4
					},
					768: {
						slidesPerView: 3
					},
					576: {
						slidesPerView: 2
					}
				}
			}
		};
	},
	props: {
		topProducts: Array
	}
};
</script>