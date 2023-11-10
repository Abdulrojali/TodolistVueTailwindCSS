<script>
export default {
    props:['IdData','listData'],
    methods:{
        deleteData:function(){
            this.listData.splice(this.IdData,1)
        }
    }
}
</script>


<template>
    <button @click='deleteData' class="bg-red-600 inline-block w-36 h-8 text-sm  text-white rounded-sm px-3 py-1">Delete</button>
</template>