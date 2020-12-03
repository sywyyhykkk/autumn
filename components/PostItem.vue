<template>
  <NuxtLink to="/">
    <div class="card-container">
      <div class="card-left">
        <p class="card-status">[{{ post.status }}]</p>
        <p class="card-title">{{ sliceTitle(post.title) }}</p>
      </div>
      <div class="card-right">
        <p class="card-author">Author: {{ post.author }}</p>
        <p class="card-comments">Comments: {{ post.comments }}</p>
      </div>
    </div>
  </NuxtLink>
</template>
<script>
export default {
  name: "PostItem",
  props: {
    post: Object,
  },

  data() {
    return {};
  },

  methods: {
    sliceTitle(title) {
      const maxLength = 20
      if (title.length < maxLength || title.length == maxLength) {
        return title;
      } else {
        return title.slice(0, maxLength) + "...";
      }
    },
  },
  mounted() {},
  computed: {},
};
</script>
<style scoped>
.card-container {
  height: 30px;
  /* border: 1px solid black; */
  box-shadow: 1px 2px 4px #dad8d8;
  display: inline-block;
  vertical-align: top;
  width: 100%;
}
.card-left {
  float: left;
}
.card-right {
  float: right;
}
.card-container p {
  display: inline-block;
  vertical-align: top;
  margin: auto;
}
.card-status {
  color: red;
  font-size: 10px;
  font-weight: bold;
  width: 40px;
}
.card-title {
  color: black;
  padding-top: 1%;
  font-size: 15px;
}
.card-author {
  font-size: 15px;
  padding-top: 2%;
  padding-right: 1%;
  /* border: 1px solid black; */
  width: 150px;
  font-size: 5px;
}
.card-comments {
  font-size: 15px;
  padding-top: 2%;
  /* border: 1px solid black; */
  width: 120px;
  font-size: 5px;
}
</style>