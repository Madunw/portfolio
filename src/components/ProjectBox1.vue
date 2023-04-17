<template>
  <div class="card">
    <div class="img-card">
      <img src="@/assets/zipper-wallet.png" />
    </div>
    
    <a href="http://www.mayue.me/projects/zipper-wallet" target="_blank" class="mask">Go to site</a>

    <div class="info-card">
      <div class="text">
        <h2><strong>Zipper Wallet</strong></h2>
        <p>
          <strong>A cryptocurrency wallet Chrome extension </strong> that allows users to generate multiple cryptocurrency accounts, send and receive transactions, and view transaction history.
          <br>
          I have developed two versions of it, a web app and a Chrome extension.
        </p>
      </div>
      <div class="technologies">
        <ul>
          <li
            v-for="technologe in technologeList"
            v-bind:key="technologe.name"
            class="technology-item"
          >
            <img :src="technologe.icon" class="technology-icon" />
            {{ technologe.name }}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import vueIcon from '@/assets/icons/vue-icon.svg';
import html5Icon from '@/assets/icons/html5-icon.svg';
import cssIcon from '@/assets/icons/css-icon.svg';
import javascriptIcon from '@/assets/icons/javascript-icon.svg';
import ethersIcon from '@/assets/icons/ethers-icon.svg';
import alchemyIcon from '@/assets/icons/alchemy-icon.png';
import elementUiIcon from '@/assets/icons/element-ui-icon.svg';
import viteIcon from '@/assets/icons/vite-icon.svg';

export default {
  name: 'ProjectBox',
  data() {
    return {
      showAddToCart: false,
      technologeList: [
        { name: 'Vue', icon: vueIcon },
        { name: 'HTML', icon: html5Icon },
        { name: 'CSS', icon: cssIcon },
        { name: 'JavaScript', icon: javascriptIcon },
        { name: 'ElementUI', icon: elementUiIcon },
        { name: 'Vite', icon: viteIcon },
        { name: 'EthersJS', icon: ethersIcon },
        { name: 'Alchemy', icon: alchemyIcon },
      ],
    };
  },
};
</script>

<style scoped>
.card {
  position: relative;
  background: #fff;
  border: solid 8px #020214;
  box-shadow: -30px 30px #000000;
  transition: all 0.2s ease-in-out;
  display: flex; /* 使用 flex 属性 */
  flex-direction: column; /* 使用 flex-direction 属性 */
  justify-content: center;
  cursor: pointer;
}

img {
  width: 100%;
  height: 100%;
}

.card:hover {
  transform:  translateX(-30px) translateY(30px);
  box-shadow: 0px 0px #333333;
}
.card .img-card {
  position: relative; /* 修改为 relative */
  width: 100%; /* 修改为 100% */
  height: 100%; /* 修改为 100% */
  display: flex;
  justify-content: center;
  align-items: center;
  transition: filter 0.2s 0.1s ease-in-out;
}

.card:hover .img-card {
  filter: blur(2px);
}

.card .mask {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.1);
  text-align: center;
  line-height: 250px;
  font-weight: bold;
  font-size: 30px;
  opacity: 0;
  color: #000000;
}

.card:hover .mask {
  opacity: 1;
  transition: opacity 0.3s 0.1s ease-in-out;
}

.card .info-card {
  width: 100%; /* 修改为 100% */
  bottom: 0;
  left: 0;
  right: 0;
  border-top: solid 6px #333;
  background-color: #56b3ff;
  color: #fff;
}

.card .info-card .text {
  margin: 1rem 2rem;
}

.card .info-card p {
  font-size: .9vw;
}
.card .technologies {
  margin: .5vw; /* 添加上下边距，可根据需要调整 */
}

.card .info-card .technologies .technology-item {
  display: inline-block;
  padding: 5px 10px;
  background-color: #ffffff;
  color: #000000;
  border-radius: 50px;
  margin-right: 5px;
  height: 1.7rem;
  font-size: .9vw;
  padding: 0.3rem 0.8rem;
  margin: 5px;
  border: 1px solid #a0a0a0;
}

.card .info-card .technologies .technology-item .technology-icon {
  max-height: 100%;
  width: auto;
  vertical-align: middle;
  margin-right: 5px;
}
@media screen and (max-width: 768px) {
  .card .info-card .text {
  margin: 0 1rem;
}

  .card .info-card .technologies .technology-item {
    height: .8rem;
  }
}


</style>
