<script>
export default {
    name: 'ProductItem',
    props: {
        thumb: String,
        price: String,
        series: String,
        type: String,
    }
}
</script>

<template>
    <div class="col">
        <div class="card border-0">
            <div class="card-img-top">
                <img :src="thumb" alt="">
            </div>
            <!-- /card-img-top -->
            <div class="card-body px-0">
                <h4 class="card-text text-uppercase">
                    {{ series }}
                </h4>
            </div>
            <!-- /card-body -->
        </div>
        <!-- /card -->
    </div>
    <!-- /col -->
</template>

<style lang="scss" scoped></style>