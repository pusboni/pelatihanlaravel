<template>
    <div class="content">
            
            <h1>Calculator</h1>
            <input type="number" v-model="number1">
            <input type="number" v-model="number2">
            <button @click="submit">Submit</button>
            Total : {{ hasil }}
            <br>
            <div v-if="hasil != null">
                <span v-if="hasil >60">Lulus</span>
                <span v-else>Tidak Lulus</span>
            </div>

            <ul>
                <li v-for="item in list" :key="item.nama">
                    {{ item.nama }}
                </li>
            </ul>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                list: [
                    {nama: "arsyad"},
                    {nama: "Ivan"},
                    {nama: "bonbon"}
                ],
                number1: 0, 
                number2: 0,
                hasil: 0
            }
        },
        methods : {
            submit(){
                console.log("arsyad");
                this.hasil = parseInt(this.number1) + parseInt(this.number2)
            }

        }
    }
</script>
<style scoped>
    .content{
        width: 700px;
        margin: 0 auto;
    }
</style>