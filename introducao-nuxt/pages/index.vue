<template>
  <div class="main">
    <h1>{{ title }}</h1>
    <table border="1">
      <thead>
        <tr>
          <th>Nome</th>
          <th>Poder</th>
        </tr>
      </thead>
      <tbody>
        <tr :key="item.id" v-for="item in herois">
          <td>{{item.nome}}</td>
          <td>{{item.poder}}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
  export default {
    data: function(){
      return{
        title: "Tabela de personagens DC",
        herois: [
          {id: 0, nome: "Flash", poder: (Math.random() * 100).toFixed(0)},
          {id: 1, nome: "Batman", poder: (Math.random() * 100).toFixed(0)},
          {id: 2, nome: "Dr. Manhattan", poder: (Math.random() * 100).toFixed(0)},
          {id: 3, nome: "John Constantine", poder: (Math.random() * 100).toFixed(0)},
        ]
      }
    }
  }
</script>

<style>
  .main{
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  table * {
    border: 1px solid #000;
    border-collapse: collapse;
    padding: 10px 15px;
  }
  table th{
    background-color: #000;
    color: #fff;
  }

  table th:first-child{
    border-right-color: #fff;
  }
</style>