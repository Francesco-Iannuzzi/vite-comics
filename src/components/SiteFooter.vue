<script>
export default {
    name: 'SiteFooter',
    data() {
        return {
            dcComicsList: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News',],
            shopList: ['Shop DC', 'Shop DC Collectibles'],
            dcList: ['Terms Of Use', 'Privacy policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us',],
            sitesList: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa',],
        }
    }
}
</script>

<template>
    <footer>
        <section class="up_footer py-3">
            <div class="container">
                <div class="row d-flex">
                    <div class="footer_left col-5 d-flex justify-content-evenly">
                        <div>
                            <div>
                                <h2 class="text-uppercase">dc comics</h2>
                                <ul>
                                    <li v-for="subSectionDcComics in dcComicsList"><a href="#">{{ subSectionDcComics }}</a>
                                    </li>
                                </ul>
                            </div>
                            <div>
                                <h2 class="text-uppercase">shop</h2>
                                <ul>
                                    <li v-for="subSectionShopList in shopList"><a href="#">{{ subSectionShopList }}</a></li>
                                </ul>
                            </div>
                        </div>
                        <div>
                            <h2 class="text-uppercase">dc</h2>
                            <ul>
                                <li v-for="subSectionDc in dcList"><a href="#">{{ subSectionDc }}</a></li>
                            </ul>
                        </div>
                        <div>
                            <h2 class="text-uppercase">sites</h2>
                            <ul>
                                <li v-for="subSectionSitesList in sitesList"><a href="#">{{ subSectionSitesList }}</a></li>
                            </ul>
                        </div>
                    </div>
                    <div class="footer_right col-7 d-flex justify-content-center">
                        <img src="../assets/img/dc-logo-bg.png" alt="">
                    </div>
                </div>
            </div>
        </section>
        <section class="bottom_footer">
            <div class="container d-flex justify-content-between align-content-center py-3">
                <button class="sign btn">
                    <h2 class="text-uppercase m-0">sign-up now!</h2>
                </button>
                <div class="social d-flex">
                    <h2 class="text-uppercase align-self-center m-0">follow us</h2>
                    <ul class="d-flex align-self-center m-0 gap-2">
                        <li>1</li>
                        <li>2</li>
                        <li>3</li>
                        <li>4</li>
                        <li>5</li>
                    </ul>
                </div>
            </div>
        </section>
    </footer>
</template>


<style lang="scss" scoped></style>