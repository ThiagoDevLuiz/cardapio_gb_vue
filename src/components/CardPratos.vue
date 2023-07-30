<template>
  <div>
    <li>
      <div class="noImage">
        <div>
          <div class="espacamento">
            <span>{{ nomePrato }}</span>
          </div>
          <p class="descricao">{{ descricao }}</p>
        </div>
        <p class="preço">R$ {{ preco }}</p>
      </div>
      <div>
        <img
          class="fotoPadrao"
          :src="imageUrl"
          @click="openModal"
          alt="foto prato"
          width="125"
          height="105" />
      </div>
    </li>

    <div v-if="modalVisible" class="modalOverlay" @click="closeModal">
      <div class="modalContent">
        <img :src="imageUrl" alt="foto prato" class="modalImage" />
        <button class="buttonModal">Fechar</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardPratos',
  props: {
    nomePrato: String,
    preco: Number,
    imageUrl: {
      type: String,
      required: true
    },
    descricao: {
      type: String,
      default: 'Feijão do dia, arroz à grega, macarrão espaguete e vinagrete.'
    }
  },
  data() {
    return {
      modalVisible: false
    };
  },
  methods: {
    openModal() {
      this.modalVisible = true;
    },
    closeModal() {
      this.modalVisible = false;
    }
  }
};
</script>

<style scoped>
section ul li {
  list-style: none;
  text-align: start;
  border: 1px solid #764a3b;
  border-radius: 15px;
  padding: 0px 13px 5px 10px;
  display: flex;
  margin: 15px 0 15px 0;
  justify-content: space-between;
}

.espacamento {
  margin: 10px 0 15px 0;
}

span {
  font-family: 'Myriad-SemiBold';
  font-size: 1.25rem;
}

.fotoPadrao {
  border-radius: 10px;
  margin: 13px 0 0 25px;
  cursor: pointer;
}

.preço {
  font-family: 'Myriad-SemiBold';
  margin: 13px 0 2px 0;
  font-size: 1.125rem;
}

.noImage {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.modalOverlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.8);
  display: flex;
  justify-content: center;
  align-items: center;
}

.modalContent {
  position: relative;
  border-radius: 10px;
  padding: 20px;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.closeButton {
  position: absolute;
  top: 10px;
  right: 10px;
  font-size: 1.5rem;
  cursor: pointer;
}

.modalImage {
  max-width: 80vw;
  max-height: 80vh;
  border-radius: 15px;
  object-fit: cover;
}

.buttonModal {
  width: 30%;
  height: 40px;
  align-self: center;
  border: none;
  border-radius: 10px;
  background-color: #fdd5af;
  color: #764a3b;
  font-family: Myriad-SemiBold;
  font-size: 1.3rem;
  cursor: pointer;
}
</style>
