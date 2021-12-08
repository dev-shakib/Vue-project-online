<template>
	<div class="blog-section bg-white py-2 pb-4">
		<div class="container">
			<div class="heading heading-flex">
				<div class="heading-left">
					<h2 class="title mb-0 font-weight-bold">From Our Blog</h2>

				</div>

				<div class="heading-right">
					<nuxt-link
						to="/blog/classic"
						class="title-link font-size-normal text-uppercase font-weight-normal"
					>View More Posts
						<i class="icon-long-arrow-right"></i>
					</nuxt-link>
				</div>

			</div>
			<div class="swiper-carousel">
				<div
					class="mb-0"
					v-swiper:swiper15="carouselSetting"
				>
					<div class="swiper-wrapper">
						<div
							class="swiper-slide"
							v-for="(blog, index) in blogs"
							:key="index"
						>
							<blog-four
								:blog="blog"
								class="mb-2"
							></blog-four>
						</div>
					</div>
				</div>
				<div class="swiper-dots d-block d-sm-none"></div>
			</div>
		</div>
		<div class="mb-lg-5"></div>
	</div>
</template>
<script>
import BlogFour from '~/components/elements/blogs/BlogFour';
import { carouselSettingDefault } from '~/utilities/carousel';

export default {
	components: {
		BlogFour
	},
	props: {
		blogs: Array
	},
	data: function() {
		return {
			carouselSetting: {
				...carouselSettingDefault,
				slidesPerView: 4,
				breakpoints: {
					480: {
						slidesPerView: 1
					},
					768: {
						slidesPerView: 2
					},
					992: {
						slidesPerView: 3
					}
				},
				pagination: {
					el: '.blog-section .swiper-dots',
					clickable: true
				}
			}
		};
	}
};
</script>