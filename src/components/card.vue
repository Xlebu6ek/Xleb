<template>
  <div class="wrap">
    <div class="container">
      <div
        id="square"
        :style="{
          background: 'url(' + post.authoravatarUrl + ')',
          'background-size': 'cover',
        }"
      ></div>
      <div>{{ post.authorName }}</div>
    </div>
    <img :src="post.postPictureUrl" width="1000px" />
    <img src="super.kot.svg" style="fill: black" >
    <img src="imba.svg" style="fill: black" >
    <div>{{post.description}}</div>
  </div>
</template>

<script>
import Vue from "vue";

export default Vue.extend({
  props: ["post"],
});
</script>

<style>
#square {
  width: 100px;
  height: 100px;
  border-radius: 100px;
  margin-bottom: 10px;
  margin-right: 10px;
}
.container {
  display: flex;
  align-items: center;
  font-size: 26px;
}

.wrap {
  width: 1000px;
  margin: 0 auto;
  margin-bottom: 25px;
  
}
.super.kot.svg {
  margin-bottom: 100px;
}


.post.description {
  margin-left: 100px;
}
</style>
