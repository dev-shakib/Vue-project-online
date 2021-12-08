<template>
	<div
		class="main home-page"
		style="background-color: #fafafa;"
	>
		<div class="intro-section">
			<div class="container mt-2">
				<div class="row">
					<div class="col-lg-5cols d-none d-lg-block">
						<nav class="side-nav">
							<div class="sidenav-title letter-spacing-normal font-size-normal d-flex justify-content-xl-between align-items-center bg-primary justify-content-center text-truncate">
								Browse Categories
								<i class="icon-bars float-right h5 text-white m-0 d-none d-xl-block"></i>
							</div>

							<ul
								class="menu-vertical sf-arrows sf-js-enabled"
								style="touch-action: pan-y;"
							>
								<!-- <li class="megamenu-container">
									<a
										class="sf-with-ul text-dark"
										href="#"
									>
										<i class="icon-laptop"></i>Electronics</a>
									<div class="megamenu">
										<div class="row ">
											<div class="col-md-8">
												<div class="menu-col">
													<div class="row">
														<div class="col-md-6">
															<div class="menu-title">Laptops &amp; Computers</div>

															<ul>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=computers">Desktop Computers</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=computers">Monitors</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=laptops">Laptops</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=tablets">iPad &amp; Tablets</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=computers">Hard Drives &amp; Storage</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=computers">Printers &amp; Supplies</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=computers">Computer Accessories</nuxt-link>
																</li>
															</ul>

															<div class="menu-title">TV &amp; Video</div>

															<ul>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=TV">TVs</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=electronics">Home Audio Speakers</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=computers">Projectors</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=computers">Media Streaming Devices</nuxt-link>
																</li>
															</ul>
														</div>

														<div class="col-md-6">
															<div class="menu-title">Cell Phones</div>

															<ul>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=electronics">Carrier Phones</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=electronics">Unlocked Phones</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=electronics">Phone &amp; Cellphone Cases</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=electronics">Cellphone Chargers </nuxt-link>
																</li>
															</ul>

															<div class="menu-title">Digital Cameras</div>

															<ul>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=cameras">Digital SLR Cameras</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=cameras">Sports &amp; Action Cameras</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=cameras">Camcorders</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=cameras">Camera Lenses</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=cameras">Photo Printer</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=cameras">Digital Memory Cards</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=cameras">Camera Bags, Backpacks &amp;
																		Cases</nuxt-link>
																</li>
															</ul>
														</div>

													</div>

												</div>

											</div>

											<div class="col-md-4">
												<div class="banner banner-overlay h-100">
													<nuxt-link
														to="/shop/sidebar/2cols"
														class="banner banner-menu"
													>
														<img
															v-lazy="'./images/home/menu/banner-1.jpg'"
															alt="Banner"
															width="280"
															height="440"
														>
													</nuxt-link>
												</div>

											</div>

										</div>

									</div>

								</li>
								<li class="megamenu-container">
									<a
										class="sf-with-ul text-dark"
										href="#"
									>
										<i class="icon-couch"></i>Furniture</a>

									<div class="megamenu">
										<div class="row ">
											<div class="col-md-8">
												<div class="menu-col">
													<div class="row">
														<div class="col-md-6">
															<div class="menu-title">Bedroom</div>

															<ul>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=beds">Beds, Frames &amp; Bases</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">Dressers</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">Nightstands</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=beds">Kids' Beds &amp; Headboards</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">Armoires</nuxt-link>
																</li>
															</ul>

															<div class="menu-title">Living Room</div>

															<ul>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">Coffee Tables</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">Chairs</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">Tables</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">Futons &amp; Sofa Beds</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">Cabinets &amp; Chests</nuxt-link>
																</li>
															</ul>
														</div>

														<div class="col-md-6">
															<div class="menu-title">Office</div>

															<ul>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">Office Chairs</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">Desks</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">Bookcases</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">File Cabinets</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">Breakroom Tables</nuxt-link>
																</li>
															</ul>

															<div class="menu-title">Kitchen &amp; Dining</div>

															<ul>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">Dining Sets</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">Kitchen Storage Cabinets</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">Bakers Racks</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">Dining Chairs</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">Dining Room Tables</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=furniture">Bar Stools</nuxt-link>
																</li>
															</ul>
														</div>

													</div>

												</div>

											</div>

											<div class="col-md-4">
												<div class="banner banner-overlay h-100">
													<nuxt-link
														to="/shop/sidebar/3cols"
														class="banner banner-menu"
													>
														<img
															v-lazy="'./images/home/menu/banner-2.jpg'"
															alt="Banner"
															width="280"
															height="440"
														>
													</nuxt-link>
												</div>

											</div>

										</div>

									</div>

								</li>
								<li class="megamenu-container">
									<a
										class="sf-with-ul text-dark"
										href="#"
									>
										<i class="icon-concierge-bell"></i>Cooking</a>

									<div class="megamenu">
										<div class="menu-col">
											<div class="row">
												<div class="col-md-4">
													<div class="menu-title">Cookware</div>

													<ul>
														<li>
															<nuxt-link to="/shop/sidebar/list?category=furniture">Cookware Sets</nuxt-link>
														</li>
														<li>
															<nuxt-link to="/shop/sidebar/list?category=furniture">Pans, Griddles &amp;Woks</nuxt-link>
														</li>
														<li>
															<nuxt-link to="/shop/sidebar/list?category=furniture">Pots</nuxt-link>
														</li>
														<li>
															<nuxt-link to="/shop/sidebar/list?category=furniture">Skillets &amp;Grill Pans</nuxt-link>
														</li>
														<li>
															<nuxt-link to="/shop/sidebar/list?category=furniture">Kettles</nuxt-link>
														</li>
														<li>
															<nuxt-link to="/shop/sidebar/list?category=furniture">Soup &amp;Stockpots</nuxt-link>
														</li>
													</ul>
												</div>

												<div class="col-md-4">
													<div class="menu-title">Dinnerware &amp;Tabletop</div>

													<ul>
														<li>
															<nuxt-link to="/shop/sidebar/list?category=decor">Plates</nuxt-link>
														</li>
														<li>
															<nuxt-link to="/shop/sidebar/list?category=decor">Cups &amp;Mugs</nuxt-link>
														</li>
														<li>
															<nuxt-link to="/shop/sidebar/list?category=decor">Trays &amp;Platters</nuxt-link>
														</li>
														<li>
															<nuxt-link to="/shop/sidebar/list?category=decor">Coffee &amp;Tea Serving</nuxt-link>
														</li>
														<li>
															<nuxt-link to="/shop/sidebar/list?category=decor">Salt &amp;Pepper Shaker</nuxt-link>
														</li>
													</ul>
												</div>

												<div class="col-md-4">
													<div class="menu-title">Cooking Appliances</div>

													<ul>
														<li>
															<nuxt-link to="/shop/sidebar/list?category=furniture">Microwaves</nuxt-link>
														</li>
														<li>
															<nuxt-link to="/shop/sidebar/list?category=furniture">Coffee Makers</nuxt-link>
														</li>
														<li>
															<nuxt-link to="/shop/sidebar/list?category=furniture">Mixers &amp;Attachments</nuxt-link>
														</li>
														<li>
															<nuxt-link to="/shop/sidebar/list?category=furniture">Slow Cookers</nuxt-link>
														</li>
														<li>
															<nuxt-link to="/shop/sidebar/list?category=furniture">Air Fryers</nuxt-link>
														</li>
														<li>
															<nuxt-link to="/shop/sidebar/list?category=furniture">Toasters &amp;Ovens</nuxt-link>
														</li>
													</ul>
												</div>

											</div>

											<div class="row menu-banners">
												<div class="col-md-4">
													<div class="banner h-100">
														<nuxt-link to="/shop/market">
															<img
																v-lazy="'./images/home/menu/1.jpg'"
																alt="image"
																width="251"
																height="141"
															>
														</nuxt-link>
													</div>

												</div>

												<div class="col-md-4">
													<div class="banner h-100">
														<nuxt-link to="/shop/sidebar/list">
															<img
																v-lazy="'./images/home/menu/2.jpg'"
																alt="image"
																width="251"
																height="141"
															>
														</nuxt-link>
													</div>

												</div>

												<div class="col-md-4 h-100">
													<div class="banner">
														<nuxt-link to="/shop/sidebar/list">
															<img
																v-lazy="'./images/home/menu/3.jpg'"
																alt="image"
																width="251"
																height="141"
															>
														</nuxt-link>
													</div>

												</div>

											</div>

										</div>

									</div>

								</li>
								<li class="megamenu-container">
									<a
										class="sf-with-ul text-dark"
										href="#"
									>
										<i class="icon-tshirt"></i>Clothing</a>

									<div class="megamenu">
										<div class="row ">
											<div class="col-md-8">
												<div class="menu-col">
													<div class="row">
														<div class="col-md-6">
															<div class="menu-title">Women</div>

															<ul>
																<li>
																	<nuxt-link to="/shop/sidebar/list">
																		<strong>New Arrivals</strong>
																	</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list">
																		<strong>Best Sellers</strong>
																	</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list">
																		<strong>Trending</strong>
																	</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=clothing">Clothing</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=shoes">Shoes</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=bags">Bags</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=accessories">Accessories</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=accessories">Jewlery &amp;Watches</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/2cols">
																		<strong>Sale</strong>
																	</nuxt-link>
																</li>
															</ul>
														</div>

														<div class="col-md-6">
															<div class="menu-title">Men</div>

															<ul>
																<li>
																	<nuxt-link to="/shop/sidebar/list">
																		<strong>New Arrivals</strong>
																	</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list">
																		<strong>Best Sellers</strong>
																	</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list">
																		<strong>Trending</strong>
																	</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=clothing">Clothing</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=shoes">Shoes</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=bags">Bags</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=accessories">Accessories</nuxt-link>
																</li>
																<li>
																	<nuxt-link to="/shop/sidebar/list?category=accessories">Jewlery &amp;Watches</nuxt-link>
																</li>
															</ul>
														</div>

													</div>

												</div>

											</div>

											<div class="col-md-4">
												<div class="banner banner-overlay">
													<nuxt-link
														to="/shop/market"
														class="banner banner-menu"
													>
														<img
															v-lazy="'./images/home/menu/banner-3.jpg'"
															alt="Banner"
															width="280"
															height="347"
														>
													</nuxt-link>
												</div>

											</div>

										</div>

										<div class="menu-col menu-brands d-flex flex-column justify-content-center">
											<div class="row">
												<div class="col-lg-2">
													<a
														href="#"
														class="brand h-100"
													>
														<img
															v-lazy="'./images/brands/1.png'"
															class="bg-transparent"
															alt="Brand Name"
															width="100"
															height="23"
														>
													</a>
												</div>

												<div class="col-lg-2">
													<a
														href="#"
														class="brand h-100"
													>
														<img
															v-lazy="'./images/brands/2.png'"
															class="bg-transparent"
															alt="Brand Name"
															width="101"
															height="34"
														>
													</a>
												</div>

												<div class="col-lg-2">
													<a
														href="#"
														class="brand h-100"
													>
														<img
															v-lazy="'./images/brands/3.png'"
															class="bg-transparent"
															alt="Brand Name"
															width="100"
															height="30"
														>
													</a>
												</div>

												<div class="col-lg-2">
													<a
														href="#"
														class="brand h-100"
													>
														<img
															v-lazy="'./images/brands/4.png'"
															class="bg-transparent"
															alt="Brand Name"
															width="101"
															height="39"
														>
													</a>
												</div>

												<div class="col-lg-2">
													<a
														href="#"
														class="brand h-100"
													>
														<img
															v-lazy="'./images/brands/5.png'"
															class="bg-transparent"
															alt="Brand Name"
															width="100"
															height="48"
														>
													</a>
												</div>

												<div class="col-lg-2">
													<a
														href="#"
														class="brand h-100"
													>
														<img
															v-lazy="'./images/brands/6.png'"
															class="bg-transparent"
															alt="Brand Name"
															width="100"
															height="23"
														>
													</a>
												</div>

											</div>

										</div>

									</div>

								</li>
								<li>
									<a
										href="#"
										class="text-dark"
									>
										<i class="icon-blender"></i>Home Appliances</a>
								</li>
								<li>
									<nuxt-link
										to="/shop/sidebar/3cols?category=women"
										class="text-dark"
									>
										<i class="icon-heartbeat"></i>Healthy &amp; Beauty</nuxt-link>
								</li>
								<li>
									<nuxt-link
										to="/shop/sidebar/3cols?category=shoes"
										class="text-dark"
									>
										<i class="icon-shoe-prints"></i>Shoes &amp; Boots</nuxt-link>
								</li>
								<li>
									<nuxt-link
										to="/shop/sidebar/3cols?category=travel"
										class="text-dark"
									>
										<i class="icon-map-signs"></i>Travel &amp; Outdoor</nuxt-link>
								</li>
								<li>
									<nuxt-link
										to="/shop/sidebar/3cols?category=electronics"
										class="text-dark"
									>
										<i class="icon-mobile-alt"></i>Smart Phones</nuxt-link>
								</li>
								<li>
									<nuxt-link
										to="/shop/sidebar/3cols?category=TV"
										class="text-dark"
									>
										<i class="icon-tv"></i>TV &amp; Audio</nuxt-link>
								</li> -->
								<li v-for="category of categories" v-bind:key="category.id">
									<nuxt-link
										to="/shop/sidebar/3cols?category=gift"
										class="text-dark"
									>
										<i class="icon-gift"></i>{{category.name}}</nuxt-link>
								</li>
							</ul>

						</nav>

					</div>

					<div class="col-lg-3-5cols col-md-9 col-12 mb-md-0 mb-2">
						<div class="intro-slider-container">
							<div class="swiper-carousel swiper-1">
								<div v-swiper:swiper1="carouselSetting1">
									<div class="swiper-wrapper">
										<div class="swiper-slide">
											<div
												class="intro-slide bg-image d-flex align-items-center"
												style="background-color:#e8eded;"
												v-lazy:background-image="'./images/home/slider/slide-1.jpg'"
											>
												<div class="intro-content">
													<h3 class="intro-subtitle font-size-normal text-dark font-weight-normal text-uppercase">
														Trade-In Offer</h3>

													<h1 class="intro-title text-dark font-weight-bold mb-0">
														Multi-motion
														<br>Food Processor
													</h1>

													<div class="intro-price text-dark font-weight-normal">
														<sup class="font-weight-normal">from
															<span class="text-primary font-weight-normal">$</span>
														</sup>
														<span class="text-primary font-weight-bold">199
															<sup class="font-weight-normal">.99</sup>
														</span>
													</div>

													<nuxt-link
														to="/shop/sidebar/4cols"
														class="btn btn-primary text-uppercase text-dark"
													>
														<span>Shop Now</span>
														<i class="icon-long-arrow-right"></i>
													</nuxt-link>
												</div>

											</div>
										</div>
										<div class="swiper-slide">
											<div
												class="intro-slide bg-image d-flex align-items-center"
												style="background-color:#e8eded;"
												v-lazy:background-image="'./images/home/slider/slide-2.jpg'"
											>
												<div class="intro-content">
													<h3 class="intro-subtitle font-size-normal text-dark font-weight-normal text-uppercase">
														New Arrivals</h3>

													<h1 class="intro-title text-white font-weight-bold mb-0">
														New Collection!
														<br>Air More Uptempo
													</h1>

													<div class="intro-price text-white font-weight-normal position-relative mb-3">
														<div class="position-relative">
															<sup class="font-weight-normal">from</sup>
															<span class="font-weight-bold ml-n2">
																$79
																<sup class="font-weight-normal">.99</sup>
															</span>
														</div>
														<img
															v-lazy="'./images/home/slider/slide-2-brushpng.png'"
															class="position-absolute w-auto h-auto bg-transparent"
															alt="Category"
															width="85"
															height="35"
														>
													</div>

													<nuxt-link
														to="/shop/market"
														class="btn btn-primary text-uppercase text-dark"
													>
														<span>Shop Now</span>
														<i class="icon-long-arrow-right"></i>
													</nuxt-link>
												</div>

											</div>
										</div>
										<div class="swiper-slide">
											<div
												class="intro-slide bg-image d-flex align-items-center"
												style="background-color:#e8eded;"
												v-lazy:background-image="'./images/home/slider/slide-3.jpg'"
											>
												<div class="intro-content">
													<h3 class="intro-subtitle font-size-normal text-white font-weight-normal text-uppercase">
														Design special</h3>

													<h1 class="intro-title text-white font-weight-bold mt-0 my-2">
														Lamps Made
														<br>Of Natural Materials
													</h1>

													<div class="intro-text text-secondary font-weight-lighter mb-4">
														Extra 25% Off
													</div>

													<nuxt-link
														to="/shop/sidebar/3cols"
														class="btn btn-primary text-uppercase text-dark"
													>
														<span>Shop Now</span>
														<i class="icon-long-arrow-right"></i>
													</nuxt-link>
												</div>

											</div>
										</div>
									</div>
								</div>
								<div class="swiper-dots swiper-dots-inner"></div>
							</div>
						</div>
					</div>

					<div class="col-lg-5cols col-md-3 col-12 mb-md-0 mb-2">
						<div
							class="banner banner-overlay bg-image h-100 mb-0"
							style="background-color: #f1f1f1;"
							v-lazy:background-image="'./images/home/banners/banner-1.jpg'"
						>
							<div class="banner-content position-relative pt-0 pb-md-7 d-flex flex-column">
								<div class="title text-center text-uppercase text-dark font-weight-bold mb-0">
									Phantom 3
									<br>Professional
								</div>
								<div class="price text-center">
									<sup class="text-dark font-weight-normal">from
										<span class="text-primary font-weight-normal">$</span>
									</sup>
									<span class="text-primary font-weight-bold">
										599.
									</span>
									<sup
										class="text-primary font-weight-bold"
										style="font-size: 55%; top: -.6em;"
									>99</sup>
								</div>
							</div>

						</div>

					</div>
				</div>
			</div>
		</div>

		<div class="container icon-boxes-section">
			<div class="icon-boxes-container py-4 bg-lighter mb-2 mt-2 row">
				<div class="icon-box col-sm-12 col-md-6 col-lg-3 mb-0 d-md-flex align-items-md-center text-center text-md-left mx-md-0 mx-auto">
					<span class="icon-box-icon mb-0">
						<i class="icon-truck py-2 pt-0 second-primary-color"></i>
					</span>
					<div class="icon-box-content">
						<h3 class="icon-box-title font-size-normal mb-0 font-weight-bold text-uppercase second-primary-color">
							Payment &amp; Delivery</h3>
						<p class="font-weight-light second-primary-color">Free shipping for orders over $50</p>
					</div>
				</div>
				<div class="icon-box col-sm-12 col-md-6 col-lg-3 mb-0 d-md-flex align-items-md-center text-center text-md-left mx-md-0 mx-auto">
					<span class="icon-box-icon text-dark mb-0">
						<i class="icon-rotate-left py-2 pt-0 second-primary-color"></i>
					</span>
					<div class="icon-box-content">
						<h3 class="icon-box-title font-size-normal mb-0 font-weight-bold text-uppercase second-primary-color">
							Return &amp; Refund</h3>
						<p class="font-weight-light second-primary-color">Free 100% money back guarantee</p>
					</div>
				</div>
				<div class="icon-box col-sm-12 col-md-6 col-lg-3 mb-0 d-md-flex align-items-md-center text-center text-md-left mx-md-0 mx-auto">
					<span class="icon-box-icon text-dark mb-0">
						<i class="icon-life-ring py-2 pt-0 second-primary-color"></i>
					</span>
					<div class="icon-box-content">
						<h3 class="icon-box-title font-size-normal mb-0 font-weight-bold text-uppercase second-primary-color">
							Quality Support</h3>
						<p class="font-weight-light second-primary-color">Alway online feedback 24/7</p>
					</div>
				</div>
				<div class="icon-box col-sm-12 col-md-6 col-lg-3 mb-0 d-md-flex align-items-md-center text-center text-md-left mx-md-0 mx-auto">
					<span class="icon-box-icon text-dark mb-0">
						<i class="icon-envelope py-2 pt-0 second-primary-color"></i>
					</span>
					<div class="icon-box-content">
						<h3 class="icon-box-title font-size-normal mb-0 font-weight-bold text-uppercase second-primary-color">
							JOIN OUR NEWSLETTER</h3>
						<p class="font-weight-light second-primary-color">10% off by subscribing to our
							newsletter</p>
					</div>
				</div>
			</div>
			<hr class="mt-2 mb-0">
		</div>

		<div class="container banner-group-1">
			<div class="categories mb-3">
				<h3 class="title text-center font-weight-bold mt-4">Explore Popular Categories</h3>
				<div class="swiper-carousel swiper-2">
					<div v-swiper:swiper2="carouselSetting2">
						<div class="swiper-wrapper">
							<div class="swiper-slide">
								<div class="category position-relative">
									<div class="category-image">
										<nuxt-link to="/shop/market">
											<img
												v-lazy="'./images/home/categories/1.png'"
												class="w-100 bg-transparent"
												alt="Category"
												width="166"
												height="160"
											>
										</nuxt-link>
									</div>
									<div class="category-body letter-spacing-normal font-size-normal text-center position-absolute text-uppercase">
										<nuxt-link
											to="/shop/market"
											class="category-title text-truncate font-weight-normal"
										>Clothing</nuxt-link>
									</div>
								</div>
							</div>
							<div class="swiper-slide">
								<div class="category position-relative">
									<div class="category-image">
										<nuxt-link to="/shop/market">
											<img
												v-lazy="'./images/home/categories/2.png'"
												class="w-100 bg-transparent"
												alt="Category"
												width="166"
												height="160"
											>
										</nuxt-link>
									</div>
									<div class="category-body letter-spacing-normal font-size-normal text-center position-absolute text-uppercase">
										<nuxt-link
											to="/shop/market"
											class="category-title text-truncate font-weight-normal"
										>Laptop</nuxt-link>
									</div>
								</div>
							</div>
							<div class="swiper-slide">
								<div class="category position-relative">
									<div class="category-image">
										<nuxt-link to="/shop/market">
											<img
												v-lazy="'./images/home/categories/3.png'"
												class="w-100 bg-transparent"
												alt="Category"
												width="166"
												height="160"
											>
										</nuxt-link>
									</div>
									<div class="category-body letter-spacing-normal font-size-normal text-center position-absolute text-uppercase">
										<nuxt-link
											to="/shop/market"
											class="category-title text-truncate font-weight-normal"
										>Lighting</nuxt-link>
									</div>
								</div>
							</div>
							<div class="swiper-slide">
								<div class="category position-relative">
									<div class="category-image">
										<nuxt-link to="/shop/market">
											<img
												v-lazy="'./images/home/categories/4.png'"
												class="w-100 bg-transparent"
												alt="Category"
												width="166"
												height="160"
											>
										</nuxt-link>
									</div>
									<div class="category-body letter-spacing-normal font-size-normal text-center position-absolute text-uppercase">
										<nuxt-link
											to="/shop/market"
											class="category-title text-truncate font-weight-normal"
										>Smart Phones</nuxt-link>
									</div>
								</div>
							</div>
							<div class="swiper-slide">
								<div class="category position-relative">
									<div class="category-image">
										<nuxt-link to="/shop/market">
											<img
												v-lazy="'./images/home/categories/5.png'"
												class="w-100 bg-transparent"
												alt="Category"
												width="166"
												height="160"
											>
										</nuxt-link>
									</div>
									<div class="category-body letter-spacing-normal font-size-normal text-center position-absolute text-uppercase">
										<nuxt-link
											to="/shop/market"
											class="category-title text-truncate font-weight-normal"
										>Televisions</nuxt-link>
									</div>
								</div>
							</div>
							<div class="swiper-slide">
								<div class="category position-relative">
									<div class="category-image">
										<nuxt-link to="/shop/market">
											<img
												v-lazy="'./images/home/categories/6.png'"
												class="w-100 bg-transparent"
												alt="Category"
												width="166"
												height="160"
											>
										</nuxt-link>
									</div>
									<div class="category-body letter-spacing-normal font-size-normal text-center position-absolute text-uppercase">
										<nuxt-link
											to="/shop/market"
											class="category-title text-truncate font-weight-normal"
										>Cooking</nuxt-link>
									</div>
								</div>
							</div>
							<div class="swiper-slide">
								<div class="category position-relative">
									<div class="category-image">
										<nuxt-link to="/shop/market">
											<img
												v-lazy="'./images/home/categories/7.png'"
												class="w-100 bg-transparent"
												alt="Category"
												width="166"
												height="160"
											>
										</nuxt-link>
									</div>
									<div class="category-body letter-spacing-normal font-size-normal text-center position-absolute text-uppercase">
										<nuxt-link
											to="/shop/market"
											class="category-title text-truncate font-weight-normal"
										>Furniture</nuxt-link>
									</div>
								</div>
							</div>
							<div class="swiper-slide">
								<div class="category position-relative">
									<div class="category-image">
										<nuxt-link to="/shop/market">
											<img
												v-lazy="'./images/home/categories/8.png'"
												class="w-100 bg-transparent"
												alt="Category"
												width="166"
												height="160"
											>
										</nuxt-link>
									</div>
									<div class="category-body letter-spacing-normal font-size-normal text-center position-absolute text-uppercase">
										<nuxt-link
											to="/shop/market"
											class="category-title text-truncate font-weight-normal"
										>Game &amp; Toy</nuxt-link>
									</div>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
			<div class="row">
				<div class="col-md-4 mb-md-0 mb-2">
					<div
						class="banner banner-overlay bg-image h-100 d-flex justify-content-end mb-0"
						v-lazy:background-image="'./images/home/banners/banner-2.jpg'"
					>
						<div class="banner-content position-relative d-flex flex-column justify-content-center">
							<h4 class="banner-subtitle letter-spacing-normal font-size-normal text-white d-none d-sm-block font-weight-light">
								<nuxt-link to="/shop/sidebar/3cols">Headphone Savings</nuxt-link>
							</h4>

							<h3 class="banner-title text-white mb-0 font-weight-bold">
								<nuxt-link to="/shop/sidebar/3cols">Headphone
									<br>Trending
									<br>JBL Harman</nuxt-link>
							</h3>

							<nuxt-link
								to="/shop/sidebar/3cols"
								class="btn font-size-normal btn-primary text-uppercase text-dark btn-rounded text-center"
							>
								<span>Shop Now </span>
								<i class="icon-long-arrow-right d-inline-block"></i>
							</nuxt-link>
						</div>

					</div>
				</div>
				<div class="col-md-4 mb-md-0 mb-2">
					<div
						class="banner banner-overlay bg-image h-100 d-flex justify-content-end mb-0"
						v-lazy:background-image="'./images/home/banners/banner-3.jpg'"
					>
						<div class="banner-content position-relative d-flex flex-column justify-content-center">
							<h4 class="banner-subtitle letter-spacing-normal font-size-normal d-none d-sm-block font-weight-light">
								<nuxt-link to="/shop/sidebar/list">Weekend Sale</nuxt-link>
							</h4>

							<h3 class="banner-title mb-0 font-weight-bold">
								<nuxt-link to="/shop/sidebar/list">Home Furnishings
									<br>Outdoor &amp; Office</nuxt-link>
							</h3>

							<nuxt-link
								to="/shop/sidebar/list"
								class="btn font-size-normal btn-primary text-uppercase text-dark btn-rounded text-center d-inline-block"
							>
								<span>Shop Now </span>
								<i class="icon-long-arrow-right d-inline-block"></i>
							</nuxt-link>
						</div>

					</div>
				</div>
				<div class="col-md-4 mb-md-0 mb-2">
					<div
						class="banner banner-overlay bg-image h-100 d-flex justify-content-end mb-0"
						v-lazy:background-image="'./images/home/banners/banner-4.jpg'"
					>
						<div class="banner-content position-relative d-flex flex-column justify-content-center">
							<h4 class="banner-subtitle letter-spacing-normal font-size-normal text-white font-weight-light d-none d-sm-block">
								<nuxt-link to="/shop/market">Amazing Value</nuxt-link>
							</h4>

							<h3 class="banner-title text-white mb-0 font-weight-bold">
								<nuxt-link to="/shop/market">Clothes Trending
									<br>Spring / Summer </nuxt-link>
							</h3>

							<h4 class="banner-text font-weight-normal text-secondary mb-0 font-weight-light">from
								$12.99</h4>
							<nuxt-link
								to="/shop/market"
								class="btn font-size-normal btn-primary text-uppercase text-dark btn-rounded text-center"
							>
								<span>Discover Now </span>
								<i class="icon-long-arrow-right d-inline-block"></i>
							</nuxt-link>
						</div>

					</div>
				</div>
			</div>
		</div>

		<top-collection
			v-if="loaded"
			:topProducts="topProducts"
		></top-collection>

		<div class="container">
			<div class="row">
				<div class="col-12">
					<div class="banner banner-rad mt-5">
						<div
							class="bg-image d-flex justify-content-center pt-4 pb-4 mb-4"
							v-lazy:background-image="'./images/home/bg-1.jpg'"
						>
							<div class="banner-content position-relative pt-0">
								<h4 class="banner-subtitle letter-spacing-normal font-size-normal text-white text-center pt-0 mb-1">
									<nuxt-link to="/shop/market">Discount</nuxt-link>
								</h4>

								<h3 class="banner-title text-white text-center font-weight-bold mb-0">
									<nuxt-link to="/shop/market">New Lower Prices On Hundreds
										<br> Of Home Furnishings</nuxt-link>
								</h3>

								<h4 class="banner-text text-secondary text-center font-weight-light text-uppercase">
									Sale Up 35% Off</h4>
							</div>

						</div>
					</div>
				</div>
			</div>
		</div>

		<electronics-collection
			v-if="loaded"
			:electronics="electronics"
		></electronics-collection>

		<fashion-collection
			v-if="loaded"
			:products="products"
		></fashion-collection>

		<div class="container banner-group-2">
			<div class="row row-sm">
				<div class="col-md-6">
					<div
						class="banner banner-overlay bg-image"
						v-lazy:background-image="'./images/home/banners/banner-5.jpg'"
					>
						<div class="banner-content banner-content-left position-relative">
							<h4 class="banner-subtitle letter-spacing-normal font-size-normal font-weight-light mb-1">
								<a href="#">Spring Sale is Coming</a>
							</h4>

							<h3 class="banner-title font-weight-bold mb-0">
								<a href="#">All Smartwatches
									<br>&amp; Accessories Discount</a>
							</h3>

							<h4 class="banner-text text-secondary font-weight-normal">15% off</h4>
							<nuxt-link
								to="/shop/sidebar/list"
								class="btn-product font-size-normal text-uppercase text-dark text-decoration-none btn-rounded"
							>Shop
								Now&nbsp;&nbsp;
								<i class="icon-long-arrow-right d-inline-block"></i>
							</nuxt-link>
						</div>

					</div>
				</div>
				<div class="col-md-6">
					<div
						class="banner banner-overlay bg-image"
						v-lazy:background-image="'./images/home/banners/banner-6.jpg'"
					>
						<div class="banner-content banner-content-left position-relative">
							<h4 class="banner-subtitle letter-spacing-normal font-size-normal text-white font-weight-light mb-1">
								<a href="#">Amazing Value</a>
							</h4>

							<h3 class="banner-title text-white font-weight-bold mb-0">
								<a href="#">Headphones Trending
									<br>Audio-Technica Professional</a>
							</h3>

							<h4 class="banner-text text-secondary font-weight-normal">from $129,99</h4>
							<nuxt-link
								to="/shop/sidebar/list"
								class="btn-product font-size-normal text-uppercase text-dark text-decoration-none btn-rounded"
							>Shop
								Now&nbsp;&nbsp;
								<i class="icon-long-arrow-right d-inline-block"></i>
							</nuxt-link>
						</div>

					</div>
				</div>
			</div>
		</div>

		<div class="container product-group mb-lg-7 mb-4">
			<div class="row justify-content-center">
				<special-collection
					v-if="loaded"
					:products="newProducts.slice(0,3)"
					addClass="arrivals col-lg-4 col-md-6 mb-2 mb-xl-0"
					title="New Arrivals"
				></special-collection>
				<special-collection
					v-if="loaded"
					:products="featuredProducts.slice(0,3)"
					addClass="recommend col-lg-4 mb-2 mb-xl-0 order-lg-0 order-md-first"
					title="Recommended Products"
				></special-collection>
				<special-collection
					v-if="loaded"
					:products="topProducts.slice(0,3)"
					addClass="expert col-lg-4 col-md-6 mb-2 mb-xl-0"
					title="Expert Picks"
				></special-collection>
			</div>
		</div>

		<div class="container">
			<div class="products">
			<div class="row">
				<div class="col-6 col-md-4 col-lg-3 col-xl-5col mb-n4" v-for="product of products" :key="product.id">
					<product-five  :product="product"></product-five>
				</div>
			</div>
			</div>
		</div>

			

		<div class="bg-white brand-section pt-5 pb-4">
			<div class="container">
				<div class="swiper-carousel brands-carousel">
					<div v-swiper:swiper14="carouselSetting3">
						<div class="swiper-wrapper">
							<div
								class="swiper-slide"
								v-for="(brand,index) in homeData.brands"
								:key="index"
							>
								<a
									href="#"
									class="brand"
								>
									<img
										v-lazy="brand.image"
										:alt="brand.name"
										:width="brand.width"
										:height="brand.height"
										class="bg-transparent"
									>
								</a>
							</div>
						</div>
					</div>
				</div>
				<hr class="mt-5 mb-0">
			</div>
		</div>

		<blog-section :blogs="blogs"></blog-section>
	</div>
