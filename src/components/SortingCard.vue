<template>
    <div class="sorting">
        <div class="sorting__select">
            <select v-model="select">
                <option v-for="(select, index) in selects" :key="index">{{ select }}</option>
            </select>
        </div>
    </div>
</template>

<style scoped>
    .sorting {
        width: 810px;
        height: 70px;
        box-sizing: border-box;
        border-radius: 2px;
        box-shadow: 0px 4px 12px #EBEBEB;
    }
    
    select {
      margin: 20px;
      width: 250px;
      height: 30px;
      border: 1px solid #E0E5E6;
      font-weight: 700;
    }
</style>

<script>
    export default {
    props: ['cards'],
    methods: {
    handleChange(value) {
      console.log(`selected ${value}`);
    }
  },
    data () {
      return {
        selects: [ 'Sorting', 'Sort by invoice number: ascending', 'Sort by invoice number: descending'],
        select: 'Sorting'
      }
    }

  }
</script>