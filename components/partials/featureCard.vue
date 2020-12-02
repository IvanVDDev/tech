<template>
  <div class="w-1/3">
          <div class="feature-card flex flex-col items-center rounded-lg shadow-lg  mx-8">
              <div>
                <img :src="getImgUrl(feature.image)" alt="">
              </div>
              <div class="py-10 px-10">
                <h3 class="mb-10 mt-6">{{feature.title}}</h3>
                <p>{{feature.description}}</p>
              </div>
          </div>
      </div>
</template>

<script>
export default {
    props: [
        'featureInfo'
    ],

    data() {
        return {
            feature : this.featureInfo
        }
    },

    methods: {
        getImgUrl: (pic) => {
            return require('@/assets/images/'+pic)
        }
    }
}
</script>

<style>

</style>