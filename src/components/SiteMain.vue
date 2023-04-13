<script>
export default {
    name: 'SiteMain',
    data() {
        return {
            sectionIcon: [
                {
                    images: '../assets/img/buy-comics-digital-comics.png',
                    title: 'digital comics',
                },
                {
                    images: '../assets/img/buy-comics-merchandise.png',
                    title: 'dc merchandise',
                },
                {
                    images: '../assets/img/buy-comics-subscriptions.png',
                    title: 'subscription',
                },
                {
                    images: '../assets/img/buy-comics-shop-locator.png',
                    title: 'comic shop locator',
                },
                {
                    images: '../assets/img/buy-dc-power-visa.svg',
                    title: 'dc power visa',
                },
            ]
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
        <section class="merch text-uppercase">
            <div class="container">
                <ul class="d-flex justify-content-around py-4 px-0 m-0">
                    <li v-for="section in sectionIcon" class="d-flex">
                        <img :src="section.images" :alt="section.title">
                        <h3 class="ms-2 mb-0 align-self-center">{{ section.title }}</h3>
                    </li>
                </ul>
            </div>
        </section>
    </main>
</template>


<style lang="scss" scoped></style>