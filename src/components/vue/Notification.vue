<script setup>
import { ref } from 'vue'

let qty = ref(1)

function add() {
    console.log("auch")
    qty.value++
    console.log(qty)

}
function rest() {


    qty.value--
    console.log(qty)



}


</script>

<template>
    <div class="bg-purple-300 rounded-lg max-w-80 mx-auto p-6 flex items-center justify-center gap-6">

        <div 
        v-if="qty > 0"
         class="bg-red-500 text-white size-8 rounded-full flex items-center justify-center font-bold" :class="{'bg-orange-500': qty > 3}">
            {{ qty }}
        </div>
        <p v-else>
            Nadie te la chupa
        </p>
        <div @click="add" class="bg-blue-400 text-white rounded size-6 flex justify-center items-center">
            +
        </div>


        <div @click="rest"f="qty > 0"
            class="bg-blue-400 text-white rounded size-6 flex justify-center items-center">
            -
        </div>
    </div>
</template>