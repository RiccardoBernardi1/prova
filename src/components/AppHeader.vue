<script>
export default {
  name: "AppHeader",
  data() {
    return {
      links: [
        {
          text: "CHARACTERS",
          active: true,
        },
        {
          text: "COMICS",
          active: false,
        },
        {
          text: "MOVIES",
          active: false,
        },
        {
          text: "TV",
          active: false,
        },
        {
          text: "GAMES",
          active: false,
        },
        {
          text: "COLLECTIBLES",
          active: false,
        },
        {
          text: "VIDEOS",
          active: false,
        },
        {
          text: "FANS",
          active: false,
        },
        {
          text: "NEWS",
          active: false,
        },
        {
          text: "SHOP",
          active: false,
        },
      ],
    };
  },
  methods: {
    changeActive(index) {
      this.links.forEach((elm, i) => {
        if (index === i) {
          elm.active = true;
        } else {
          elm.active = false;
        }
      });
    },
  },
};
</script>

<template>
  <header>
    <div class="container-flex">
      <img src="../assets/dc-logo.png" alt="Logo DC" />
      <ul>
        <li
          v-for="(link, index) in links"
          :class="{ active: link.active }"
          @click="changeActive(index)"
        >
          <a href="#">{{ link.text }}</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<style scoped lang="scss">
img {
  padding: 1rem;
}
ul {
  display: flex;
  list-style: none;
  height: 8.4375rem;
  li {
    height: 100%;
    margin: 0 1.25rem;
    a {
      text-decoration: none;
      display: inline-block;
      color: inherit;
      line-height: 8.4375rem;
      font-weight: bold;
    }
    &.active {
      color: var(--primary-color);
      border-bottom: 4px solid var(--primary-color);
    }
  }
}
</style>
