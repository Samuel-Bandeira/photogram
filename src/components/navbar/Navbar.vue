<template>
  <div class="navbar">
    <p class="logo">Photogram</p>
    <div class="routes">
      <router-link to="/">Home</router-link>
      <router-link to="/profile">Profile</router-link>
    </div>
  </div>
</template>
<script>
export default {
  name: "Navbar",
};
</script>
<style src="./style.css"></style>
