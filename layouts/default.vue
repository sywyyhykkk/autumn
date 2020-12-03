<template>
  <a-layout id="components-layout-demo-fixed-sider">
    <a-layout-sider
      :style="{
        overflow: 'auto',
        height: '100vh',
        position: 'fixed',
        left: 0,
        background: '#fff',
        border: '1px solid red',
      }"
    >
      <div
        class="logo"
        :style="{
          border: '1px solid red',
          textAlign: 'center',
          height: '100px',
          lineHeight: '100px',
        }"
      >
        <h1>Autumn</h1>
        <div>
          <div
            :style="{
              border: '1px solid red',
              height: '150px',
              width: '150px'
            }"

            v-for="dog in dogs" :key="dog"
          >
          
            <nav-bar-item :imageUrl="imageUrl" />
          </div>

        </div>
      </div>
      <!-- <a-menu theme="light" mode="inline" :style="{}">
        <a-menu-item key="1">
          <span class="nav-text">nav 1</span>
        </a-menu-item>
        <a-menu-item key="2">
          <span class="nav-text">nav 2</span>
        </a-menu-item>
        <a-menu-item key="3">
          <span class="nav-text">nav 3</span>
        </a-menu-item>
        <a-menu-item key="4">
          <span class="nav-text">nav 4</span>
        </a-menu-item>
        <a-menu-item key="5">
          <span class="nav-text">nav 5</span>
        </a-menu-item>
        <a-menu-item key="6">
          <span class="nav-text">nav 6</span>
        </a-menu-item>
        <a-menu-item key="7">
          <span class="nav-text">nav 7</span>
        </a-menu-item>
        <a-menu-item key="8">
          <span class="nav-text">nav 8</span>
        </a-menu-item>
      </a-menu> -->
    </a-layout-sider>

    <a-layout :style="{ marginLeft: '200px' }">
      <a-layout-header
        :style="{
          background: '#fff',
          padding: 0,
          border: '1px solid red',
          margin: '0 16px 0',
        }"
      >
        <div
          :style="{ textAlign: 'center', lineHeight: '50px', height: '50px' }"
        >
          <h1>Header</h1>
        </div>
      </a-layout-header>

      <a-layout-content :style="{ margin: '20px 16px 0', overflow: 'initial' }">
        <div
          :style="{
            padding: '24px',
            background: '#fff',
            textAlign: 'center',
            border: '1px solid red',
          }"
        >
          <Nuxt />
        </div>
      </a-layout-content>
    </a-layout>
  </a-layout>
</template>
<script>
import NavBarItem from "../components/NavBarItem.vue";

export default {
  data() {
    return {
      imageUrl: require('../assets/images/1.png'),
      dogs: [1, 2, 3]
    };
  },
  components: { NavBarItem },
};
</script>

<style>

</style>
