<template>
  <h1>About Me</h1>
  <div id="aboutme">
    <div id="introduction">
      <p>
        My name is <strong>MA YUE</strong>, and I graduated from Toyo
        University in 2022 with a degree in Information Sciences. <br>
        Throughout my academic and personal pursuits, I have acquired a diverse
        set of skills in <strong>web development</strong>,
        <strong>blockchain</strong>, and other related areas.<br> As someone
        passionate about the emerging field of Web3, I am now actively <strong>seeking
        job opportunities</strong> where I can apply my skills and knowledge to make a
        meaningful contribution to the industry. I am excited to take on new
        challenges.
      </p>
    </div>


    <div id="my-skills">
      <h2 style="margin: 2rem">My Skills</h2>
      <div id="skills">
        <ul>
          <li
            v-for="skill in skillList"
            v-bind:key="skill.name"
            class="skill-item"
          >
            <img :src="skill.icon" class="skill-icon" />
            {{ skill.name }} 
          </li>
          etc.
        </ul>
      </div>
    </div>
  </div>

  <Welcome />
</template>

<script>
  import vueIcon from '@/assets/icons/vue-icon.svg';
import html5Icon from '@/assets/icons/html5-icon.svg';
import cssIcon from '@/assets/icons/css-icon.svg';
import javascriptIcon from '@/assets/icons/javascript-icon.svg';
import solidityIcon from '@/assets/icons/solidity-icon.svg';
import openzeppelinIcon from '@/assets/icons/openzeppelin-icon.svg';
import ethersIcon from '@/assets/icons/ethers-icon.svg';
import pythonIcon from '@/assets/icons/python-icon.svg';
import apacheIcon from '@/assets/icons/apache-icon.svg';
import npmIcon from '@/assets/icons/npm-icon.svg';
import gitIcon from '@/assets/icons/git-icon.svg';
import seleniumIcon from '@/assets/icons/selenium-icon.svg';
import viteIcon from '@/assets/icons/vite-icon.svg';
import remixIcon from '@/assets/icons/remix-icon.png';
import hardhatIcon from '@/assets/icons/hardhat-icon.svg';
import pytorchIcon from '@/assets/icons/pytorch-icon.svg';
import typescriptIcon from '@/assets/icons/typescript-icon.svg';

export default {
  name: 'AboutMe',
  data() {
    return {
      skillList: [
        { name: 'HTML', icon: html5Icon },
        { name: 'CSS', icon: cssIcon },
        { name: 'JavaScript', icon: javascriptIcon },
        { name: 'TypeScript', icon: typescriptIcon },
        { name: 'Vue', icon: vueIcon },
        { name: 'Vite', icon: viteIcon },
        { name: 'Python', icon: pythonIcon},
        { name: 'Selenium', icon: seleniumIcon},
        { name: 'PyTorch', icon: pytorchIcon},
        { name: 'Solidity', icon: solidityIcon },
        { name: 'OpenZeppelin', icon: openzeppelinIcon },
        { name: 'EthersJS', icon: ethersIcon },
        { name: 'Remix', icon: remixIcon },
        { name: 'Hardhat', icon: hardhatIcon },
        { name: 'Apache', icon: apacheIcon },
        { name: 'Npm', icon: npmIcon },
        { name: 'Git', icon: gitIcon },
        
        

      ],
    };
  },
};
</script>

<style scoped>
#aboutme {
  display: flex;
  align-items: center;
  padding: 5vm;
}

#introduction {
  margin: 5rem 3rem;
  width: 40%;
  color: #171a4b;
}
#introduction p {
  font-size: 1.1rem;
  line-height: 1.7rem;
}
#my-skills {
  margin: auto 3rem;
  width: 40%;
  font-size: 1.6rem;
}
#skills {
  display: flex;
  flex-wrap: wrap;
  align-items: flex-start;
}
.skill {
  padding: 1rem 2rem;
  background: rgba(153, 153, 153, 0.2);
  border-radius: 5px;
  color: #666;
}


.skill-item {
  display: inline-block;
  background-color: #ffffff;
  color: #000000;
  border-radius: 50px;
  margin-right: 6px;
  height: 1.8vw;
  padding: 0.3rem 1.2rem;
  margin: .5vw;
  border: 1px solid #474747;
  font-size: .8rem;
}

.skill-icon {
  max-height: 100%;
  width: auto;
  vertical-align: middle;
}



.email-link {
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 5px;
  background: #56b3ff;
  box-shadow: 0px 6px 24px 0px rgba(0, 0, 0, 0.2);
  overflow: hidden;
  border: none;
  margin: 1rem 0;
  text-decoration:none;
  position: relative;
}

.email-link:after {
  content: " ";
  width: 0%;
  height: 100%;
  background: #ffdc2b;
  
  position: absolute;
  transition: all 0.4s ease-in-out;
  right: 0;
}

.email-link:hover::after {
  right: auto;
  left: 0;
  width: 100%;
}

.email-link span {
  text-align: center;
  text-decoration: none;
  width: 100%;
  padding: 18px 25px;
  color: #fff;
  font-size: 2em;
  font-weight: 700;
  z-index: 20;
  transition: all 0.3s ease-in-out;
}

.email-link:hover span {
  color: #152941;
  animation: scaleUp 0.3s ease-in-out;
}





@media (orientation: portrait) {
  #introduction {
  margin: 0;
}
  #introduction {
  width: 100%;
}

#my-skills {
  width: 100%;
  margin: 0;
}
.skill-item {
  height: 1.2rem;
  font-size: 1rem;
}
}
</style>
