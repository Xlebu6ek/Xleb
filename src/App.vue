<template>
  <div id="app">
    <glebNavbar></glebNavbar>
    <!--<div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>-->

    <router-view />
    <card v-for="(post, index) in posts" :key="index" :post="post" />
  </div>
</template>

<script>
// @ is an alias to /src

import glebNavbar from "@/components/navbar.vue";
import card from "./components/card.vue";

let posts = [
  {
    authorName: "Ogurets332 ",
    postPictureUrl:
      "https://memepedia.ru/wp-content/uploads/2021/09/bro-tebe-nado-trenirovatsja-memy-pro-simpla-2.jpg",
    authoravatarUrl:
      "https://otvet.imgsmail.ru/download/288163020_424f77f301683fe539ed05352e906e3a_800.jpg",
    countlikes: 55,
    description: "огузок, тебе надо тренироваться сказал шеф огузку",
  },
  {
    authorName: "gvguyg",
    postPictureUrl:
      "https://i.pinimg.com/236x/98/be/53/98be538050252167f8a31297c7f74761.jpg?nii=t",
    authoravatarUrl:
      "https://i.pinimg.com/236x/98/be/53/98be538050252167f8a31297c7f74761.jpg?nii=t",
    countlikes: 55,
    description: "ребёнка нашли",
  },
  {
    authorName: ";guyethyukr68",
    postPictureUrl:
      "https://ds04.infourok.ru/uploads/ex/110f/0000381e-e35932dc/img17.jpg",
    authoravatarUrl:
      "https://ds04.infourok.ru/uploads/ex/110f/0000381e-e35932dc/img17.jpg",
    countlikes: 55,
    description: "морфологический разбор имени существительного ",
  },
  {
    authorName: "seeiopjropiopf",
    postPictureUrl:
      "https://img2.ntv.ru/home/news/20191127/nabozhena_io.jpg",
    authoravatarUrl:
      "https://img2.ntv.ru/home/news/20191127/nabozhena_io.jpg",
    countlikes: 55,
    description: "я не умру в туалете!",
  },
  {
    authorName: "ejobkopjiogy",
    postPictureUrl:
      "https://serebro-shop.ru/image/cache/catalog/serebro/data/big/01-010013-720x520.jpg",
    authoravatarUrl:
      "https://serebro-shop.ru/image/cache/catalog/serebro/data/big/01-010013-720x520.jpg",
    countlikes: 55,
    description: "кольцо золотое, продам, 1990 рублей, звоните: 7 983 566 37 42",
  },
];

export default {
  name: "Home",
  components: {
    glebNavbar,
    card,
  },

  data() {
    return {
      posts: posts,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
