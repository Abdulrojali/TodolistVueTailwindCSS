<script>
import buttonAdd from '../component/buttonAdd.vue'
import buttonDelete from '../component/delete.vue'

export default{
    data() {
        return {
            todoInput:'',
            data:['makan','tidur','belajar'], 
        }
    },
    components:{
        buttonAdd,
        buttonDelete,
    },
}
</script>

<template>
    <div class="w-full h-screen p-3 flex justify-center items-center">
        <div class="w-3/4 content flex flex-col gap-2">
            <div class="col w-full flex gap-2">
                <input type="text" class="w-full  py-2 rounded-sm border-4 px-2" v-model="todoInput" placeholder="input">
                <buttonAdd :inputData="todoInput" :listData="data"></buttonAdd>
            </div>
            <div class="col output flex flex-col gap-5 mt-20">
                <h3 class="pb-3 text-3xl font-black text-black capitalize text-center">list jadwal</h3>
               <div class="w-full flex justify-around items-center"  
               v-for="(output,index) in data" 
               :key="index">
                <p class="text-2xl font-black text-black capitalize">
                {{output}}
            </p>
            <buttonDelete :IdData="index" :listData="data"></buttonDelete>
               </div> 
            </div>
        </div>
    </div>
</template>