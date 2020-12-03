<template>
  <a-layout>
    <a-layout-sider
      :style="{
        overflow: 'auto',
        height: '100vh',
        background: '#fff',
      }"
    >
      <div>
        <img
          :style="{ width: '200px', height: '100px' }"
          src="../assets/images/logo.png"
        />
      </div>
      <a-menu theme="light" mode="inline" v-model="selectedKeys">
        <a-menu-item :key="menus[0].key">
          <NuxtLink :to="menus[0].link">
            <a-icon type="home" />
            <span>{{ menus[0].name }}</span>
          </NuxtLink>
        </a-menu-item>

        <a-menu-item :key="menus[1].key">
          <NuxtLink :to="menus[1].link">
            <a-icon type="heart" />
            <span>{{ menus[1].name }}</span>
          </NuxtLink>
        </a-menu-item>

        <a-menu-item :key="menus[2].key">
          <NuxtLink :to="menus[2].link">
            <a-icon type="menu" />
            <span>{{ menus[2].name }}</span>
          </NuxtLink>
        </a-menu-item>

        <a-menu-item :key="menus[3].key">
          <NuxtLink :to="menus[3].link">
            <a-icon type="setting" />
            <span>{{ menus[3].name }}</span>
          </NuxtLink>
        </a-menu-item>
      </a-menu>
    </a-layout-sider>

    <a-layout :style="{ height: '100vh' }">
      <a-layout-header
        :style="{
          background: '#fff',
          margin: '0 16px 0',
          padding: '0px',
        }"
      >
        <div class="header">
          <NuxtLink :to="topMenus[0].link" style="width: 100px">
            <a-button class="header-item" type="link">
              <a-icon type="user" /> {{ topMenus[0].name }}
            </a-button>
          </NuxtLink>
          <NuxtLink :to="topMenus[1].link" style="width: 100px">
            <a-button class="header-item" type="link">
              <a-icon type="message" /> {{ topMenus[1].name }}
            </a-button>
          </NuxtLink>
          <NuxtLink :to="topMenus[2].link" style="width: 100px">
            <a-button class="header-item" type="link">
              <a-icon type="search" /> {{ topMenus[2].name }}
            </a-button>
          </NuxtLink>
          <NuxtLink :to="topMenus[3].link" style="width: 100px">
            <a-button class="header-item" type="link">
              <a-icon type="plus" /> {{ topMenus[3].name }}
            </a-button>
          </NuxtLink>
        </div>
      </a-layout-header>

      <a-layout-content :style="{ margin: '20px 16px 0', height: '100vh' }">
        <Nuxt />
      </a-layout-content>

      <a-layout-footer :style="{ textAlign: 'center' }">
        Copyright © 2020 Autumn
      </a-layout-footer>
    </a-layout>
  </a-layout>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      imageUrl: require("../assets/images/1.png"),
      menus: [
        {
          key: "1",
          name: "Home",
          link: "/",
        },
        {
          key: "2",
          name: "Favourite",
          link: "/favourite",
        },
        {
          key: "3",
          name: "Your Posts",
          link: "/",
        },
        {
          key: "4",
          name: "Setting",
          link: "/setting",
        },
      ],
      topMenus: [
        {
          name: "User",
          link: "/login",
        },
        {
          name: "Message ",
          link: "/message",
        },
        {
          name: "Search",
          link: "/search",
        },
        {
          name: "New Post",
          link: "/",
        },
      ],
      selectedKeys: ["1"],
    };
  },
  methods: {},
};
</script>

<style>
.header {
  display: inline-block;
  vertical-align: top;
  /* border: 1px red solid;  */
  margin-right: 10px;
}
.header-item {
  padding: 10px;
  width: 100px;
}
</style>

