<template>
  <div class="contact-container">
    <h1>Contact Me</h1>
    <img src="@/assets/icons/mail-icon.svg" class="mail-icon">
    <button class="email-link"  @click="sendEmail"><span>job@mayue.me</span></button>
  </div>
</template>
<script>
export default {
  name: 'Contact',
  methods: {
    sendEmail() {
      window.location.href = "mailto:job@mayue.me";
    }
  }
};
</script>
<style scoped>
.contact-container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

h1 {
  font-size: 2rem;
  margin-top: 1rem;
  margin-bottom: 1rem;
}

.mail-icon {
  width: 5rem;
  margin-top: 1rem;
  margin-bottom: 2rem;
  filter: brightness(0) invert(1);
}

.email-link {
  cursor: pointer;
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

@media screen and (max-width: 768px) {
  h1 {
    font-size: 2rem;
    margin-top: 0.5rem;
    margin-bottom: 0.5rem;
  }
  
  .mail-icon {
    width: 3rem;
    margin-top: 0.5rem;
    margin-bottom: 1rem;
  }
  
  .email-link {
    margin: 0.5rem 0;
  }
  
  .email-link span {
    padding: 12px 20px;
    font-size: 1.5rem;
  }
}
</style>