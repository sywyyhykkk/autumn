<template>
  <div class="container">
    <div v-for="(post, i) in posts" :key="i">
      <post-item :post="post" />
    </div>
  </div>
</template>

<script>
import PostItem from "../components/PostItem.vue";
export default {
  components: { PostItem },
  data() {
    return {
      posts: [
        {
          status: "Top",
          title: "那是真的牛逼啊啊",
          author: "喜羊羊与灰太狼",
          comments: 10213,
        },
        {
          status: "New",
          title: "那是真的牛逼啊那是真的牛逼啊那是真的牛逼啊那是真的牛逼啊那是真的牛逼啊",
          author: "喜羊羊与灰太狼",
          comments: 1113,
        },
        {
          status: "Hot",
          title: "那是真的牛逼啊啊啊啊啊那是真的牛逼啊啊啊啊啊那是真的牛逼啊啊啊啊啊那是真的牛逼啊啊啊啊啊那是真的牛逼啊啊啊啊啊",
          author: "喜羊羊与灰太狼",
          comments: 9875,
        },
      ],
    };
  },
  methods: {},
};
</script>

<style>
.container {
  height: 200px;
  padding: 24px;
  background: #fff;
  /* border: 1px solid red; */
}
</style>
