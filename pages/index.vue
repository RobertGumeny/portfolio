<template>
  <div class="container">
    <section class="mt-4 font-secondary h2">
      <span class="text-animated text-secondary"></span>
      <span class="cursor h2">_</span>
    </section>
    <section>
      <h4 class="mt-3">
        Hello! My name is
        <span class="text-secondary bold">Robert Gumeny.</span>
      </h4>
      <h4 class="mt-2">
        I am a <span class="text-secondary bold">Boise, ID</span> based web
        designer and developer specializing in creating websites that are
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
import { gsap } from "gsap";
import { TextPlugin } from "gsap/TextPlugin";
import { CSSRulePlugin } from "gsap/CSSRulePlugin";
export default {
  data() {
    return {};
  },
  mounted() {
    gsap.registerPlugin(TextPlugin);
    gsap.registerPlugin(CSSRulePlugin);
    const words = [
      "Web Designer.",
      "Software Developer.",
      "Avid Hiker.",
      "Wine Enthusiast."
    ];
    let cursor = gsap.to(".cursor", {
      opacity: 0,
      duration: 1,
      ease: "power2.inOut",
      repeat: -1
    });

    let mainTL = gsap.timeline({ repeat: -1 });
    words.forEach(word => {
      let tl = gsap.timeline({
        repeat: 1,
        delay: 1,
        yoyo: true,
        repeatDelay: 1
      });
      tl.to(".text-animated", { duration: 2, text: word });
      mainTL.add(tl);
    });
  }
};
</script>

<style lang="scss" scoped>
.cursor {
  display: inline-block;
}
</style>
