<template>
  <div>
    <NavbarVue />
    <main>
      <div>
        <p> {{ 2 + 2 }}</p>
      </div>
    </main>
    <FooterVue />
  </div>
</template>

<script setup>
import NavbarVue from "./components/Navbar.vue";
import FooterVue from "./components/Footer.vue";
import {ref} from "vue";

 
</script>

<style scoped>
</style>