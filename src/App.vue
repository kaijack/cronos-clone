<template>
  <div>
    <navbar />
    <router-view />
    <bawah />
  </div>
</template>

<script>
import navbar from "@/components/Navbar.vue";
import bawah from "@/components/Bawah.vue";
export default {
  components: {
    navbar,
    bawah
  }
};
</script>
