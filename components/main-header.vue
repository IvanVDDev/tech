<template>
  <div class="px-10 py-10 fixed header-section">
    <header class="container mx-auto flex flex-row">
        <div class="w-1/4 logo">
        SOLUTIONS
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
export default {

}
</script>

<style lang='scss'>

.header-section {
  width: 100%;

  nav {
    li {
      a {
        color: white;
      }
    }
  }

  .logo {
    font-size: 26px;
    font-weight: 700;
    color: white;
  }
}
</style>