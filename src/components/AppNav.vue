<script>
export default {
    data() {
        return {
            menu: [
                {
                    label: 'Home',
                    url: '#',
                    active: false,
                    dropdown: [
                        { label: 'home-alternate', url: '#' },
                    ]
                },
                {
                    label: 'Shop',
                    url: '#',
                    active: false,
                    dropdown: [
                        { label: 'shop', url: '#' },
                        { label: 'Shop', url: '#' },
                        { label: 'Shop', url: '#' },
                        { label: 'Shop', url: '#' },
                        { label: 'Shop', url: '#' },

                    ]
                },
                {
                    label: 'About',
                    url: '#',
                    active: false
                },
                {
                    label: 'Blog',
                    url: '#',
                    active: false
                },
                {
                    label: 'Contact',
                    url: '#',
                    active: false
                },
                {
                    label: 'Shop by brand',
                    url: '#',
                    active: false,
                    dropdown: [
                        { label: 'Submenu 1', url: '#' },
                        { label: 'Submenu 2', url: '#' },
                        { label: 'Submenu 3', url: '#' },
                    ]
                },
            ]
        }
    },
    methods: {
        setActive: function (index) {
            this.menu.forEach((item, i) => {
                item.active = i === index;
            });
        },
        handleScroll() {
            this.scroll = window.scrollY;
        },
        mounted() {
            window.addEventListener("scroll", this.handleScroll);
        },
        beforeUnmount() {
            window.removeEventListener('scroll', this.handleScroll);
        }
    }

}
</script>


<template lang="">
  <header  :class="(this.scroll > 70 && this.scroll < 400) ? 'fixed' : ''">
    <nav>
      <!-- <ul>
        <li v-for="(item, index) in menu" :key="index" :class="item.active ? 'active' : ''" @click="setActive(index)">
          <a :href="item.url" class="link">{{item.label}}</a>
          <div v-if="item.dropdown" class="dropdown">
            <a v-for="drop in item.dropdown" :key="drop.label" :href="drop.url">{{drop.label}}</a>
          </div>
        </li>
      </ul> -->
        <div class="dropdown_">
            <div class="dropbtn" v-for="(item, index) in menu" :key="index" :class="item.active ? 'active' : ''" @click="setActive(index)">
                <a :href="item.url" class="link">{{item.label}}</a>
            </div>
            
            <!-- <div class="dropdown_content">
                <a v-for="drop in item.dropdown" :key="drop.label" :href="drop.url">{{drop.label}}</a>
            </div> -->
        </div>
    </nav>
  </header>
</template>


<style scoped lang="scss">
a {
    text-decoration: none;
    color: rgb(120, 118, 118);
    transition: 0.2s;
}

a:hover {
    color: black;
}

.dropbtn {
    background-color: white;
    color: white;
    padding: 16px;
    font-size: 16px;
    border: none;
}

.dropdown_ {
    position: relative;
    display: flex;
    justify-content: center;
}

.dropdown_content {
    display: none;
    position: absolute;
    background-color: #f1f1f1;
    min-width: 160px;
    box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
    z-index: 1;
}

.dropdown_content a {
    color: black;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
}

.dropdown_content a:hover {
    background-color: #ddd;
}

.dropdown:hover .dropdown_content {
    display: block;
}

.dropdown_:hover .dropbtn {
    background-color: white;
}

// .dropdown_ {
//     display: none;
//     position: absolute;
//     background-color: #f9f9f9;
//     min-width: 160px;
//     box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
// }

// li:hover .dropdown_ {
//     display: block;
// }

header {
    height: 50px;
    background-color: #fff;
    width: 100%;
    text-align: center;
}

s nav {
    width: 70%;
    text-align: center;
    font-size: 15px;

}

.logo {
    height: 70px;
}

ul {
    list-style: none;
}

li.active {
    border-bottom-color: #1e3120;
}

li {
    display: inline;

    a:link {
        text-decoration: none;
    }

    padding: 15px;
    border-bottom: 5px solid transparent;

    &:hover {
        border-bottom-color: #1e3120;
    }
}
</style>
