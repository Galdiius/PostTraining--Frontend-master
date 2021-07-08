<template>
    <v-container class="main-container">
        <v-card class="main-card">
            <h1>Register</h1>
            <div class="input">
                <label for="">Nama : </label><input v-model="nama" placeholder="Username"/><br>
                <label for="">Username : </label><input v-model="username" placeholder="Username"/>
                <label for="">Password : </label><input placeholder="Password" v-model="password"/>
            </div>
            <v-btn gray v-on:click="register()">Register</v-btn>
        </v-card>
    </v-container>
</template>
<script>
export default {
    data(){
        return {
            username : '',
            password : '',
            nama : ''
        }
    },
    methods : {
        register(){
            console.log('ok');
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
label{
    margin-top: 50px;
}
</style>