<template>
  <div class="bg-black w-full flex justify-between px-6 md:px-20 py-5 relative">
      <div class="flex">
        <img src="~/assets/images/logo.png" class="mr-2 -mt-1"/>
        <p class="mt-1 text-[#616161] text-sm"> <span  class="text-white">Adens Law</span> Group</p>
      </div>
      <ul class="hidden lg:flex justify-between mt-1 w-[30%]">
        <li  class="text-white text-xs">Home</li>
        <li  class="text-[#616161] text-xs">Practice areas</li>
        <li  class="text-[#616161] text-xs">The team</li>
        <li  class="text-[#616161] text-xs">Blog</li>
      </ul>
      <ul v-if="showMenu" class="w-full flex flex-col h-screen absolute bg-black mt-12 lg:hidden">
        <li  class="text-white text-md py-6">Home</li>
        <hr class="border-[#121212]">
        <li  class="text-white text-md py-6">Practice areas</li>
        <hr class="border-[#121212]">
        <li  class="text-white text-md py-6">The team</li>
        <hr class="border-[#121212]">
        <li  class="text-white text-md py-6">Blog</li>
      </ul>
      
      <div class="hidden md:flex ">
      <button class="text-white border text-xs border-white px-4  rounded-md">Get in touch</button>
      </div>
      <div @click="toggleNav" class="flex md:hidden">
      <button  class="border text-xs bg-white border-white px-4 rounded-md">{{ showMenu ? 'Close' : 'Menu' }}</button>
    </div>
      
  </div>


</template>

<script>
  export default {
    data() {
      return {
        showMenu: false
      }
    },
    methods: {
      toggleNav() {
        this.showMenu = !this.showMenu
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>
