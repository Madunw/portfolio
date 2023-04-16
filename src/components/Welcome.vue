<template id="welcome">
  <div id="welcome">
    <div class="main">
      <h1 class="title">Hi</h1>
      <h1 class="title">I'm MAYUE</h1>
      <p>
        I am a Frontend Developer based in Tokyo. I'm actively seeking new
        employment opportunities, specifically within the Web3 field.
      </p>
      <div class="icons">
        <GithubIcon />
      </div>

      <button class="btn">Contact Me</button>
    </div>
    <div class="illustration">
      <img src="../assets/welcome-illustration.svg" alt="illustration" />
    </div>
  </div>
</template>

<script>
import GithubIcon from '@/components/GithubIcon.vue';
export default {
  name: 'Welcome',
  data() {
    return {};
  },
  components: {
    GithubIcon,
  },
};
</script>

<style scoped>
#welcome {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  color: rgb(13, 34, 51);
  padding: 0 2rem 0 8rem;
}

.main {
  flex: 1;
  width: 100%;
}
.main p{
  font-size: 1vw;
}
.illustration {
  flex: 0 0 50%;
  text-align: center;
}

.illustration img {
  width: 100%;
}

.title {
  font-size: 5vw; /* 使用vw单位，根据视窗宽度改变字体大小 */
  font-weight: 700;
  margin-left: 1rem;
  margin-bottom: 0;
}

.icons {
  display: flex;
  margin: 1rem 0;
}

.btn {
  padding: 1.1em 2em;
  background: none;
  border: 2px solid #fff;
  font-size: 1rem;
  color: #131313;
  cursor: pointer;
  position: relative;
  overflow: hidden;
  transition: all 0.3s;
  border-radius: 12px;
  background-color: #fde03d;
  font-weight: bolder;
  box-shadow: 0 2px 0 2px rgb(13, 34, 51);
}

.btn:before {
  content: '';
  position: absolute;
  width: 100px;
  height: 120%;
  background-color: #eb6942;
  top: 50%;
  transform: skewX(30deg) translate(-150%, -50%);
  transition: all 0.5s;
}

.btn:hover {
  background-color: #43c6ee;
  color: #fff;
  box-shadow: 0 2px 0 2px #0d3b66;
}

.btn:hover::before {
  transform: skewX(30deg) translate(150%, -50%);
  transition-delay: 0.1s;
}

.btn:active {
  transform: scale(0.9);
}

/* 响应式布局：移动端隐藏 illustration */
@media (max-width: 768px) {
  .illustration {
    display: none;
  }
  #welcome {
    padding: 0 2rem;
  }
  .icons a{
   margin: auto;
  }
.main {
    padding: auto;
    text-align: center;
  }

  h1 {
    font-size: 4rem;
    margin-top: 2rem;
  }

  p {
    margin-top: 1rem;
    font-size: 0.8rem;
  }

  .icons {
    margin-top: 1rem;
  }
}
</style>