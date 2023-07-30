<template>
  <header class="App-header">
    <img class="logo" src="/LogoGB.png" alt="LogoGB" width="250" />
    <h1>Guara Burguer</h1>
    <h5>Almoço, lanches e jantas</h5>
  </header>

  <main>
    <Menu />

    <HorarioAlmoco />

    <PratosPrincipais />

    <PratosDoDia />
  </main>

  <footer>
    <p>
      2022 Guara Burguer - Todos os direitos reservados<br />
      guaraburguer5@gmail.com (81)9.8518.8955
    </p>
  </footer>
</template>

<script>
import Menu from './components/Menu.vue';
import HorarioAlmoco from './components/HorarioAlmoco.vue';
import PratosPrincipais from './components/PratosPrincipais.vue';
import PratosDoDia from './components/PratosDoDia.vue';

export default {
  name: 'App',
  components: {
    Menu,
    HorarioAlmoco,
    PratosPrincipais,
    PratosDoDia
  }
};
</script>


<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  outline: 0;
}

html {
  scroll-behavior: smooth;
  background-color: #fee9d4;
}

@font-face {
  font-family: 'Myriad-Regular';
  src: url(assets/Fonts/MYRIADPRO-REGULAR.woff);
}

@font-face {
  font-family: 'Myriad-Bold';
  src: url(assets/Fonts/MYRIADPRO-BOLD.woff);
}

@font-face {
  font-family: 'Myriad-SemiBold';
  src: url(assets/Fonts/MYRIADPRO-SEMIBOLD.woff);
}

body {
  text-align: center;
  font-family: 'Myriad-Regular';
  background-color: #fee9d4;
  color: #764a3b;
}

header {
  padding: 20px 0 30px 0;
  line-height: 35px;
  font-size: 1.37rem;
  font-family: 'Myriad-Bold';
}

footer {
  background-color: #fdd5af;
  padding: 10px;
  text-align: center;
  margin-top: 25px;
}
</style>
