<template>
  <h1>Projects</h1>
  <div class="project-boxes">
    <div class="project">
      <ProjectBox :project="nutrak"></ProjectBox>
    </div>
    <div class="project">
      <ProjectBox :project="zipperWallet"></ProjectBox>
    </div>
  </div>
</template>

<script>
import ProjectBox from './ProjectBox.vue';
import nutrakrImg from '@/assets/nutrakr.png';
import zipperWalletImg from '@/assets/zipper-wallet.png';

import vueIcon from '@/assets/icons/vue-icon.svg';
import html5Icon from '@/assets/icons/html5-icon.svg';
import cssIcon from '@/assets/icons/css-icon.svg';
import javascriptIcon from '@/assets/icons/javascript-icon.svg';
import solidityIcon from '@/assets/icons/solidity-icon.svg';
import openzeppelinIcon from '@/assets/icons/openzeppelin-icon.svg';
import ethersIcon from '@/assets/icons/ethers-icon.svg';
import alchemyIcon from '@/assets/icons/alchemy-icon.png';
import elementUiIcon from '@/assets/icons/element-ui-icon.svg';
import viteIcon from '@/assets/icons/vite-icon.svg';
import axiosIcon from '@/assets/icons/axios-icon.png';
import echartsIcon from '@/assets/icons/echarts-icon.png';

export default {
  name: 'Projects',
  data() {
    return {
      nutrak: {
        url: 'http://www.nutrakr.com',
        img: nutrakrImg,
        title: 'Nutrakr',
        summary: 'A blockchain health management app',
        text1:
          'to assist users in achieving nutrition and weight management goals. Features include daily nutrient requirement calculation, food nutrient content analysis, and weight management challenges.',
        text2:
          'I have issued a cryptocurrency a crypto token(SoulBound) reward system to incentivize successful challengers. with a crypto token reward system.',
        technologeList: [
          { name: 'Vue', icon: vueIcon },
          { name: 'HTML', icon: html5Icon },
          { name: 'CSS', icon: cssIcon },
          { name: 'JavaScript', icon: javascriptIcon },
          { name: 'ElementUI', icon: elementUiIcon },
          { name: 'Echarts', icon: echartsIcon },
          { name: 'Solidity', icon: solidityIcon },
          { name: 'OpenZeppelin', icon: openzeppelinIcon },
          { name: 'EthersJS', icon: ethersIcon },
        ],
      },
      zipperWallet: {
        url: 'https://madunw.github.io/zipper-wallet/',
        img: zipperWalletImg,
        title: 'Zipper Wallet',
        summary: 'A cryptocurrency wallet Chrome extension',
        text1:
          ' that allows users to generate multiple cryptocurrency accounts, send and receive transactions, and view transaction history.',
        text2:
          'I have developed two versions of it, a web app and a Chrome extension.',
          technologeList: [
        { name: 'Vue', icon: vueIcon },
        { name: 'HTML', icon: html5Icon },
        { name: 'CSS', icon: cssIcon },
        { name: 'JavaScript', icon: javascriptIcon },
        { name: 'ElementUI', icon: elementUiIcon },
        { name: 'Vite', icon: viteIcon },
        { name: 'EthersJS', icon: ethersIcon },
        { name: 'Axios', icon: axiosIcon },
        { name: 'Alchemy', icon: alchemyIcon },
      ],
      },
    };
  },
  components: {
    ProjectBox,
  },
};
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
@media (orientation: portrait) {
  .project {
    width: 40rem;
    margin-left: 3rem;
  }
}
</style>
