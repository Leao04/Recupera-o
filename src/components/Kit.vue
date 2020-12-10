<template>
<div class="corpo">
    <div class="card">
  <img src="../assets/surviver.jpg" alt="produto">
  <div class="container">
    <h1><b>Kit de sobrevivência</b></h1>
    <p>-Artigo Militar</p>
    <div class="price">
      <h2>
        R$101,00
      </h2>
    </div>
    <div class="multiple">
      <p>12x R$ 10,14 </p>
    </div>
  </div>
    </div>
</div>
</template>

<script>
export default {
  components: {
   Kit
},
};
</script>

<style scoped>
.card {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  transition: 0.3s;
}
.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}
.container {
  padding: 2px 16px;
}
.corpo {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  width: 30%;
}
.price{
  color: green;
}
</style>