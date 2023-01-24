<script>
export default {

}
</script>

<template lang="">
<div class="container-fluid">
    <div class="row text-center">
        <div class="col-3 text-center d-flex align-items-center justify-content-center">
            <img src="../assets/img/logo-symbol.png" alt="" class="logo">
            <h1 class="m-3">
                <b>
                Avada Pet Supplies
                </b>
            </h1>
                
        </div>
        <div class="col-3 text-center d-flex align-items-center justify-content-center">
            <form name="search">
                <input type="text" class="input" placeholder="inserisci link">
            </form>
        </div>
        <div class="col-4 text-center d-flex align-items-center justify-content-center">
           <b class="m-2">Questions?</b> Call us : 1.800.123.4567
            
        </div>
        <div class="col-2 text-center d-flex align-items-center justify-content-center">
            <i class="fa-regular fa-user m-2"></i>
            <i class="fa-solid fa-bag-shopping"></i>
        </div>
    </div>
</div>
</template>

<style lang="scss" scoped>
@use '../style/generals.scss';

h1 {
    font-size: 20px;
}

input {
    width: 200px;
}

.logo {
    height: 50px;
    width: 50px;
}

.fa-regular,
b {
    cursor: pointer;
}
</style>
