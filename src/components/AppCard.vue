<script>
export default {
  name: "AppCard",
  props: {
    img: String,
    title: String,
  },
};
</script>

<template>
  <div class="card">
    <img :src="img" :alt="title" />
    <h4>{{ title }}</h4>
  </div>
</template>

<style lang="scss" scoped>
.card {
  padding: 0.5rem;
  text-align: center;
  img {
    max-width: 100%;
    margin: 0 0 1rem;
    max-height: 11.25rem;
    width: 11.25rem;
    object-fit: cover;
    object-position: top;
  }
  h4 {
    min-height: 2.25rem;
  }
}
</style>
