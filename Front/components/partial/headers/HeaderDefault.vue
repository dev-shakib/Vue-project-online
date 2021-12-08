<template>
	<header class="header header-intro-clearance header-26">
		<div class="header-top">
			<div :class="isFullwidth ? 'container-fluid' : 'container'">
				<div class="header-left">
					<div class="welcome-msg d-flex">
						<a
							href="tel:#"
							class="font-weight-normal"
						>
							<i class="icon-phone h6 second-primary-color"></i>Call: +0123 456 789</a>
					</div>
				</div>

				<div class="header-right font-weight-normal">
					<ul class="top-menu">
						<li>
							<a href="#">Links</a>
							<ul>
								<li>
									<div class="header-dropdown">
										<a href="#">USD</a>
										<div class="header-menu">
											<ul>
												<li>
													<a href="#">Eur</a>
												</li>
												<li>
													<a href="#">Usd</a>
												</li>
											</ul>
										</div>

									</div>
								</li>
								<li>
									<div class="header-dropdown">
										<a href="#">English</a>
										<div class="header-menu">
											<ul>
												<li>
													<a href="#">English</a>
												</li>
												<li>
													<a href="#">French</a>
												</li>
												<li>
													<a href="#">Spanish</a>
												</li>
											</ul>
										</div>

									</div>
								</li>
								<li>
									<a
										href="#signin-modal"
										@click.prevent="openSignInModal"
									>Sign in / Sign up</a>
								</li>
							</ul>
						</li>
					</ul>
				</div>
			</div>
		</div>

		<div class="header-middle">
			<div :class="isFullwidth ? 'container-fluid' : 'container'">
				<div class="header-left">
					<button
						class="mobile-menu-toggler"
						@click="openMobileMenu"
					>
						<span class="sr-only">Toggle mobile menu</span>
						<i class="icon-bars"></i>
					</button>

					<nuxt-link
						to="/"
						class="logo"
					>
						<img
							v-lazy="'./images/home/logo.png'"
							class="bg-transparent"
							alt="Molla Logo"
							width="105"
							height="25"
						/>
					</nuxt-link>
				</div>

				<div class="header-center">
					<header-search></header-search>
				</div>

				<div class="header-right">
					<div class="header-dropdown-link">
						<compare-menu></compare-menu>

						<wishlist-menu></wishlist-menu>

						<cart-menu></cart-menu>
					</div>
				</div>
			</div>
		</div>

		<sticky-header>
			<div class="header-bottom sticky-header">
				<div :class="isFullwidth ? 'container-fluid' : 'container'">
					<div class="header-center">
						<main-menu></main-menu>
					</div>

					<div class="header-right">
						<i class="la la-lightbulb-o"></i>
						<p class="text-dark">Clearance Up to 30% Off</p>
					</div>
				</div>
			</div>
		</sticky-header>
	</header>
</template>

<script>
import CartMenu from '~/components/partial/headers/shared/CartMenu';
import WishlistMenu from '~/components/partial/headers/shared/WishlistMenu';
import CompareMenu from '~/components/partial/headers/shared/CompareMenu';
import MainMenu from '~/components/partial/headers/shared/MainMenu';
import HeaderSearch from '~/components/partial/headers/shared/HeaderSearch';
import StickyHeader from '~/components/elements/StickyHeader';

export default {
	components: {
		CartMenu,
		WishlistMenu,
		CompareMenu,
		MainMenu,
		HeaderSearch,
		StickyHeader
	},
	computed: {
		isFullwidth: function() {
			return this.$route.path.includes('fullwidth');
		}
	},
	methods: {
		openSignInModal: function() {
			this.$modal.show(
				() => import('~/components/elements/modals/SignInModal'),
				{},
				{ width: '575', height: 'auto', adaptive: true }
			);
		},
		openMobileMenu: function() {
			document.querySelector('body').classList.add('mmenu-active');
		}
	}
};
</script>