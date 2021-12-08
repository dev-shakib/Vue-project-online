<template>
	<div class="container mb-4 electronics">
		<div class="bg-lighter trending-products">
			<div class="heading heading-flex">
				<div class="heading-left">
					<h2 class="title font-weight-bold mb-1">Electronics</h2>
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
					id="tab1-cell-phone"
				>
					<div class="swiper-carousel electronic-carousel swiper-4">
						<div v-swiper:swiper4="carouselSetting4">
							<div class="swiper-wrapper">
								<div
									class="swiper-slide"
									v-for="(product,index) in cellPhones"
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
					id="tab1-computers"
				>
					<div class="swiper-carousel electronic-carousel swiper-5">
						<div v-swiper:swiper5="carouselSetting4">
							<div class="swiper-wrapper">
								<div
									class="swiper-slide"
									v-for="(product,index) in computers"
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
					id="tab1-tv"
				>
					<div class="swiper-carousel electronic-carousel swiper-6">
						<div v-swiper:swiper6="carouselSetting4">
							<div class="swiper-wrapper">
								<div
									class="swiper-slide"
									v-for="(product,index) in tvs"
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
					id="tab1-smart-phones"
				>
					<div class="swiper-carousel electronic-carousel swiper-7">
						<div v-swiper:swiper7="carouselSetting4">
							<div class="swiper-wrapper">
								<div
									class="swiper-slide"
									v-for="(product,index) in smartPhones"
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
					id="tab1-audios"
				>
					<div class="swiper-carousel electronic-carousel swiper-8">
						<div v-swiper:swiper8="carouselSetting4">
							<div class="swiper-wrapper">
								<div
									class="swiper-slide"
									v-for="(product,index) in audios"
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
					v-lazy:background-image="'./images/home/banners/banner-bg-1.jpg'"
				>
					<span class="product-label label-sale text-uppercase">Best Deal</span>
					<div class="banner-content position-relative d-flex flex-column">
						<h3 class="banner-title font-weight-bold mb-2 text-left">Apple Watch
							<br>Starting at $199</h3>
						<nuxt-link
							to="/shop/sidebar/list"
							class="btn-product text-uppercase text-dark text-decoration-none btn-rounded"
							title="Discover now"
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
		electronics: Array
	},
	data: function() {
		return {
			tabsData: [
				{
					id: 'cell-phone',
					title: 'CELL PHONES',
					active: true
				},
				{
					id: 'computers',
					title: 'COMPUTERS'
				},
				{
					id: 'tv',
					title: 'TV & VIDEO'
				},
				{
					id: 'smart-phones',
					title: 'SMART PHONES'
				},
				{
					id: 'audios',
					title: 'AUDIO'
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
		cellPhones: function() {
			return catFilter(this.electronics, ['cell-phone']);
		},
		computers: function() {
			return catFilter(this.electronics, ['computers']);
		},
		tvs: function() {
			return catFilter(this.electronics, ['tv']);
		},
		smartPhones: function() {
			return catFilter(this.electronics, ['smart-phones']);
		},
		audios: function() {
			return catFilter(this.electronics, ['audio']);
		}
	}
};
</script>
