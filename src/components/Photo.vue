<template>
  <div class="photo">
    <div class="header">
      <div class="user-picture">
        <img :src="imageUrl" />
      </div>
      <div>
        <p>{{ user.name }}</p>
      </div>
    </div>
    <div class="content">
      <img :src="imageUrl" />
    </div>
  </div>
</template>
<script>
export default {
  name: "Photo",
  props: {
    user: {
      type: Object,
      default: {},
    },
    imageUrl: {
      type: String,
      default: "",
    },
  },
};
</script>
<style src="./style.css"></style>
