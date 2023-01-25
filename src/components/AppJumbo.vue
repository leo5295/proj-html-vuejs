<script>
export default {

}
</script>
<template lang="">
    <div class="container-fluid bg paw">
        <div class="row">
            <div class="col-4 text-center">
                <span class="text-center"><span><i class="fa-regular fa-map"></i></span> International Shipping Services</span>
            </div>
            <div class="col-4 text-center">
                <span class="text-center"><span><i class="fa-regular fa-clock"></i></span> See our store hours and services</span>
            </div>
            <div class="col-4 text-center">
                <span class="text-center"><span><i class="fa-solid fa-check"></i></span> We price match to give you the best deals</span>
            </div>

        </div>
    </div>
    <div class="bg-img">
        <img src="https://avada.theme-fusion.com/pet-supplies/wp-content/uploads/sites/139/2020/04/banner-5@2x-scaled.jpg" alt="">
    </div>
</template>
<style lang="scss" scoped>
@use '../style/generals.scss';

img {
    width: 100%;
}

.paw {
    background: url("../assets/img/bg-transparent-3.png");
    background: cover;
}

.container-fluid {
    padding-top: 15px;
}

.bg {
    height: 50px;
    background-color: #1e3120;
    color: white;
}
</style>
