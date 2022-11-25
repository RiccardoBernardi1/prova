<script>
export default {
  name: "AppBtn",
  props: {
    text: String,
  },
};
</script>

<template>
  <div class="btn">
    {{ text }}
  </div>
</template>

<style lang="scss" scoped>
.btn {
  padding: 1rem 1.875rem;
  min-width: 9.375rem;
  background-color: var(--primary-color);
  color: white;
}
</style>
