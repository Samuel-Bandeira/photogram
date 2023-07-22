<template>
  <div>
    <div class="profile-container">
      <div class="user-picture">
        <img :src="user.img" />
      </div>
      <p class="user-name">{{ user.name }}</p>
    </div>
    <UploadFile />
  </div>
</template>

<script>
import UploadFile from "../../components/uploadFile/UploadFile.vue";

export default {
  name: "Profile",
  components: { UploadFile },
  data() {
    return {
      user: {},
    };
  },
  created() {
    this.getUser();
  },
  methods: {
    getUser() {
      this.user = {
        id: 1,
        name: "Samuel_Oliveira",
        img: "https://shorturl.at/iAT04",
      };
    },
  },
};
</script>
<style src="./style.css"></style>
