<script setup lang="ts">
import { ref, reactive } from 'vue';
defineProps<{
  msg: string
}>()

const selectboxtest = ref("1");
const count = ref(0);


const increment = () =>{    
  count.value++
}
/*
function increment() {
  count.value++
}
*/

</script>

<template>
    <div class="greetings">
        <p>test desuyo!</p>
        <p>{{selectboxtest}}</p>
        <select v-model="selectboxtest">
            <option value="1">1:aaa</option>
            <option value="2">2:bbb</option>
        </select>

        <div>count: {{count}}</div>
        <button @click="increment">クリック</button>
    </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
