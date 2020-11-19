<template>
  <div class="container">
    <section class="mt-4 font-secondary h1">
      <span class="text-secondary">Design.</span>
      <span class="text-primary">Dogs.</span>
      <span class="text-primary">Hiking.</span>
      <span class="text-secondary">Coding.</span>
      <span class="text-primary">Cocktails.</span>
    </section>
    <section>
      <h4 class="mt-3">
        Hello! My name is <span class="text-secondary">Robert Gumeny.</span>
      </h4>
      <h4 class="mt-2">
        I am a <span class="text-secondary">Boise, ID</span> based web designer
        and developer specializing in creating websites that are
        <span class="text-secondary">engaging, responsive,</span> and
        <span class="text-secondary">user-friendly.</span>
      </h4>
    </section>
    <section class="mt-2">
      <nuxt-link to="/portfolio" class="mt-3 mr-1 btn btn-primary"
        >See My Work</nuxt-link
      >
      <nuxt-link to="/contact" class="mt-3 btn btn-secondary"
        >Get In Touch</nuxt-link
      >
    </section>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss"></style>
