<template>
  <div class="icon">
    <img :src="imageUrl" alt="bear"/>
  
  </div>
</template>
<script>

export default {
  name: "NavBarItem",
  props: {
    imageUrl: String,
  },

  data() {
    return {
    }
  },

  methods: {},
  mounted() {
    
  },
  computed:{
     
  }
};
</script>
<style scoped>
.icon img {
  height: 120px;
  width: 120px;
}
</style>