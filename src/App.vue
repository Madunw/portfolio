<template>

  <div class="sidebar" :style="sidebarStyle">
    <a
      v-for="(section, index) in sections"
      :key="index"
      :href="'#' + section.id"
      :style="{ backgroundColor: getBackgroundColor(index) }"
      @click.prevent="scrollToSection(section.id)"
      >{{ section.id }}</a
    >
  </div>

  <section id="welcome">
    <Welcome />
  </section>

  <section id="projects">
    <Projects />
  </section>

  <section id="aboutme">
    <AboutMe />
  </section>

  <section id="contact">
    <Contact />
  </section>

</template>

<script>
import Welcome from './components/Welcome.vue';
import Projects from './components/Projects.vue';
import AboutMe from './components/AboutMe.vue';

import Contact from './components/Contact.vue';

export default {
  name: 'App',
  data() {
    return {
      sections: [],
      sidebarStyle: {},
    };
  },
  components: {
    Welcome,
    Projects,
    AboutMe,

    Contact,
  },

  mounted() {
    // 获取所有的section元素
    this.sections = document.querySelectorAll('section');
    // 监听滚动事件，根据滚动距离设置侧边栏的位置
    window.addEventListener('scroll', () => {
      if (window.scrollY > 100) {
        this.sidebarStyle = { right: '20px' };
      } else {
        this.sidebarStyle = { right: '-400px' };
      }
    });
  },
  methods: {
    getBackgroundColor(index) {
      // 新增方法，根据索引返回不同的背景颜色
      const colors = ['#ff6c52', '#f3d218', '#29ffa2', '#61ccff'];
      // 修改处，如果索引超出颜色数组范围，返回默认颜色
      return colors[index] || '#ffffff';
    },
    scrollToSection(id) {
      // 点击侧边栏链接时滚动到目标section的中间位置
      const targetSection = document.getElementById(id);
      const targetOffsetTop = targetSection.offsetTop;
      const targetHeight = targetSection.offsetHeight;
      const windowHeight = window.innerHeight;
      const scrollTo = targetOffsetTop - windowHeight / 2 + targetHeight / 2;
      window.scrollTo({
        top: scrollTo,
        behavior: 'smooth',
      });
    },
  },
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
}
#app {
  height: 100%;
  width: 100%;
  color: #13172e;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  scroll-behavior: smooth;
  box-sizing: border-box;
}

section {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

section h1 {
  font-size: 3em;
  margin-bottom: 2em;
}

section p {
  font-size: 1.5rem;
}
#welcome {
  background-color: #fafcff;
  padding: 0 2rem 0 8rem;
}
#projects {
  background-color: #32425a;
  color: #e6e6e6;
}
#aboutme {
  background-color: #ffffff;
}
#contact {
  background-color: #32425a;
  color: #e6e6e6;
}

.sidebar {
  position: fixed;
  top: 50%;
  right: -400px;
  transform: translateY(-50%);
  display: flex;
  flex-direction: column;
  text-transform: uppercase;
  transition: right 0.3s ease-in-out;
}

.sidebar a {
  margin-bottom: 10px;
  padding: 10px;
  color: #030111;
  text-decoration: none;
  color: #ffffff;
  font-weight: bold;
}

.sidebar a:hover {
  transform: scale(1.1);
}

section {
  padding: 10rem;
}


@media screen and (orientation: portrait) {
  #aboutme {
    flex-direction: column;
  }
}
</style>
