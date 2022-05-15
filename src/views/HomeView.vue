<template>
  <div class="home">
    <h1>Home</h1>
    <div class="cards">
      <CardBox 
      itemName="Card 1"
      itemDesc="description"
      itemImage="https://cdn-icons-png.flaticon.com/512/5149/5149064.png"
      />
      <CardBox 
      itemName="Card 2"
      itemDesc="description"
      itemImage="https://cdn-icons-png.flaticon.com/512/7465/7465886.png"
      />
      <CardBox 
      itemName="Card 3"
      itemDesc="description"
      itemImage="https://cdn-icons-png.flaticon.com/512/4219/4219963.png"
      />
      <CardBox 
      itemName="Card 4"
      itemDesc="description"
      itemImage="https://cdn-icons-png.flaticon.com/512/7215/7215701.png"
      />
      <CardBox 
      itemName="Card 5"
      itemDesc="description"
      itemImage="https://cdn-icons-png.flaticon.com/512/4456/4456860.png"
      />
      <CardBox 
      itemName="Card 6"
      itemDesc="description"
      itemImage="https://cdn-icons-png.flaticon.com/512/5345/5345472.png"
      />
      <CardBox 
      itemName="Card 7"
      itemDesc="description"
      itemImage="https://cdn-icons-png.flaticon.com/512/4105/4105458.png"
      />
      <CardBox 
      itemName="Card 8"
      itemDesc="description"
      itemImage="https://cdn-icons-png.flaticon.com/512/4524/4524473.png"
      />
    </div>
  </div>
</template>

<script>
import CardBox from '../components/CardBox.vue';

export default {
  name: 'HomeView',
  components: {
    CardBox
  } 
}
</script>

<style scoped>
  .cards{
    display: flex;
    flex-direction: row;
    justify-content: center;
    flex-wrap: wrap;
  }
</style>
