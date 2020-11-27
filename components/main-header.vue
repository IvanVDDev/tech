<template>
  <div class="w-screen px-10 py-10 bg-purple-900">
    <header class="container mx-auto flex flex-row">
        <div class="w-1/4 logo">
          <SVGLogo/>
        </div>
        <!-- ... -->
        <nav class="w-3/4"> 
          <ul  class="flex flex-row justify-end">
            <li class="px-10"><a href="#">Home</a></li>
            <li class="px-10"><a href="#">Home</a></li>
            <li class="px-10"><a href="#">Home</a></li>
            <li class="pl-10"><a href="#">Home</a></li>
          </ul>
        </nav>
    </header>
  </div>
</template>

<script>
import SVGLogo from '@/assets/svg/flame.svg';
export default {
components: {
    SVGLogo,
  }
}
</script>

<style lang='scss'>

</style>