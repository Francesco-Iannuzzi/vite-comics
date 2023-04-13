<script>
export default {
    data() {
        return {
            menuList: ['characters', 'comics', 'movies', 'tv', 'games', 'collectibles', 'videos', 'fans', 'news', 'shop',]
        }
    }
}
</script>

<template>
    <header>
        <div class="container d-flex justify-content-between text-uppercase">
            <div class="logo">
                <img class="ms-2" src="../assets/img/dc-logo.png" alt="">
            </div>
            <nav class="navbar navbar-expand-lg">
                <div class="container-fluid">
                    <div class="collapse navbar-collapse" id="navbarNav">
                        <ul class="navbar-nav">
                            <li v-for="item in menuList" class="nav-item">
                                <a class="nav-link" href="#">{{ item }}</a>
                            </li>
                        </ul>
                    </div>
                </div>
            </nav>
        </div>
    </header>
</template>


<style lang="scss" scoped></style>