<template>
  <div>
  <main-header/>
  <div class="px-10 py-100 hero-section">
    <div class="container mx-auto flex flex-row justify-center items-center">
      <div class="w-1/2 hero-text">
        <h1>Some text that should leave an impression</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, quae harum. Nisi aliquam quasi illum dignissimos vel, totam autem eos modi consectetur necessitatibus perferendis, expedita earum iusto reiciendis fugiat aperiam.</p>
      <button>Explore!</button>
      </div>
      <div class="w-1/2 hero-image"><img src="~/assets/images/hero.png" alt=""></div>
    </div>
  </div>
  <div class="divider">
    <BottomDivider/>
  </div>
  <div class="feature-section px-10 py-10">
    <div class="container ml-8">
      <h2 class="mb-4">Services we do best</h2>
      <p class="mb-16">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptatum, reprehenderit?</p>
    </div>
    <div class="container mx-auto flex flex-row justify-center items-center">
      <feature-card v-for="(feature, index) in features" :key="index" :featureInfo="feature"/>
    </div>
  <div class="bottom-divider">
    <BottomDivider/>
  </div>
  </div>

  <div class="benefits-section px-10 py-20">
    <h2 class="mb-24">Benefits we provide</h2>
    <div class="container mx-auto flex flex-row justify-center items-center">
      <div class="w-1/4 ml-6 mr-3 benefits-card bg-white px-10 py-16 rounded-xl shadow-2xl">
        <Wheel class="mb-6"/>
        <h3 class="mb-4">Security</h3>
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nesciunt, earum!</p>
      </div>
      <div class="w-1/4 mx-3 benefits-card bg-white px-10 py-16 rounded-xl shadow-2xl">
        <Wheel class="mb-6"/>
        <h3 class="mb-4">Security</h3>
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nesciunt, earum!</p>
      </div>
      <div class="w-1/4 mx-3 benefits-card bg-white px-10 py-16 rounded-xl shadow-2xl">
        <Wheel class="mb-6"/>
        <h3 class="mb-4">Security</h3>
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nesciunt, earum!</p>
      </div>
      <div class="w-1/4 mr-6 ml-3 benefits-card bg-white px-10 py-16 rounded-xl shadow-2xl">
        <Wheel class="mb-6"/>
        <h3 class="mb-4">Security</h3>
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nesciunt, earum!</p>
      </div>
    </div>
  </div>
  <div class="container slider-container mx-auto py-20">
    <h2 class="mb-2">They have spoken</h2>
    <p class="text-center">Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit, aliquam!</p>
   <VueSlickCarousel :settings="carouselSettings">
      <div class="slide-item shadow-2xl">
        <div class="testemonial flex ">
          <div class="image">
            <img src="https://placeimg.com/640/640/people?t=1607017330993" alt="">
          </div>
          <div class="info py-20 px-10">
            <p class="mb-10">"Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nam eum officia voluptatem recusandae totam officiis ab cupiditate! Illum, obcaecati dolor. Dignissimos sit quis totam assumenda aperiam, unde aspernatur quaerat ut."</p>
            <h4 class="mb-1">John Doe</h4>
            <b>CEO Fiction DevOps</b>
          </div>
        </div>
      </div>
      <div class="slide-item shadow-2xl">
         <div class="testemonial flex ">
          <div class="image">
            <img src="https://placeimg.com/640/640/people?t=1607017330993" alt="">
          </div>
          <div class="info py-20 px-10">
            <p class="mb-10">"Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nam eum officia voluptatem recusandae totam officiis ab cupiditate! Illum, obcaecati dolor. Dignissimos sit quis totam assumenda aperiam, unde aspernatur quaerat ut."</p>
            <h4 class="mb-1">John Doe</h4>
            <b>CEO Fiction DevOps</b>
          </div>
        </div>
      </div>
      <div class="slide-item shadow-2xl">
         <div class="testemonial flex ">
          <div class="image">
            <img src="https://placeimg.com/640/640/people?t=1607017330993" alt="">
          </div>
          <div class="info py-20 px-10">
            <p class="mb-10">"Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nam eum officia voluptatem recusandae totam officiis ab cupiditate! Illum, obcaecati dolor. Dignissimos sit quis totam assumenda aperiam, unde aspernatur quaerat ut."</p>
            <h4 class="mb-1">John Doe</h4>
            <b>CEO Fiction DevOps</b>
          </div>
        </div>
      </div>
      <div class="slide-item shadow-2xl">
         <div class="testemonial flex ">
          <div class="image">
            <img src="https://placeimg.com/640/640/people?t=1607017330993" alt="">
          </div>
          <div class="info py-20 px-10">
            <p class="mb-10">"Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nam eum officia voluptatem recusandae totam officiis ab cupiditate! Illum, obcaecati dolor. Dignissimos sit quis totam assumenda aperiam, unde aspernatur quaerat ut."</p>
            <h4 class="mb-1">John Doe</h4>
            <b>CEO Fiction DevOps</b>
          </div>
        </div>
      </div>
    </VueSlickCarousel>
  </div>
