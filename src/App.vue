<script>
import todoComponent from './view/todolist.vue'
export default {
  data() {
    return {
    }
  },
  components:{
        todoComponent
      }
}
</script>

<template>
  <div class='w-full h-screen flex flex-col justify-center items-center p-2 border-4 py-10'>
    <h3 class="text-5xl font-black capitalize text-black font-mono"> todolist <span class="text-red-600">sederhana</span></h3>
    <todoComponent></todoComponent>
  </div>
</template>