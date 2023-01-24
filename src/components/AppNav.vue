<script>
export default {
    data() {
        return {
            menu: [
                {
                    label: 'Home',
                    url: '#',
                    active: false
                },
                {
                    label: 'Shop',
                    url: '#',
                    active: true
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
                    active: false
                },
            ]
        }
    },
    methods: {
        setActive: function (index) {
            this.menu.forEach((item, i) => {
                item.active = i === index;
            });
        }
    }
}
</script>


<template lang="">
  <header>
     <nav>
      <ul>
        <li v-for="(item, index) in menu" :key="index" :class="item.active ? 'active' : ''" @click="setActive(index)">
              <a :href="item.url" class="link">
              {{item.label}}
              </a>
          </li>
      </ul>
     </nav>
  </header>
</template>


<style scoped lang="scss">
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
