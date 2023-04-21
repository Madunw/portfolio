<template>
  <h1>Projects</h1>
  <div class="project-boxes">
    <div class="project">
    <ProjectBox />
  </div>
  <div class="project">
    <ProjectBox1 />
  </div>
  </div>
</template>

<script>
  import ProjectBox from './ProjectBox.vue';
  import ProjectBox1 from './ProjectBox1.vue';
export default {
  name: 'Projects',
  data() {
    return {
    };
  },
  components: {
  ProjectBox,
  ProjectBox1,
}
}

</script>

<style scoped>
  .project-boxes {
    display: flex;
    justify-content: space-around;
    width: 100%;
    flex-wrap: wrap;
  }
  .project {
    width: 30rem;
    margin: 2rem;

}
@media (orientation:portrait) {
  .project {
    width: 40rem;
    margin-left: 3rem;
}
}

  </style>
  