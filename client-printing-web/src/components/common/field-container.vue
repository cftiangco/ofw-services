<template>
     <div class="field-container">
        <slot></slot>
     </div>
</template>

<style lang="scss">
    .field-container {
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        gap: 2px;
        margin-bottom: 10px;
    }
</style>