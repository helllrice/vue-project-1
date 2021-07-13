<template>
  <div id="app">
    <div class="app__title">
      <ButtonAdd 
        @click="showPopupInfo"
      />
      <SortingCard />
      <Switches />
    </div>
    <div class="app__body">
      <FilterCard />
      <Cards  v-bind:cards="cards"/>
    </div>
    <SwitchCard/>
  </div>
</template>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');

  * {
    box-sizing: border-box;
    font-family: 'Roboto', sans-serif;
  }

  #app {
    width: 1200px;
    margin: 0 auto;
  }
  
  .app__title {
    display: flex;
    justify-content: space-between;
  }
  
  .app__body {
    display: flex;
  }
</style>

<script>
  import ButtonAdd from '@/components/ButtonAdd'
  import SortingCard from '@/components/SortingCard'
  import Switches from '@/components/Switches'
  import FilterCard from '@/components/FilterCard'
  import Cards from '@/components/Cards'
  import SwitchCard from '@/components/SwitchCard'
  
  
  export default {
    name: 'app',
    props: {},
    data() {
    return {
      newCardText: '',
      cards: [
        {id: 1, title: 'Card 1', letter: 'A'},
        {id: 2, title: 'Card 2', letter: 'B'},
        {id: 3, title: 'Card 3', letter: 'C'},
        {id: 4, title: 'Card 4', letter: 'D'},
        {id: 5, title: 'Card 5', letter: 'E'}
      ],
      nextCardId: 6
    }
  },
  
  methods: {
      addNewCard: function () {
        this.cards.push({
          id: this.nextCardId++,
          title: this.newCardText
        })
        this.newCardText = ''
      }
    },
    
    
    
    components: {
      ButtonAdd,
      SortingCard,
      Switches,
      FilterCard,
      Cards,
      SwitchCard,
    }
    
  }
</script>
