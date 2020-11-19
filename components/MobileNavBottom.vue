<template>
  <div class="navbar-bottom">
    <ul>
      <li>
        <nuxt-link to="/">
          <i class="fas fa-home fa-2x"></i><span>Home</span>
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/portfolio">
          <i class="fas fa-laptop-code fa-2x"></i><span>Portfolio</span>
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/blog">
          <i class="fas fa-rss-square fa-2x"></i><span>Blog</span>
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/about">
          <i class="fas fa-user-alt fa-2x"></i><span>About</span>
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/contact">
          <i class="fas fa-envelope fa-2x"></i><span>Contact</span>
        </nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "mobile-nav-bottom",
  data() {
    return {};
  },
  computed: {},
  methods: {},
  components: {}
};
</script>

<style lang="scss" scoped>
ul {
  list-style: none;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}

li {
  border: 1px solid $border-dark;
  padding: 10px;
  width: 20%;
}

li a {
  text-decoration: none;
  margin-top: 5px;
  color: $primary;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.navbar-bottom {
  background-color: $bg-dark;
  overflow: hidden;
  bottom: 0;
  position: fixed;
  width: 100%;
}

.nuxt-link-exact-active {
  color: $accent-dark;
}
</style>
