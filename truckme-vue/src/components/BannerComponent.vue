<template>
  <div class="banner">
    <img class="banner-image" :src="bannerImage" alt="Banner Image" />
    <h1 class="banner-title">Seja bem-vindo</h1>
  </div>
</template>

<script>
export default {
  name: "BannerComponent",
  data() {
    return {
      bannerImage: require("@/assets/images/banner.jpeg"),
    };
  },
};
</script>

<style scoped>
.banner {
  position: relative;
  width: 100%;
  max-width: 100%;
  overflow: hidden;
  text-align: center;
}

.banner-image {
  width: 100%;
  height: auto;
  display: block;
}

.banner-title {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: black;
  font-size: 4rem;
  opacity: 0;
  animation: fadeInUp 1.5s ease forwards;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translate(-50%, -60%);
  }
  to {
    opacity: 1;
    transform: translate(-50%, -50%);
  }
}
</style>
