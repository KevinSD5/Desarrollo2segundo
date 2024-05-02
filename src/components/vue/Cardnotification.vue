<script setup>
import { ref } from 'vue'

const counter = ref(0)

function decrement() {
    if (counter.value>0) {
        counter.value--    
    }
    
    
}
function increment() {
    counter.value++
}
</script>

<template>
    <div class="flex-col bg-slate-200 rounded py-8 px-6 w-96 shadow-md flex items-center">
		<div class=" relative ">
			<img class="size-32 rounded-full" src="https://pbs.twimg.com/profile_images/1600219064869298177/lhnutETN_400x400.jpg" alt="">
			<div v-show="counter > 0" class=" absolute top-0 right-0 size-7 rounded-full bg-red-950 text-white flex justify-center items-center p">
				{{ counter }}
			</div>
                
		</div>
                <p v-if="counter > 0">New mensagge 😜</p>
                <p v-else="">Nadie te habla 😢</p>

		<div class=" flex justify-around w-24 mt-6">
			<button @click=" decrement" class="bg-blue-200 rounded px2 w-6 flex justify-center items-center">
				-
			</button >
			{{ counter  }}
			<button @click="increment" class="bg-blue-200 rounded px2 w-6 flex justify-center items-center">
				+
			</button>
		</div>
	</div>
</template>
