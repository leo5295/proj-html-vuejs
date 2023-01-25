<script>
export default {
    data() {
        return {
            footerList: [
                {
                    title: 'Shop by brand',
                    list: ['bed', 'food', 'transport', 'toys']

                },
                {
                    title: 'Useful links',
                    list: ['bed', 'food', 'transport', 'toys']
                },
            ],
            socials: [
                {
                    facebook: ''
                }
            ],
            links: [
                { name: 'Home', url: '/' },
                { name: 'About', url: '/about' },
                { name: 'Contact', url: '/contact' },
                { name: 'Privacy Policy', url: '/privacy-policy' },
            ],
            currentYear: new Date().getFullYear(),
            companyName: 'Avada',

            socials: [
                { name: 'Facebook', icon: 'fa-facebook-f' },
                { name: 'Twitter', icon: 'fa-twitter' },
                { name: 'Instagram', icon: 'fa-instagram' },
                { name: 'Youtube', icon: 'fa-youtube' },
            ]
        }
    }
}

</script>

<template lang="">
    <div>
        <footer>
            <div class="container-fluid white">
                <div class="row align-items-center">
                    <div class="col">
                        <div>
                            <img src="../assets/img/dark-pet-logo-2x.png" alt="" class="w-50">
                            <p>
                                1234 Avada Avenue Avadaville
                                info@your-company.com
                                Call us: (1) 234 5678
                            </p>
                        </div>
                    </div>
                    <div class="col">
                    <h3>{{ footerList[0].title }}</h3>
                    <ul>
                        <li v-for="listItem in footerList[0].list" :key="listItem">{{ listItem }}</li>
                    </ul>
                    </div>
                    <div class="col">
                    <h3>{{ footerList[1].title }}</h3>
                    <ul>
                        <li v-for="listItem in footerList[1].list" :key="listItem">{{ listItem }}</li>
                    </ul>
                    </div>
                    <div class="col">
                        <div class="square">
                            ciao
                        </div>
                    </div>
                </div>
            </div>
            <div class="container-fluid d-flex justify-content-center text-white m-4">
                <div v-for="link in links" :key="link.name" class="m-4">
                    <a :href="link.url" class="m-6">{{ link.name }}</a>
                </div>
            </div>
            <div class="d-flex justify-content-center socials">
                <div v-for="social in socials" :key="social.name" class="m-3">
                    <i :class="'fa-brands ' + social.icon"></i>
                </div>
            </div>
        </footer>
        <p class="text-center copyright p-4">Copyright © {{ currentYear }} {{ companyName }}</p>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/generals.scss';

footer {
    padding: 0;
}

li {
    list-style: none;
}

ul {
    padding: 0;
}

.square {
    height: 100px;
    width: 100px;
    background-color: red;
}

.white {
    color: #fff;
}

.copyright {
    background-color: black;
    color: white;
    margin-bottom: 0;
}

footer {
    background-color: #1e3120;
    padding: 1em;
}

footer a {
    text-decoration: none;
    margin-right: 0.5em;
    color: white;
}

.row {
    height: 200px;


}

.socials {
    color: #fff;
    font-size: 20px;
    height: 100px;
}
</style>
