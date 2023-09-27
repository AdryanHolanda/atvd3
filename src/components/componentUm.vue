<template>
  <div>
    <h1>Faça sua pergunta: </h1>
    <input type="text" v-model="pergunta">
    <button @click="gerarResp">Enviar</button>
    <h2>  <p>{{perguntaExibida}} </p></h2>
     <p> {{ resposta }}</p>
  </div>
</template>

<script>
export default {
  name: 'componentUm',
  data() {
    return {
      pergunta: "",
      resposta: "",
      nRandom: "",
      respostas: "",
    }
  },
  methods: {
    gerarResp() {
      this.perguntaExibida= this.pergunta;
       this.respostas = [
        'Com certeza', 
        'É... não tenho certeza!', 
        'Claro que não', 
        'Acho difícil', 
        'Possivelmente não'
      ];

      this.nRandom = Math.floor(Math.random() * 5);
      this.resposta = this.respostas[this.nRandom];
    }
  }
}
</script>

<style>

</style>
