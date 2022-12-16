<script setup>
import ButtonComponent from '@/components/button/ButtonComponent.vue';
import { ref, watch } from 'vue'

const count = ref(0)
const countUp = () => {
    count.value += 1
}

watch(count, () => {
    console.log('count up')
})
</script>

<template>
    <div>This is ChildComponent!</div>
    <ButtonComponent 
        :count="count"
        @countUp="countUp"
    />
</template>
