<template>
<h1>{{question}}</h1>
    <button type="button" :class="{ active: modelValue === 'poor' }" @click="updateModelValue('poor')">Poor</button>
    <button type="button" :class="{ active: modelValue === 'average' }" @click="updateModelValue('average')">Average</button>
    <button type="button" :class="{ active: modelValue === 'great' }" @click="updateModelValue('great')">Great</button>
</template>

<script>
export default {
    props: ['modelValue', 'question'],
    emits: ['update:modelValue'],
    methods: {
        updateModelValue(option){
            this.$emit('update:modelValue', option)
        }
    }
}
</script>

<style scoped>
.active {
  border-color: green;
}
.active button {
  color: greenyellow;
}
</style>