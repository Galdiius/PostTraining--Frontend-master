<template>
    <v-container id="main-container" fluid>
        <h1 class="text-center mb-5">Enrollment</h1>
        <v-row align="center" justify="center">
            <v-card id="main-card" class="text-center ma-5">
                <div class="ma-5">
                    <label for="">Kelas&emsp; : </label>
                    <input type="text" placeholder="  Masukkan Kelas">
                </div>
                <div class="ma-5">
                    <label for="">Student : </label>
                    <input type="text" placeholder="  Masukkan Kelas">
                </div>
                <div class="ma-5">
                    <label for="">Course&ensp;: </label>
                    <input type="text" placeholder="  Masukkan Kelas">
                </div>
                <v-btn
                    elevation="2"
                    @click="enroll(student,course)"
                >Submit</v-btn>
            </v-card>
        </v-row>
    </v-container>
</template>

<script>
export default {
    data() {
        return {
            testt: 'astaga'
        }
    },
    methods:{
        enroll() {

        }
    }
}
</script>

<style lang="scss" scoped>
#main-container{
    margin-top: 50px;
}
input{
    border: 1px solid black;
    padding-left: 5px;
}
#main-card{
    max-width: 500px;
    padding: 20px;
}

</style>