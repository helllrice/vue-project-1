<template>
  <div>
    <ul>
      <CardsItem 
        v-bind:card="card"
        v-for="card in cards" :key="card.title"
      />
    </ul>
  </div>
</template>

<script >
  import CardsItem from '@/components/CardsItem'
  
  export default {
    props: ['cards', 'title'],
    components: {
      CardsItem
    }
  }
</script>

<style scoped>
div {
  display: flex;
  width: 100%;
}

 ul {
   list-style: none;
   display: flex;
   justify-content: flex-start;
   flex-wrap: wrap;
 }
</style>