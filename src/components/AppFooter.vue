<script>
export default {
    data() {
        return {
            footerList: [
                {
                    image: '../assets/img/dark-pet-logo-2x.png'
                },
                {
                    title: 'Shop by brand'
                },
                {
                    title: 'Useful links'
                },
            ]
        }
    },
}
</script>

<template lang="">
    <div>
        <footer>
            <div class="container">
                <div class="row align-items-center">
                    <div class="col text-center">
                        ciao
                    </div>
                    <div class="col text-center">
                        ciao
                    </div>
                    <div class="col text-center">
                        ciao
                    </div>
                    <div class="col text-center">
                        ciao
                    </div>

                </div>
            </div>
        </footer>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/generals.scss';

footer {
    background-color: #1e3120;
    color: white;
}

.row {
    height: 300px;
    outline: 1px solid;

}
</style>
