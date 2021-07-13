<template>
     <div class="card__box">
         <ul class="card__list__title">
             <li>ID</li>
             <li>Номер накладной</li>
             <li>Тип Заказа</li>
             <li>Датa создания</li>
             <li></li>
         </ul>
         <div class="card__list__body">
             <div></div>
             <div></div>
             <div></div>
             <div></div>
             <div></div>
         </div>
     </div>
</template>

<style scoped>
    .card__box {
        width: 912px;
    }

    .card__list__title {
        display: flex;
        justify-content: space-between;
        list-style: none;
    }
    
    .card__list__body {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        height: 200px;
        border: 1px solid #E6E6E6;
    }
    
    .card__list__body div {
        padding: 10px;
        border-top: 1px solid #E6E6E6;
    }
    
    li {
        margin: 3px;
        padding: 10px;
    }
    
    li:nth-child(1) {
        width: 134px;
        height: 40px;
        text-align: center;
        background: #E6E6E6;
    }
    
    li:nth-child(2) {
        width: 244px;
        height: 40px;
        text-align: center;
        background: #E6E6E6;
    }
    
    li:nth-child(3) {
        width: 189px;
        height: 40px;
        text-align: center;
        background: #E6E6E6;
    }
    
    li:nth-child(4) {
        width: 268px;
        height: 40px;
        text-align: center;
        background: #E6E6E6;
    }
    
    li:nth-child(5) {
        width: 65px;
        height: 40px;
        background: #E6E6E6;
    }
    
</style>

<script>
export default {
        props: {
            card: {
                type: Object,
                default() {
                    return {}
                }
            }
        }
    }
</script>
