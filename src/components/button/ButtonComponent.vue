<script setup>
import { computed } from 'vue'

// eslint-disable-next-line
const props = defineProps({
    count: Number
})
// eslint-disable-next-line
const emit = defineEmits(['countUp'])

// const count = computed(() => {
//     return props.count
// })
const count = computed(() => (props.count))

const countUp = () => {
    emit('countUp')
}
</script>

<template>
    <div>
        <button @click="countUp">＋</button>
        <p>{{ count }}</p>
    </div>
</template>