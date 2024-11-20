<script>
export default{
  name: "App",
  methods: {
    // loadChip(){
    //   new URL('src/assets/img/' + this.urlChip, import.meta.url).href
    // }
  },
  data(){
    return{
      title: "",
      urlChip: "",
      codigo: "",
      fechaExp: "",
      dueño: "",
      type: ""
    }
  }
}
</script>

<template>
  <div id="app">
      <form>
        <div>
          <label>Título de la tarjeta: </label>
          <input v-model="title" />
        </div>

        <div>
          <label>Chip SRC: </label>
          <input v-model="urlChip"/>
        </div>

        <div>
          <label>Número: </label>
          <input v-model="codigo" />
        </div>

        <div>
          <label>Fecha de expiración: </label>
          <input v-model="fechaExp" />
        </div>

        <div>
          <label>Propietario: </label>
          <input v-model="dueño"/>
        </div>

        <div>
          <label>Tipo de tarjeta SRC: </label>
          <input  v-model="type">
        </div>
      </form>

      <div class="carnet">
        <h3> {{ title }}</h3>
        <img width="40" :src="'/src/assets/img/'+urlChip"  alt="" />
        <div class="midle">
          <h2>{{codigo}}</h2>
        </div>
        <div class="midle">
          <span>Fecha Exp: <b>{{fechaExp}}</b></span>
        </div>
        <footer>
          <span>{{dueño}}</span>
          <img :src="'src/assets/img/'+type" width="60" />
        </footer>
      </div>
    </div>

</template>

<style scoped>
 * {
        margin: 0;
      }
      body {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 60vh;
        font-size: 10px;
        font-family: sans-serif;
      }

      #app {
        display: flex;
        gap: 40px;
      }
      form {
        padding: 18px;
        border-radius: 20px;
        border: ridge 1px;
        box-shadow: 1px 1px 1px 1px gray;
        font-weight: bold;
        display: flex;
        flex-direction: column;
        gap: 15px;
        justify-content: center;
      }
      form div {
        display: grid;
        grid-template-columns: 100px 200px;
        align-items: start;
        gap: 5px;
      }

      form div label {
        text-align: right;
      }

      .carnet h3{
        text-align: start;
      }

    .midle{
      display: flex;
      flex-direction: column;
      align-items: start;
    }

    

      .carnet {
        width: 400px;
        height: 230px;
        background: #1c1a1e;
        color: white;
        border-radius: 20px;
        padding: 20px;
        box-shadow: 0px 0px 10px 2px black;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
      }

      h3 {
        font-size: 20px;
      }

      h2 {
        font-size: 30px;
        letter-spacing: 10px;
        margin-bottom: 15px;
        text-shadow: 0px 0px 1px gold;
        font-family: Times;
      }

      b {
        font-size: 16px;
      }

      footer {
        display: flex;
        justify-content: space-between;
        align-items: flex-end;
        font-weight: bold;
        font-size: 18px;
        text-transform: uppercase;
        font-style: italic;
      }
</style>
