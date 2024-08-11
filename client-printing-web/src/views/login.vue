<template>
    <div class="container">
       <div class="login-container">
           <div class="form-container">
                <TextBox 
                    label="Username"
                    type="text"
                    id="username"
                    v-model="usernameModel"
                />
                <TextBox 
                    label="Password"
                    type="password"
                    id="password"
                    v-model="passwordModel"
                />
                <PrimaryButton 
                    label="Login"
                    @click="handleClick"
                />
           </div>
       </div>
    </div>
</template>

<script setup>

    import { ref } from 'vue'

    import TextBox from '@/components/common/text-box.vue'
    import PrimaryButton from '@/components/common/primary-button.vue'
    
    const usernameModel = ref('')
    const passwordModel = ref('')

    const handleClick = () => {
        console.log(`clicked`,usernameModel.value,passwordModel.value);
    }
</script>

<style lang="scss">
@import '@/assets/styles/base.scss';

.container {
    height: 100vh;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: $primary-color;
}
.login-container {
    height: 300px;
    width: 400px;
    background-color: $primary-light-color;
    border-radius: 3px;
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>