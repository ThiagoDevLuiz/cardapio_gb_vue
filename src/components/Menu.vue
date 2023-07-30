<template>
  <div class="menu-wrapper">
    <div class="menu">
      <nav>
        <ul>
          <li>
            <a href="#pratosPrincipais">PRATOS PRINCIPAIS</a>
          </li>
          <li>
            <a href="#pratosDoDia">PRATOS DO DIA</a>
          </li>
          <li>
            <a href="#todosOsDias">TODOS OS DIAS</a>
          </li>
          <li>
            <a href="#porcoes">PORÇÕES EXTRAS</a>
          </li>
          <li>
            <a href="#bebidas">BEBIDAS</a>
          </li>
          <li>
            <a href="#sobremesas">SOBREMESAS</a>
          </li>
          <li>
            <a href="#janta">JANTA</a>
          </li>
          <li>
            <a href="#bebidasQuentes">BEBIDAS QUENTES</a>
          </li>
          <li>
            <a href="#vitaminas">VITAMINAS</a>
          </li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Menu'
};
</script>

<style scoped>
.menu-wrapper {
  white-space: nowrap;
  /* overflow: hidden; */
  overflow-x: auto;
  padding: 20px 10px;
}

.menu-wrapper::-webkit-scrollbar {
  display: none;
}

nav ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

nav li {
  display: inline-block;
  margin-right: 10px;
  border: 1px solid #fdd5af;
  border-radius: 20px;
  padding: 8px 20px;
  background-color: #fdd5af;
}

nav a {
  font-family: 'Myriad-SemiBold';
  text-decoration: none;
  color: #764a3b;
}
</style>
