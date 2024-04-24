<template>
    <form @submit="submitForm" class="form">
    <input type="text" v-model="name" placeholder="Type your fuc name"/>
    <input type="email" v-model="email" placeholder="Type your fuc email"/>
    <input type="password" v-model="password" placeholder="Type your fuc password"/>
    <button @submit.prevent="submitForm">Sign ME up</button>
    </form>
</template>

<script>
    export default {
        data(){
            return{
                gender: '',
                name: '',
                email: '',
                password: '',
            }
        },
        methods:{
            submitForm(){
                console.log("Form data has been submitted");
            }
        }
    }
</script>

<style>
    .form{
        display: grid;
        flex-direction: column;
        gap: 20px;
        margin: 50px 0;
    }
    input{
        border-radius: 12px;
        padding: 10px 10px;
        border: none;
        outline: none;
        background: #4d4d4d8b;
        color: WHITE;
        font-size: 17px;
    }
    
    button{
        border-radius: 12px;
        margin: 20px 0;
        padding: 10px;
        outline: none;
        border: none;
        font-size: 17px;
        font-weight: 600;
        background: #41B883;
        color: rgb(0, 0, 0);
    }
</style>
