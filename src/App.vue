<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <router-link to="/Kelas">Data Kelas </router-link>
    <router-link to="/siswa">Data Siswa</router-link>
    <router-view/> -->
  <h1>{{ nama }}</h1>
  <h2>Nama : <input v-model="nama" type="" name=""><br></h2>
  <h2>Nilai Anda : {{  nilai }}</h2>
  <button @click = "totalnilai">Click Me</button>
  <h2>1. Siapakah Pelukis Lukisan Monalisa ?</h2>
  <input type="radio" name="" v-model="soal1" value="Leonardo Da Vinci">Leonardo Da Vinci
  <input type="radio" name="" v-model="soal1" value="Leonardo Di Caprio">Leonardo Di Caprio
  <input type="radio" name="" v-model="soal1" value="Leonardo Da Odon">Leonardo Da Odon
  <input type="radio" name="" v-model="soal1" value="Leonardo Bonnuci">Leonardo Bonnuci<br>
  <h2>2. Berapakah  Angka Setelah 12 ?</h2>
  <input type="radio" name="" v-model="soal2" value="10">10
  <input type="radio" name="" v-model="soal2" value="13">13
  <input type="radio" name="" v-model="soal2" value="11">11
  <input type="radio" name="" v-model="soal2" value="14">14<br>
  <h2>3. Tanggal Berapakah Hari Ibu Kartini ?</h2>
  <input type="radio" name="" v-model="soal3" value="28 Agustus">28 Agustus
  <input type="radio" name="" v-model="soal3" value="21 Agustus">21 Agustus
  <input type="radio" name="" v-model="soal3" value="28 April">28 April
  <input type="radio" name="" v-model="soal3" value="21 April">21 April<br>
  </div>
</template>

<script>
/*import HelloWorld from './components/HelloWorld.vue'
*/
export default {
  name: 'App',
  data() {
    return{
      nama: '',
      nilai: 0,
      soal1: '',
      soal2: '',
      soal3: ''
    }
  },
  methods: {
    totalnilai(){
      if(this.soal1 == 'Leonardo Da Vinci' && this.soal2 == '13' && this.soal3 == '21 April') {
        this.nilai=+3
      }
      else if (this.soal1 == 'Leonardo Da Vinci' && this.soal2 == '13') {
        this.nilai=+2
      }
      else if (this.soal1 == 'Leonardo Da Vinci' && this.soal3 == '21 April') {
        this.nilai=+2
      }
      else if (this.soal2 == '13' && this.soal3 == '21 April') {
        this.niali=+2
      }
      else if (this.soal1 == 'Leonardo Da Vinci') {
        this.nilai=+1
      }
      else if (this.soal2 == '13') {
        this.nilai=+1
      }
      else if (this.soal3 == '21 April') {
        this.nilai=+1
      }
      else{
        this.nilai = 0
      }
    }
  }
  /*,
  components: {
    HelloWorld
  }*/
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>