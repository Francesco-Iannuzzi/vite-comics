<script>
export default {
    name: 'SiteMain',
    data() {
        return {
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
        <section class="content">
            <div class="container">
                <h1>Content goes here</h1>
            </div>
        </section>
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
    </main>
</template>


<style lang="scss" scoped></style>