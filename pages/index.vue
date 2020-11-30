<template>
  <div>
  <main-header/>
  <div class="s px-10 py-100 hero-section hero-section">
    <div class="container mx-auto flex flex-row justify-center items-center">
      <div class="w-1/2 hero-text">
        <h1>Some text that should leave an impression</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, quae harum. Nisi aliquam quasi illum dignissimos vel, totam autem eos modi consectetur necessitatibus perferendis, expedita earum iusto reiciendis fugiat aperiam.</p>
      <button>Go for it!</button>
      </div>
      <div class="w-1/2 hero-image"><img src="~/assets/images/hero.png" alt=""></div>
    </div>
  </div>
  <div class="divider">
    <BottomDivider/>
  </div>
  </div>
</template>

<script>
import MainHeader from '../components/main-header.vue'
import BottomDivider from '@/assets/svg/slant-up-bottom.svg'

export default {
  components: { MainHeader, BottomDivider },}
</script>

<style lang="scss">
html {
  font-family: 'Montserrat';
}

.hero-image {
  margin-top: 20px; 
}

.hero-section {
  padding-top: 80px;
  padding-bottom: 200px;
  overflow: hidden;
  min-height: 100vh;
  background: rgb(58,62,180);
  background: linear-gradient(149deg, rgba(58,62,180,1) 0%, rgba(253,29,229,1) 94%);

  h1 {
  font-size: 50px;
  color: white;
  font-weight: 700;
  margin-bottom: 23px;
  }

  p {
    color: white;
    max-width: 80%;
    margin-bottom: 55px;
  }

  button {
     background-color: white;
    padding: 20px 40px;
    border-radius: 15px;
    font-size: 20px;
    color: rgb(58,62,180);
    font-weight: 700;
    transition: all 0.2s ease-in-out;
    box-shadow: 0px 0px 15px 2px rgb(58,62,180);

    &:hover {
      background-color:  rgba(253,29,229,1);
      color: white;
    }
  }
}

.divider {
  margin-top: -200px;
  
  svg {
    min-height: 200px;
    height: 100%;
  }
}
</style>
