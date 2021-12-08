<template>
	<footer
		class="footer footer-2 font-weight-normal second-primary-color"
		style="background-color: #222"
	>
		<div class="cta cta-horizontal cta-horizontal-box pt-5 pb-5">
			<div class="container">
				<div class="row align-items-center justify-content-center">
					<div class="col-xl-4-5col offset-xl-10col">
						<div class="row align-items-center">
							<div class="col-lg-5 cta-txt text-lg-left text-center">
								<h3 class="cta-title text-white my-2 mt-0">Join Our Newsletter</h3>

								<p class="cta-desc font-size-normal second-primary-color font-weight-normal">Subcribe to get information about products and coupons</p>

							</div>

							<div class="col-lg-7">
								<form
									action="#"
									class="d-flex justify-content-end justify-content-center"
								>
									<div class="input-group">
										<input
											type="email"
											class="form-control mr-0 font-weight-normal"
											placeholder="Enter your Email Address"
											aria-label="Email Adress"
											required
										>
										<div class="input-group-append">
											<button
												class="btn text-uppercase"
												type="submit"
											>Subscribe
												<i class="icon-long-arrow-right mr-0"></i>
											</button>
										</div>

									</div>

								</form>
							</div>

						</div>

					</div>

				</div>

			</div>

		</div>

		<div class="container">
			<hr
				class="mt-0 mb-0"
				style="border-color: #444;"
			>
		</div>
		<div class="footer-middle border-0">
			<div class="container">
				<div class="row">
					<div class="col-12 col-lg-2-5cols">
						<div class="widget widget-about mb-4">
							<img
								v-lazy="'./images/home/logo-footer.png'"
								class="footer-logo bg-transparent"
								alt="Footer Logo"
								width="105"
								height="25"
							>
							<p class="font-weight-normal second-primary-color">Praesent dapibus, neque id cursus ucibus, tortor neque egestas augue, eu vulputate magna
								eros eu erat. Aliquam erat volutpat. Nam dui mi, tincidunt quis, accumsan porttitor,
								facilisis luctus, metus. </p>

							<div class="widget-about-info">
								<div class="row">
									<div class="col-sm-6 col-md-4">
										<span class="widget-about-title text-white">Got Question? Call us 24/7</span>
										<a
											href="tel:123456789"
											class="text-primary"
										>+0123 456 789</a>
									</div>

									<div class="col-sm-6 col-md-8">
										<span class="pl-3 widget-about-title text-white">Payment Method</span>
										<figure class="pl-3 mb-0 footer-payments">
											<img
												v-lazy="'./images/payments.png'"
												class="bg-transparent"
												alt="Payment methods"
												width="272"
												height="20"
											>
										</figure>

									</div>

								</div>

							</div>

						</div>

					</div>

					<div class="col-sm-4 col-lg-5cols">
						<div class="widget mb-4">
							<h4 class="widget-title text-white">Information</h4>

							<ul class="widget-list">
								<li>
									<nuxt-link to="/pages/about">About Molla</nuxt-link>
								</li>
								<li>
									<a href="#">How to shop on Molla</a>
								</li>
								<li>
									<a href="#">FAQ</a>
								</li>
								<li>
									<nuxt-link to="/pages/contact">Contact us</nuxt-link>
								</li>
								<li>
									<nuxt-link to="/pages/login">Log in</nuxt-link>
								</li>
							</ul>

						</div>

					</div>

					<div class="col-sm-4 col-lg-5cols">
						<div class="widget mb-4">
							<h4 class="widget-title text-white">Customer Service</h4>

							<ul class="widget-list">
								<li>
									<a href="#">Payment Methods</a>
								</li>
								<li>
									<a href="#">Money-back guarantee!</a>
								</li>
								<li>
									<a href="#">Returns</a>
								</li>
								<li>
									<a href="#">Shipping</a>
								</li>
								<li>
									<a href="#">Terms and conditions</a>
								</li>
								<li>
									<a href="#">Privacy Policy</a>
								</li>
							</ul>

						</div>

					</div>

					<div class="col-sm-4 col-lg-5cols">
						<div class="widget mb-4">
							<h4 class="widget-title text-white">My Account</h4>

							<ul class="widget-list">
								<li>
									<a href="#">Sign In</a>
								</li>
								<li>
									<nuxt-link to="/shop/cart">View Cart</nuxt-link>
								</li>
								<li>
									<nuxt-link to="/shop/wishlist">My Wishlist</nuxt-link>
								</li>
								<li>
									<nuxt-link to="/shop/dashboard">Track My Order</nuxt-link>
								</li>
								<li>
									<a href="#">Help</a>
								</li>
							</ul>

						</div>

					</div>

				</div>

			</div>

		</div>

		<div class="footer-bottom font-weight-normal">
			<div class="container">
				<p class="footer-copyright font-weight-normal ml-lg-2 second-primary-color">Copyright © {{ new Date().getFullYear() }} Molla Store. All Rights Reserved. </p>

				<ul class="footer-menu justify-content-center">
					<li>
						<a href="#">Terms Of Use</a>
					</li>
					<li>
						<a href="#">Privacy Policy</a>
					</li>
				</ul>

				<div class="social-icons social-icons-color justify-content-center">
					<span class="social-label">Social Media</span>
					<a
						href="#"
						class="social-icon social-facebook"
						title="Facebook"
						target="_blank"
					>
						<i class="icon-facebook-f"></i>
					</a>
					<a
						href="#"
						class="social-icon social-twitter"
						title="Twitter"
						target="_blank"
					>
						<i class="icon-twitter"></i>
					</a>
					<a
						href="#"
						class="social-icon social-instagram"
						title="Instagram"
						target="_blank"
					>
						<i class="icon-instagram"></i>
					</a>
					<a
						href="#"
						class="social-icon social-youtube"
						title="Youtube"
						target="_blank"
					>
						<i class="icon-youtube"></i>
					</a>
					<a
						href="#"
						class="social-icon social-pinterest"
						title="Pinterest"
						target="_blank"
					>
						<i class="icon-pinterest"></i>
					</a>
				</div>

			</div>

		</div>

		<div class="mb-10" v-if="bottomSticky"></div>
	</footer>
</template>

<script>
export default {
    data: function () {
        return {
            bottomSticky: false
        }
    },
    computed: {
        isFullwidth: function() {
            return this.$route.path.includes('fullwidth');
        }
    },
    watch: {
        $route: function () {
            this.handleBottomSticky();
        }
    },
    mounted: function() {
        this.handleBottomSticky();
        window.addEventListener('resize', this.handleBottomSticky, {passive: true});
    },
    destroyed: function () {
        window.removeEventListener('resize', this.handleBottomSticky);
    },
    methods: {
        handleBottomSticky: function () {
            this.bottomSticky = this.$route.path.includes('/product/default') && (window.innerWidth > 991);
        }
    }
};
</script>