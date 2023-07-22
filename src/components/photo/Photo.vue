<template>
  <div class="photo">
    <div class="header">
      <div class="user-picture">
        <img :src="imageUrl" />
      </div>
      <div>
        <p class="user-name">{{ user.name }}</p>
      </div>
    </div>
    <div class="content">
      <img :src="imageUrl" />
    </div>
    <div class="actions">
      <i
        class="like"
        :class="liked ? 'pi pi-heart-fill' : 'pi pi-heart'"
        @click="handleLikeButtonClick"
      ></i>
      <i class="comment pi pi-comment"></i>
    </div>
  </div>
</template>
<script>
export default {
  name: "Photo",
  props: {
    imageUrl: {
      type: String,
      default: "",
    },
    user: {
      type: Object,
      default: {},
    },
  },
  created() {
    this.likedOrNot();
  },
  data() {
    return {
      liked: false,
    };
  },
  methods: {
    likedOrNot() {
      //chamar api pra verificar se o user curtiu a foto ou n.
      this.liked = false;
    },
    handleLikeButtonClick() {
      this.liked = !this.liked;
    },
  },
};
</script>
<style src="./style.css" scoped></style>