</div>
</template>

<script>
import MainHeader from '../components/main-header'
import BottomDivider from '@/assets/svg/slant-up-bottom.svg'
import Wheel from '@/assets/svg/wheel.svg'
import FeatureCard from '../components/partials/featureCard'
import FeatureData from '../data/features'
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
// optional style for arrows & dots
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'

export default {
  components: { 
    MainHeader, 
    BottomDivider, 
    FeatureCard,
    Wheel,
    VueSlickCarousel
  },

  data() {
    return {
      features: FeatureData,
      carouselSettings: {
        "dots": true,
        "dotsClass": "slick-dots custom-dot-class",
        "edgeFriction": 0.35,
        "infinite": false,
        "speed": 500,
        "slidesToShow": 1,
        "slidesToScroll": 1
      }
    }
  }
}
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
    fill: transparent;
    z-index: 3;
  }
}

.feature-section {
  position: relative;
  padding-bottom: 200px;

  h2 {
    font-size: 50px;
    font-weight: bold;
    color: rgb(58,62,180);
  }

  p {
    color: black;
  }

  .feature-card {
    img {
      height: 250px;
      width: 100%;
      object-fit: cover;
    }

    h3 {
      font-size: 30px;
      font-weight: 700;
      color: rgb(58,62,180);
      text-align: center;
    }

    p {
      text-align: center;
    }
  }

  .bottom-divider {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 200px;
    min-width: 200px;
    transform: rotate(180deg);
    background: rgba(58,62,180,0.1);
    z-index: -1;
    
  }
}

 .benefits-section {
    background: linear-gradient(149deg, rgba(253,29,229,1) 0%, rgba(58,62,180,1) 94%);

  h2 {
    font-size: 50px;
    font-weight: 700;
    color: white;
  }
  
  .benefits-card {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;

    svg {
      width: 120px;
      height: 120px;
      padding: 20px;
      border-radius: 50%;
      background: rgba(58,62,180,0.1);
    }

    h3 {
      font-size: 30px;
      font-weight: 700;
      color: rgb(58,62,180);
    }

    p {
      text-align: center;
     }
    }
  }

  .slider-container {
    position: relative;

    &::before {
      content: '';
      position: absolute;
      display: block;
      width: 7.5%;
      height: 100%;
      top: 0;
      left: 0;
      background: linear-gradient(to right, white 20%, rgba(255,255,255,0.5) 70%,  transparent 100%);
      z-index: 1;
    }

     &::after {
      content: '';
      position: absolute;
      display: block;
      width: 7.5%;
      height: 100%;
      top: 0;
      right: 0;
      background: linear-gradient(to left, white 20%, rgba(255,255,255,0.5) 70%,  transparent 100%);
    }

    h2 {
      font-size: 50px;
      font-weight: 700;
      color: rgb(58,62,180);
      text-align: center;
    }

    .slide-item {
      height: 300px;
      margin: 100px 10%;
      width: 80% !important;
      border-radius: 20px;
      overflow: hidden;
      outline: none;

      &::before, &::after {
        content: none;
        border-color: transparent;
      }

      .testemonial {
        height: 100%;
        
        .image {
          width: 300px;
          height: 100%;
          display: flex;
          align-items: center;
          justify-content: center;

          img {
            width: 200;
            height: 200px;
            border-radius: 50%;
          }
        }

        .info {
          width: calc(100% - 300px);
          height: 100%;

          p {
            font-style: italic;
          }

          h4 {
            color: rgb(58,62,180);
            font-weight: 700;
            font-size: 19px;
          }
        }
      }
    }
  }
</style>
