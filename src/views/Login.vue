<template>
    <v-container class="main-container">
        <v-card class="main-card">
            <div class="input">
                <label for="">Username : </label><input v-model="username" placeholder="Username"/>
                <label for="">Password : </label><input placeholder="Password" v-model="password"/>
            </div>
            <v-btn gray v-on:click="login()">Login</v-btn>
        </v-card>
    </v-container>
</template>

<script>
    import axios from 'axios'
    // const BASE_URL = 'https://bnitechshipservices.azurewebsites.net'
    const BASE_URL = 'https://bnitechship1-gateway.azurewebsites.net'
    export default {
        name: 'Login',
        data(){
            return{
                username: '',
                password : ''
            }
        },
        methods:{
            async login(){
                await axios.post(BASE_URL+'/auth/Users/Authentication',{"username" : this.username,"password" : this.password})
                .then(function(r){
                    console.log(r);
                })
                .catch(function(e){
                    console.log(e);
                })
            }
        }
    }
</script>

<style scoped>
.main-container{
    position: absolute;
    max-width: 400px;
    left: 50%;
    top: 50%;
    -webkit-transform: translate(-50%, -50%);
    transform: translate(-50%, -50%);
}
.main-card{
    padding: 20px;
}
</style>