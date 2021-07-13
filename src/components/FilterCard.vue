<template>
    <div class="filter">
         <h2 class="filter-title">Filters</h2>
         <div class="filter__body">
            <h2 class="filter__body--title">Invoice number</h2>
            <input type="text" placeholder="Enter value">
         </div>
    </div>
</template>

<style scoped>

    .filter {
        width: 280px;
        height: 160px;
        margin: 20px;
        box-shadow: 0px 4px 12px #EBEBEB;
        border-radius: 3px;
    }

    .filter-title {
        font-weight: 700;
        padding: 15px 38px;
        font-family: Roboto;
        font-style: normal;
        font-weight: bold;
        font-size: 16px;
        line-height: 19px;
        border-bottom: 1px solid #EBEBEB;
    }

    .filter__body {
        margin-right: 20px;
    }

    .filter__body--title {
        padding: 5px 30px;
        font-size: 14px;
    }

    input {
        margin-left: 30px;
        padding: 7px 10px 7px 10px;
        width: 220px;
        height: 30px;
        font-family: 'Roboto';
        background: #FFFFFF;
        border: 1px solid #D9D9D9;
        box-sizing: border-box;
        border-radius: 2px;
    }

</style>