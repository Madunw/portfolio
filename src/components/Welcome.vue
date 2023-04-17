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

      <button class="btn"  @click="sendEmail">Contact Me</button>
    </div>
    <div class="illustration">
      <img src="../assets/welcome-illustration.svg" alt="illustration" />
    </div>
  </div>
  <div class="mouse">
  <svg data-v-3699c9a0="" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="28.5px" height="43.5px" viewBox="0 0 28.5 43.5" enable-background="new 0 0 28.5 43.5" xml:space="preserve"><g data-v-3699c9a0=""><path data-v-3699c9a0="" fill="none" stroke="#4568dc" stroke-width="3" d="M14.415,41.848L14.415,41.848C7.587,41.848,2,36.261,2,29.433V14.415 C2,7.587,7.587,2,14.415,2h0c6.828,0,12.415,5.587,12.415,12.415v15.019C26.829,36.261,21.243,41.848,14.415,41.848z"></path><line data-v-3699c9a0="" id="dropdown-point" x1="14.415" y1="12.408" x2="14.415" y2="12.408" stroke="#4568dc" stroke-width="5" stroke-linecap="round"><animate data-v-3699c9a0="" id="animation1" attributeName="y2" dur="3s" values="12.408; 12.408; 12.408; 15.908; 19.408; 19.408; 23.408; 23.408; 23.408; 23.408; 23.408" repeatCount="indefinite" begin="0s" fill="freeze"></animate><animate data-v-3699c9a0="" id="animation2" attributeName="y1" dur="3s" values="12.408; 12.408; 12.408; 12.408; 12.408; 12.408; 23.408; 23.408; 23.408; 23.408; 23.408" repeatCount="indefinite" begin="0s" fill="freeze"></animate><animate data-v-3699c9a0="" id="animation3" attributeName="opacity" dur="3s" values="0; 1; 1; 1; 1; 1; 1; 1; 1; 0; 0;" repeatCount="indefinite" begin="0s" fill="freeze"></animate></line></g></svg></div>
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
  methods: {
    sendEmail() {
      window.location.href = 'mailto:you@example.com';
    },
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
  padding: 0 2rem 0 12vw;
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
.mouse {
  margin-top: 3rem;
}

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

  .mouse {
    display: none;
}
}
</style>