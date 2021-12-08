<template>
	<div class="container mb-4 electronics fashion">
		<div class="bg-lighter trending-products">
			<div class="heading heading-flex">
				<div class="heading-left">
					<h2 class="title font-weight-bold mb-1">Fashion & Clothing</h2>
				</div>

				<div class="heading-right">
					<tabs
						class="nav nav-pills justify-content-center mr-n3"
						:data="tabsData"
						id="tab1"
					></tabs>
				</div>
			</div>
			<div class="tab-content tab-content-carousel position-relative">
				<div
					class="tab-pane fade show active"
					id="tab1-best-seller"
				>
					<div class="swiper-carousel electronic-carousel swiper-9">
						<div v-swiper:swiper9="carouselSetting4">
							<div class="swiper-wrapper">
								<div
									class="swiper-slide"
									v-for="(product,index) in products"
									:key="index"
								>
									<product-twelve
										:product="product"
										:isShownSold="false"
									></product-twelve>
								</div>
							</div>
						</div>
					</div>
				</div>
				<div
					class="tab-pane fade p-0"
					id="tab1-women"
				>
					<div class="swiper-carousel electronic-carousel swiper-10">
						<div v-swiper:swiper10="carouselSetting4">
							<div class="swiper-wrapper">
								<div
									class="swiper-slide"
									v-for="(product,index) in women"
									:key="index"
								>
									<product-twelve
										:product="product"
										:isShownSold="false"
									></product-twelve>
								</div>
							</div>
						</div>
					</div>
				</div>
				<div
					class="tab-pane p-0 fade"
					id="tab1-men"
				>
					<div class="swiper-carousel electronic-carousel swiper-11">
						<div v-swiper:swiper11="carouselSetting4">
							<div class="swiper-wrapper">
								<div
									class="swiper-slide"
									v-for="(product,index) in men"
									:key="index"
								>
									<product-twelve
										:product="product"
										:isShownSold="false"
									></product-twelve>
								</div>
							</div>
						</div>
					</div>
				</div>
				<div
					class="tab-pane p-0 fade"
					id="tab1-shoes"
				>
					<div class="swiper-carousel electronic-carousel swiper-12">
						<div v-swiper:swiper12="carouselSetting4">
							<div class="swiper-wrapper">
								<div
									class="swiper-slide"
									v-for="(product,index) in shoes"
									:key="index"
								>
									<product-twelve
										:product="product"
										:isShownSold="false"
									></product-twelve>
								</div>
							</div>
						</div>
					</div>
				</div>
				<div
					class="tab-pane p-0 fade"
					id="tab1-accessories"
				>
					<div class="swiper-carousel electronic-carousel swiper-13">
						<div v-swiper:swiper13="carouselSetting4">
							<div class="swiper-wrapper">
								<div
									class="swiper-slide"
									v-for="(product,index) in accessories"
									:key="index"
								>
									<product-twelve
										:product="product"
										:isShownSold="false"
									></product-twelve>
								</div>
							</div>
						</div>
					</div>
				</div>
				<div
					class="banner banner-overlay mb-0 bg-image position-md-relative position-absolute"
					v-lazy:background-image="'./images/home/banners/banner-bg-2.jpg'"
				>
					<span class="product-label label-sale">CLEARANCE</span>
					<div class="banner-content position-relative d-flex flex-column">
						<h3 class="banner-title text-white font-weight-bold mb-2 text-left">Women's
							<br>Sportswear &amp; Joggers</h3>
						<nuxt-link
							to="/shop/market"
							class="btn-product text-decoration-none text-uppercase text-dark btn-rounded"
							title=""
						>
							<span class="text-dark shadow-none">Discover Now&nbsp;&nbsp;
								<i class="icon-long-arrow-right d-inline-block"></i>
							</span>
						</nuxt-link>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
import Tabs from '~/components/elements/Tabs';
import ProductTwelve from '~/components/elements/products/ProductTwelve';

import { catFilter } from '~/utilities/common';
import { carouselSetting1 } from '~/utilities/carousel';

export default {
	components: {
		Tabs,
		ProductTwelve
	},
	props: {
		products: Array
	},
	data: function() {
		return {
			tabsData: [
				{
					id: 'best-seller',
					title: 'BEST SELLER',
					active: true
				},
				{
					id: 'women',
					title: 'WOMAN'
				},
				{
					id: 'men',
					title: 'MAN'
				},
				{
					id: 'shoes',
					title: 'SHOES'
				},
				{
					id: 'accessories',
					title: 'ACCESSORIES'
				}
			],
			carouselSetting4: {
				...carouselSetting1,
				slidesPerView: 6,
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
	computed: {
		women: function() {
			return catFilter(this.products, ['women']);
		},
		men: function() {
			return catFilter(this.products, ['men']);
		},
		shoes: function() {
			return catFilter(this.products, ['shoes']);
		},
		accessories: function() {
			return catFilter(this.products, ['accessories']);
		}
	}
};
</script>
