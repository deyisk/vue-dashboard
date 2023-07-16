<template>
  <div>
    <div
      class="cards"
      v-for="card in cards"
      :key="card.id"
      :class="['card', 'card-' + card.id]"
    >
      {{ card.title }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        { id: 1, title: 'Card 1' },
        { id: 2, title: 'Card 2' },
        { id: 3, title: 'Card 3' },
        { id: 4, title: 'Card 4' }
      ]
    };
  }
};
</script>

<style>
.cards {

  width: 25%;
  float: right;
  padding: 30px;
  height: 12rem;
  text-align: center;
  margin-right: 100px;
  justify-content: center;
}

.card-1 {
  background-color: red;
}

.card-2 {
  background-color: green;
}

.card-3 {
  background-color: yellow;
}

.card-4 {
  background-color: orange;
}

@media (max-width: 992px) {
  .cards {
     
    width: 50%;
    margin: 0 auto;
    float: none;
    margin-top: 1rem;
  }
}

@media (max-width: 768px) {
  .cards {
   
    
    width: 75%;
    margin: 0 auto;
    float: none;
    margin-top: 1rem;
    margin-right: 0;
  }
}

@media (max-width: 576px) {
  .cards {
     
    width: 90%;
    margin: 0 auto;
    float: none;
    margin-top: 1rem;
    margin-right: 0;
  }
}

@media (max-width: 400px) {
  .cards {
     
    width: 100%;
    margin: 0 auto;
    float: none;
    margin-top: 1rem;
    margin-right: 0;
    height: auto;
    padding: 20px;
  }
}
</style>
