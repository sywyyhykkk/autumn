<template>
  <div class="container">
    <div>
      <Navbar />
    </div>
    <div>
      <Nuxt />
    </div>
  </div>
</template>

<script>
import Navbar from "~/components/Navbar";

export default {
  components: {
    Navbar,
  },
};
</script>

<style>
.container {
  width: 100%;
}
</style>