</template>
<script>
import { mapGetters } from 'vuex';

import ElectronicsCollection from '~/components/partial/home/ElectronicsCollection';
import FashionCollection from '~/components/partial/home/FashionCollection';
import SpecialCollection from '~/components/partial/home/SpecialCollection';
import TopCollection from '~/components/partial/home/TopCollection';
import BlogSection from '~/components/partial/home/BlogSection';
import NewsletterModal from '~/components/elements/modals/NewsletterModal';
import Repository, { baseUrl } from '~/repositories/repository.js';
import { attrFilter, catFilter } from '~/utilities/common';
import {
	carouselSettingSingle,
	carouselSettingDefault
} from '~/utilities/carousel';
import { homeData } from '~/utilities/data';
import axios from 'axios'
import ProductFive from '~/components/elements/products/ProductFive.vue';

export default {
	components: {
		SpecialCollection,
		TopCollection,
		ElectronicsCollection,
		FashionCollection,
		BlogSection,
		ProductFive
	},
	data: function() {
		return {
			loaded: false,
			categories: [],
			products: [],
			topProducts: [],
			newProducts: [],
			featuredProducts: [],
			electronics: [],
			blogs: [],
			carouselSetting1: {
				...carouselSettingSingle,
				pagination: {
					el: '.swiper-1 .swiper-dots',
					clickable: true
				}
			},
			carouselSetting2: {
				...carouselSettingDefault,
				slidesPerView: 8,
				spaceBetween: 10,
				breakpoints: {
					1200: {
						slidesPerView: 8
					},
					992: {
						slidesPerView: 6
					},
					768: {
						slidesPerView: 5
					},
					576: {
						slidesPerView: 3
					},
					480: {
						slidesPerView: 2
					}
				}
			},
			carouselSetting3: {
				...carouselSettingDefault,
				slidesPerView: 6,
				spaceBetween: 0,
				breakpoints: {
					992: {
						slidesPerView: 5
					},
					768: {
						slidesPerView: 4
					},
					576: {
						slidesPerView: 3
					},
					480: {
						slidesPerView: 2
					}
				}
			},
			homeData: homeData
		};
	},
	computed: {
		...mapGetters('demo', ['newsletterShow'])
	},
	created: function() {
		this.getProducts();
	},
	mounted: function() {
		if (this.newsletterShow) {
			setTimeout(() => {
				if (this.$route.path == '/' && this.newsletterShow) {
					this.$modal.show(
						NewsletterModal,
						{},
						{ width: '970', height: 'auto', adaptive: true }
					);
				}
			}, 80000);

		}
		this.getCategories();	
		
	},
	methods: {
		getProducts: async function() {
			this.loaded = false;
			// await Repository.get(`${baseUrl}/demo26`)
			// 	.then(response => {
			// 		this.products = response.data.products;
			// 		this.electronics = catFilter(this.products, [
			// 			'electronics'
			// 		]);
			// 		this.newProducts = attrFilter(this.products, 'new');
			// 		this.featuredProducts = attrFilter(
			// 			this.products,
			// 			'featured'
			// 		);
			// 		this.topProducts = attrFilter(this.products, 'top');
			// 		this.blogs = response.data.blogs;
			// 		this.loaded = true;
			// 	})
			// 	.catch(error => ({ error: JSON.stringify(error) }));
			await axios.get( process.env.BASE_URL + '/products')
			.then((res) => {
				this.products = res.data;
				
			})
		},
		getCategories: async function(){
			await axios.get( process.env.BASE_URL + '/categories')
			.then((res) => {
				this.categories = res.data
				
			})
		}
	}
};
</script>