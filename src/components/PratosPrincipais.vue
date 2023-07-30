<template>
  <section id="pratosPrincipais">
    <h2>PRATOS PRINCIPAIS</h2>
    <ul>
      <CardPratos
        nomePrato="Feijoada"
        descricao="Arroz branco, couve refogada, laranja e farofa."
        :imageUrl="feijoada" preco="26,00"/>
      <CardPratos
        nomePrato="Dobradinha"
        descricao="Fava, arroz branco e farofa."
        :imageUrl="dobradinha" preco="20,00"/>
      <CardPratos
        nomePrato="Frango à parmegiana"
        descricao="Macarrão espaguete, molho de tomate e purê de batata."
        :imageUrl="parmegiana" preco="22,00"/>
      <CardPratos
        nomePrato="Strogonoff de frango"
        descricao="Arroz branco, purê de batata, salada e batata palha."
        :imageUrl="strogonoff" preco="18,00"/>
    </ul>
  </section>
</template>

<script>
import CardPratos from './CardPratos.vue';

export default {
  components: { CardPratos },
  name: 'PratosPrincipais',
  data() {
    return {
      feijoada:
        'https://firebasestorage.googleapis.com/v0/b/guara-burguer.appspot.com/o/Pratos%20Principais%2FFotos%20Guarar%20Burguer%20(57)%20Feijoada.jpg?alt=media&token=10700c97-2c09-4df5-9aba-4bde3abef7ca',
      dobradinha:
        'https://s2.glbimg.com/TU9P6952S8K6MPXDmJY0E_6hztg=/0x0:1280x800/984x0/smart/filters:strip_icc()/i.s3.glbimg.com/v1/AUTH_1f540e0b94d8437dbbc39d567a1dee68/internal_photos/bs/2022/V/d/blmCJLSu63MBTBuXsvug/dobradinha-com-feijao-branco.jpg',
      parmegiana:
        'https://firebasestorage.googleapis.com/v0/b/guara-burguer.appspot.com/o/Todos%20os%20dias%2FFotos%20Guarar%20Burguer%20(50)%20parmegiana.jpg?alt=media&token=d8b8a02b-eb20-4129-ab54-a573bf725e68',
      strogonoff:
        'https://firebasestorage.googleapis.com/v0/b/guara-burguer.appspot.com/o/Pratos%20do%20Dia%2FTerca%2FFotos%20Guarar%20Burguer%20(76)%20Strogonoff.jpg?alt=media&token=1022adb0-9d4a-4246-839f-c2bd1d15888d'
    };
  }
};
</script>

<style scoped>
section {
  padding: 10px 0;
  width: 95%;
  margin: auto;
}

section h2 {
  font-size: 1.875rem;
  padding: 0px 0 25px 0;
}
</style>
