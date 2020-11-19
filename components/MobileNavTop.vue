<template>
  <div class="mobile-nav-top">
    <span class="logo text-accent font-primary">RG</span>
  </div>
</template>

<script>
export default {
  name: "mobile-nav-top",
  data() {
    return {};
  },
  computed: {},
  methods: {},
  components: {}
};
</script>

<style lang="scss" scoped>
.mobile-nav-top {
  margin-top: 1.85rem;
  padding: 0 1.1rem;
}
.logo {
  padding: 6px;
  font-size: 2rem;
  font-weight: bold;
  border: 2.25px solid $accent-dark;
  border-radius: 15px;
}
</style>
