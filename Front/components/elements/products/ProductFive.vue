<template>
    <div class="product product-11 text-center my-4">
        <figure class="product-media">
            <!---->
            <span class="product-label label-circle label-sale">Sale</span>
            <span class="product-label label-circle label-top">Top</span>
            <!---->
            <a
                href="/vue/molla/demo-1/product/default/butler-stool-ladder"
                class=""
                ><img
                    alt="Product"
                    class="product-image fade-in"
                    :data-src="`${baseUrl}/${product.photo}`"
                    v-lazy="`${baseUrl}/${product.photo}`"
                    width="300"
                    height="300" />
                <img
                    alt="Product"
                    class="product-image-hover"
                    :data-src="`${baseUrl}/${product.photo}`"
                    v-lazy="`${baseUrl}/${product.photo}`"
                    width="300"
                    height="300"
            /></a>
            <div class="product-action-vertical">
                <a
                    href="javascript:;"
                    class="btn-product-icon btn-wishlist btn-expandable"
                    ><span>add to wishlist</span></a
                >
                <a
                    href="javascript:;"
                    title="Quick view"
                    class="btn-product-icon btn-quickview"
                    ><span>Quick view</span></a
                >
                <!---->
            </div>
        </figure>
        <div class="product-body">
            <div class="product-cat">
                <span
                    ><a
                        href="/vue/molla/demo-1/shop/sidebar/list?category=furniture"
                        class=""
                        >{{product.category_id}}</a
                    >
                </span>
            </div>
            <h3 class="product-title">
                <a
                    href="/vue/molla/demo-1/product/default/butler-stool-ladder"
                    class=""
                    >{{product.name}}</a
                >
            </h3>
            <div class="product-price">
                <span class="new-price">${{product.price}}</span>
                <!-- <span class="old-price">${{product.price}}</span> -->
            </div>
            <div class="ratings-container">
                <div class="ratings">
                    <div class="ratings-val" style="width: 60%"></div>
                    <span class="tooltip-text">3.00</span>
                </div>
                <span class="ratings-text">( 2 Reviews )</span>
            </div>
        </div>
        <div class="product-action">
            <button class="btn-product btn-cart">
                <span>add to cart</span>
            </button>
        </div>
    </div>
</template>

<script>
import { mapGetters, mapActions } from 'vuex';
import { baseUrl } from '~/repositories/repository';
export default {
    props: {
        product: Object,
    },
    data: function () {
        return {
            baseUrl: process.env.APP_URL,
            maxPrice: 0,
            minPrice: 99999,
        };
    },
    computed: {
        // ...mapGetters('cart', ['canAddToCart']),
        // ...mapGetters('wishlist', ['isInWishlist']),
        // ...mapGetters('compare', ['isInCompare'])
    },

    created: function () {
        // let min = this.minPrice;
        // let max = this.maxPrice;
        // this.product.variants.map(item => {
        //     if (min > item.price) min = item.price;
        //     if (max < item.price) max = item.price;
        // }, []);
        // if (this.product.variants.length == 0) {
        //     min = this.product.sale_price
        //         ? this.product.sale_price
        //         : this.product.price;
        //     max = this.product.price;
        // }
        // this.minPrice = min;
        // this.maxPrice = max;
    },
    methods: {
        // ...mapActions('cart', ['addToCart']),
        // ...mapActions('wishlist', ['addToWishlist']),
        // ...mapActions('compare', ['addToCompare']),
        // quickView: function() {
        //     this.$modal.show(
        //         () => import('~/components/elements/modals/QuickViewModal'),
        //         {
        //             product: this.product
        //         },
        //         { width: '1030', height: 'auto', adaptive: true }
        //     );
        // }
        getImage: function (data) {
            return data.photo;
        },
    },
};
</script>