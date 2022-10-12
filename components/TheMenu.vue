<template>
  <div class="flex">
    <button @click="openMenu" class="absolute z-10 sm:hidden">
      <img
        :src="require(`@/assets/icons/${menuIcon}.png`)"
        class="hover:cursor-pointer"
      />
    </button>
    <nav
      :class="isOpen ? 'block' : 'hidden'"
      class="fixed flex flex-col h-screen w-8/12 pt-16 bg-smoke/30 sm:bg-transparent sm:h-20 sm:static sm:flex-row sm:justify-around sm:items-center sm:w-screen"
    >
      <ul class="w-full flex flex-col justify-around sm:flex-row">
        <a class="hidden sm:block" href=""
          ><img src="@/assets/icons/halloween-party.png"
        /></a>
        <NuxtLink
          :to="item.to"
          v-for="(item, index) in menu"
          :key="index"
          class="link-items capitalize h-16 bg-emphasis my-2 flex items-center justify-center sm:items-end sm:bg-transparent sm:h-max"
          >{{ item.title }}</NuxtLink
        >
      </ul>
    </nav>
  </div>
</template>
<script>
export default {
  name: "Menu",
  computed: {},
  data() {
    return {
      menu: [
        { title: "home", to: "/" },
        { title: "events", to: "/##" },
        { title: "nightlife", to: "/###" },
        { title: "contact", to: "/####" },
      ],
      menuIcon: "open-menu",
      isOpen: false,
    };
  },
  methods: {
    openMenu() {
      this.isOpen = !this.isOpen;
      if (this.isOpen) {
        this.menuIcon = "close-menu";
      } else {
        this.menuIcon = "open-menu";
      }
      console.log("abrir menu");
    },
  },
};
</script>
<style>
@media screen and (min-width: 640px) {
  nav {
    display: flex !important;
  }
  ul {
    align-items: center;
  }
}
</style>
