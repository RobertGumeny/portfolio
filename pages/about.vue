<template>
  <div class="container">
    <h1 class="h2 mt-3 text-secondary page-title">About Me</h1>
    <p>
      I enjoy designing and creating websites for the modern web that look and
      perform great across all devices and browsers.
    </p>
    <p>
      Some of my favorite things about being a developer include the diverse
      range of tools available to solve problems and the ability to constantly
      iterate over and improve upon your projects and skills.
    </p>
    <p>
      In my spare time I enjoy spending time with my fiancée and our dog,
      Maximus. We love hiking in the Boise Foothills and escaping into the
      mountains to unplug and enjoy the raw, natural beauty that Idaho and the
      greater Northwest have to offer.
    </p>
    <p>
      I am currently working with and learning the following tools, languages,
      and technologies:
    </p>
    <section class="mt-1 tools">
      <ul>
        <li>JavaScript</li>
        <li>HTML/CSS</li>
        <li>PHP</li>
        <li>C#</li>
        <li>SQL</li>
      </ul>
      <ul>
        <li>Node.js</li>
        <li>Vue/Nuxt</li>
        <li>Bootstrap</li>
        <li>MongoDB</li>
        <li>Adobe XD</li>
      </ul>
    </section>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
p {
  margin-top: 1.25rem;
  font-size: 1.1rem;
}
.tools {
  display: grid;
  grid-template-columns: auto auto;
  justify-items: center;
}

ul {
  list-style: none;
  font-size: 1.1rem;
}

ul li::before {
  content: "\2022";
  color: $accent-dark;
  font-weight: bold;
  display: inline-block;
  width: 1em;
  margin-left: -1em;
}
</style>
