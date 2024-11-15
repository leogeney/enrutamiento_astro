<script setup>

    import {ref} from 'vue'
    let qty = ref(0);

    function add (){

      qty.value++;
      console.log(qty);

      

      

    }

    function menos (){

qty.value--;
console.log(qty);



}


</script>

<template >
<div class="font-sans max-w-80 mx-auto rounded-md bg-purple-700 p-6 flex flex-col items-center shadow-xl">
    <div 
    v-if="qty > 0 "    
    class="bg-red-500 text-white rounded-full size-8 flex justify-center items-center font-bold":class="{'bg-green-500 text-yellow-400':qty > 10 }">
        {{qty}}


        
    </div>
    <div v-else>
            nadie te visita
        </div>
    <br>
<div @click="add"  
 class="bg-green-600 hover:bg-green-800 text-white p-6 max-w-30 rounded-md border-2 border-white flex justify-center items-center cursor-pointer">

    MAS
</div>
<br>
<div @click="menos"  
 class="bg-yellow-600  hover:bg-yellow-400 text-blue-600 font-mono p-6 max-w-30 rounded-md border-2 border-red-500 flex justify-center items-center cursor-pointer">

    menos
</div>

</div>
</template>