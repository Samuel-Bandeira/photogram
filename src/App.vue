<template>
  <div>
    <Photo :user="user" :imageUrl="imageUrl" />
  </div>
</template>
<script>
import Photo from "./components/Photo.vue";

export default {
  components: { Photo },
  data() {
    return {
      user: {
        id: 1,
        name: "Samuel_Oliveira",
      },
      imageUrl: "https://shorturl.at/iAT04",
    };
  },
};
</script>
