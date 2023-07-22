<template>
  <div>
    <div class="photos">
      <div v-for="(image, index) in imagesToRender" :key="index">
        <Photo :user="user" :imageUrl="image.imageUrl" />
      </div>
    </div>
  </div>
</template>
<script>
import Photo from "../components/photo/Photo.vue";
import Navbar from "../components/navbar/Navbar.vue";

export default {
  name: "Home",
  components: { Photo, Navbar },
  data() {
    return {
      user: {
        id: 1,
        name: "Samuel_Oliveira",
      },
      imagesToRender: [
        {
          imageUrl: "https://shorturl.at/iAT04",
        },
        {
          imageUrl: "https://shorturl.at/iAT04",
        },
        {
          imageUrl: "https://shorturl.at/iAT04",
        },
      ],
    };
  },
};
</script>
