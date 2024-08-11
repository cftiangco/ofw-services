<template>
    <FieldContainer>
        <label for="username">{{ label }}</label>
        <input 
            :type="type" 
            :id="id" 
            class="text-box"
            @input="handleInput"
            :value="modelValue"
        />
    </FieldContainer>
</template>

<script setup>
import FieldContainer from './field-container.vue';
defineProps([
    'label',
    'type',
    'id',
    'modelValue'
]);

const emit = defineEmits(['update:modelValue'])

const handleInput = (event) => {
    emit('update:modelValue', event.target.value);
}

</script>

<style lang="scss">

.text-box {
    outline: none;
    height: 30px;
    width: 300px;
    border:1px solid #ddd;
    border-radius: 2px;
    padding:5px 15px
}

.mb-10 {
    margin-bottom: 10px;
}
</style>