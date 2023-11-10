<script>
export default {
    props:['inputData','listData'],
    methods:{
        addItems:function(){
            if(this.inputData===''){
                alert('tolong masukkan inputan!')
            }
            else{
                this.listData.push(this.inputData)
            }    
        }
    }
}
</script>

<template>
    <button @click="addItems" class="px-5 py-1 rounded-sm bg-orange-500 text-white capitalize">add</button>
</template>