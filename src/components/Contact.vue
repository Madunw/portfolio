<template>
  <h1>Contact Me</h1>
  <a href="https://github.com" target="_blank" rel="noopener noreferrer">
    <img src="@/assets/icons/mail-icon.svg"><span>mayue2022@gmail.com</span>
</a>
  <a href="https://github.com" target="_blank" rel="noopener noreferrer">
      <span>Github</span>
  </a>
  <a href="https://github.com" target="_blank" rel="noopener noreferrer">
    <span>LinkedIn</span>
</a>

  <Welcome />
</template>

<script>
export default {
  name: 'Contact',
};
</script>

<style scoped>
a {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 5px;
  background: #FFD401;
  box-shadow: 0px 6px 24px 0px rgba(0, 0, 0, 0.2);
  overflow: hidden;
  border: none;
  margin: 1rem 0;
}

a:after {
  content: " ";
  width: 0%;
  height: 100%;
  
  background: #61ccff;
  position: absolute;
  transition: all 0.4s ease-in-out;
  right: 0;
}

a:hover::after {
  right: auto;
  left: 0;
  width: 100%;
}

a span {
  text-align: center;
  text-decoration: none;
  width: 100%;
  padding: 18px 25px;
  color: #fff;
  font-size: 1.125em;
  font-weight: 700;
  letter-spacing: 0.3em;
  z-index: 20;
  transition: all 0.3s ease-in-out;
}

a:hover span {
  color: #183153;
  animation: scaleUp 0.3s ease-in-out;
}

a img {
  width: 3rem;
  margin-top: 1rem;
  margin-bottom: 2rem;
}
@keyframes scaleUp {
  0% {
    transform: scale(1);
  }

  50% {
    transform: scale(0.95);
  }

  100% {
    transform: scale(1);
  }
}
</style>
