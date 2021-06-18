<template>
    <h1>Kalkulator</h1>
    <table>
        <tr>
            <td>Input angka ke-1</td>
            <td>: <input type="number" v-model="input1"></td>
        </tr>
        <tr>
            <td>Input angka ke-2</td>
            <td>: <input type="number" v-model="input2"></td>
        </tr>
    </table><br/>
    <div>
        <button v-on:click="tambah" style="width: 80px;">+</button>
        <button v-on:click="kurang" style="margin-left:80px; width: 50px;">-</button>
        <button v-on:click="kali" style="margin-left:80px; width: 50px;">x</button>
        <button v-on:click="bagi" style="margin-left:80px; width: 50px;">/</button>
    </div>
    <div>
        <h1>Hasil : {{ hasil }}</h1>
    </div>
</template>

<script>
export default {
    data(){
        return{
            hasil : 0
        }
    },
        methods:{
            tambah(){
                this.hasil = parseInt(this.input1) + parseInt(this.input2);
            },
            kurang(){
                this.hasil = parseInt(this.input1) - parseInt(this.input2);
            },
            kali(){
                this.hasil = parseInt(this.input1) * parseInt(this.input2);
            },
            bagi(){
                this.hasil = parseInt(this.input1) / parseInt(this.input2);
            },
        }
}
</script>
<style>
    *{background: #6F00FF
    }
</style>