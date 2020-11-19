<template>
  <div class="container">
    <h1 class="h2 mt-4 page-title">My Work</h1>
    <ul>
      <li v-for="project of projects" :key="project.slug" class="my-2 card">
        <img
          :src="require(`~/assets/images/${project.img}`)"
          :alt="project.alt"
        />
        <h3 class="title">{{ project.title }}</h3>
        <p class="h6 p-1 description my-2">{{ project.description }}</p>
        <ul class="skills-list">
          <li v-for="skill in project.skills" :key="skill">
            <span class="mr-1">{{ skill }}</span>
          </li>
        </ul>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const projects = await $content("projects", params.slug).fetch();

    return {
      projects
    };
  },
  data() {
    return {};
  }
};
</script>

<style lang="scss" scoped>
li {
  list-style: none;
  position: relative;
}

img {
  width: 100%;
  border-radius: 3px;
  filter: brightness(50%);
}

.skills-list {
  display: flex;
  flex-direction: row;
}

.skills-list li span {
  background: $bg-dark;
  color: $secondary;
  padding: 1px 5px;
  border-radius: 5px;
}

li:nth-child(odd) {
  .title {
    position: absolute;
    top: 7.5%;
    right: 7.5%;
  }

  .description {
    text-align: right;
  }

  .skills-list {
    position: absolute;
    right: 3%;
    bottom: 5%;
  }
}

li:nth-child(even) {
  .title {
    position: absolute;
    top: 7.5%;
    left: 7.5%;
  }
  .description {
    text-align: left;
  }
  .skills-list {
    position: absolute;
    left: 6.5%;
    bottom: 5%;
  }
}
</style>
