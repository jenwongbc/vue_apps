<template>
  <div>
    <h1>Welcome {{ user }}</h1>

    <router-link
      :to="{
        name: 'invoices'
      }"
    >
    </router-link>
    <button @click="logOut" class="btn">Log out</button>
  </div>
</template>
<script>
import store from "@/store.js";
export default {
  data() {
    return {
      user: store.user
    };
  },
  methods: {
    logOut() {
      store.user = null;
      this.$router.push("/");
    }
  }
};
</script>
