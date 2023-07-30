<template>
  <section id="pratosDoDia">
    <h2>PRATOS DO DIA</h2>

    <div>
      <h3>{{ weekDay }}</h3>
      <p>(Feijão do dia ou Macassar)</p>
      <ul>
        <CardPratos
          nomePrato="Assado Misto"
          descricao="(Cupim, Frango e Calabresa) Feijão macassar, arroz à grega, vinagrete e farofa."
          :imageUrl="assadoMisto"
          preco="24,00" />
        <CardPratos
          nomePrato="Costela c/ Pirão"
          descricao="Pirão, arroz branco e legumes cozidos."
          :imageUrl="costela"
          preco="24,00" />
        <CardPratos
          nomePrato="Omelete de Charque"
          :imageUrl="omelete"
          preco="20,00" />
        <CardPratos
          nomePrato="Bisteca Suína Acebolada"
          :imageUrl="bisteca"
          preco="20,00" />
      </ul>
    </div>
  </section>
</template>

<script>
import { weekDayList } from '../data/diasDaSemana';
import CardPratos from './CardPratos.vue';

const weekDay = weekDayList[new Date().getDay()];

export default {
  data() {
    return {
      weekDay,
      assadoMisto:
        'https://firebasestorage.googleapis.com/v0/b/guara-burguer.appspot.com/o/Pratos%20do%20Dia%2FSegunda%2FFotos%20Guarar%20Burguer%20(150)%20Assado%20misto.jpg?alt=media&token=11defaaf-3bd5-4048-bd71-9250a0164650',
      costela:
        'https://firebasestorage.googleapis.com/v0/b/guara-burguer.appspot.com/o/Pratos%20do%20Dia%2FSabado%2FFotos%20Guarar%20Burguer%20(105)%20Costela%20pir%C3%A3o.jpg?alt=media&token=775f8429-1182-4c68-b556-b49bccce5b69',
      omelete:
        'https://firebasestorage.googleapis.com/v0/b/guara-burguer.appspot.com/o/Pratos%20do%20Dia%2FTerca%2FFotos%20Guarar%20Burguer%20(120)%20Omelete.jpg?alt=media&token=aa859ddb-b9de-49fe-955f-db3bcd6c1592',
      bisteca:
        'https://firebasestorage.googleapis.com/v0/b/guara-burguer.appspot.com/o/Todos%20os%20dias%2FFotos%20Guarar%20Burguer%20(160)%20Bisteca.jpg?alt=media&token=38217f2c-1444-4269-b0d9-740e1dee1173'
    };
  },
  components: { CardPratos }
};
</script>

<style>
section {
  padding: 10px 0;
  width: 95%;
  margin: auto;
}

section h2 {
  font-size: 1.875rem;
  padding: 0px 0 25px 0;
}

h3 {
  font-size: 1.6875rem;
}
</style>
