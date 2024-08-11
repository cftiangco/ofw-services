<template>
    <FieldContainer>
        <button class="btn-primary" @click="handleClick">{{label}}</button>
    </FieldContainer>
</template>


<script setup>
import FieldContainer from './field-container.vue'
defineProps(['label'])

const emit = defineEmits(['click'])
const handleClick = () => {
    emit('click')
}
</script>

<style lang="scss">
@import '@/assets/styles/base.scss';
.btn-primary {
    height:40px;
    background-color: $primary-color;
    color: $primary-light-color;
    font-size: 18px;
    font-weight: bold;
    outline: none;
    border: none;
    cursor: pointer;
    border-radius: 2px;
}
</style>