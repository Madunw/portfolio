<template>
  <a href="https://github.com/Madunw" target="_blank" rel="noopener noreferrer">
	<div id="github" class="social-btn flex-center">
			<img src="@/assets/icons/github-icon.svg"/>
      <span>github.com/Madunw</span>
		</div>
  </a>
</template>

<script>
export default {
  name: 'GithubIcon',
};
</script>

<style scoped>
img {
  height: 3rem;
  width: 3rem;
}
.social-links,.flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

.social-btn {
  cursor: pointer;
  height: 3rem;
  width: 3rem;
  font-family: 'Titillium Web', sans-serif;
  color: #333;
  border-radius: 10px;
  background: white;
  margin: 5px;
  transition: 0.3s;
  justify-content: center;
}

.social-btn svg {
  height: 24px;
  width: 24px;
}

.social-btn span {
  width: 0px;
  overflow: hidden;
  transition: 0.3s;
  text-align: center;
  margin-left: 5px;
  font-weight: bold;
}

.social-btn:hover {
  width: 15rem;
  border-radius: 5px;
}

.social-btn:hover span {
  padding: 2px;
  width: 16rem;
}

#twitter svg {
  fill: #1da1f2;
}

#linkedin svg {
  fill: #0e76a8;
}

#github {
  fill: #333;
}

</style>
