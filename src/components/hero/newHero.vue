<template>
 <div class="container">
    <div class="cards-row">
      <div class="card"
           v-for="card in cards.slice(0, 2)"
           :key="card.id"
           :class="'card-' + card.id"
      >
        {{ card.title }}
      </div>
    </div>

    <div class="cards-row">
      <div class="card"
           v-for="card in cards.slice(2, 4)"
           :key="card.id"
           :class="'card-' + card.id"
      >
        {{ card.title }}
      </div>
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
.cards-row{
  margin:20%;
  text-align: center;
}

.card {
  width: 25vh;
  height: 20vh;
  margin-bottom: 30px; 
  
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
</style>
