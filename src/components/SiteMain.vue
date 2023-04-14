<script>
import products from "../data/product.js";
import ProductItem from "../components/ProductItem.vue";
export default {
    name: 'SiteMain',
    components: {
        ProductItem
    },
    data() {
        return {
            products: products,
            sectionBanner: [
                {
                    images: 'buy-comics-digital-comics.png',
                    title: 'digital comics',
                },
                {
                    images: 'buy-comics-merchandise.png',
                    title: 'dc merchandise',
                },
                {
                    images: 'buy-comics-subscriptions.png',
                    title: 'subscription',
                },
                {
                    images: 'buy-comics-shop-locator.png',
                    title: 'comic shop locator',
                },
                {
                    images: 'buy-dc-power-visa.svg',
                    title: 'dc power visa',
                },
            ]
        }
    },
    methods: {
        getImageUrl(name) {
            return new URL(`../assets/img/${name}`, import.meta.url).href
        }
    }
}
</script>

<template>
    <main>
        <section class="jumbotron"></section>
        <!-- /jumbotron -->
        <section class="comics">
            <div class="container">
                <div class="badge_current_comics">
                    <button class="btn text-uppercase rounded-0 border-0">current series</button>
                </div>
                <div class="row row-cols-1 row-cols-sm-2 row row-cols-md-3 row-cols-lg-6 row-cols-xl-6 py-5 text-center">
                    <ProductItem v-for="product in products" :thumb="product.thumb" :series="product.series"></ProductItem>
                </div>
                <!-- /row cards -->
                <div class="badge_load_more d-flex justify-content-center pb-3">
                    <button class="btn text-uppercase rounded-0 border-0">load more</button>
                </div>
                <!-- /badge_load_more -->
            </div>
        </section>
        <!-- /comics -->
        <section class="banner text-uppercase">
            <div class="container">
                <ul class="d-flex justify-content-around py-4 px-0 m-0">
                    <li v-for="section in sectionBanner" class="d-flex">
                        <img :src="getImageUrl(section.images)" :alt="section.title">
                        <h3 class="ms-2 mb-0 align-self-center">{{ section.title }}</h3>
                    </li>
                </ul>
            </div>
        </section>
        <!-- /banner -->
    </main>
</template>


<style lang="scss" scoped></style>