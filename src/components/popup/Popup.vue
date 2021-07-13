<template>
    <div class="popup__wrapper">
        <div class="popup">
            <div class="popup__header">
                <p class="popup__header-title">Добавление</p>
                <span
                    @click="closePopup"
                >X</span>
            </div>
            <form v-on:submit.prevent="addNewCard">
                <div class="popup__content">
                <div class="popup__content-body">
                    <p>Номер накладной</p>
                    <input v-model="newCardText" type="text" placeholder="Введите значение">
                </div>
                <div class="popup__content-footer">
                    <p>Тип заказа</p>
                    <input v-model="newCardText"  type="text">
                    <button  class="popup__button" @click="closePopup">Оформить</button>
                </div>
            </div>
            </form>
        </div>
    </div>
</template>

<script>
    export default {
        name: "popup",
        props: ['id', 'title', 'letter',],
        data() {
            return {}
        },
        methods: {
            closePopup() {
                this.$emit('closePopup')
            },
            
        },
        computed: {}
    }
</script>

<style scoped>
    .popup__wrapper {
        background: rgba(64, 64, 64, .4);
        display: flex;
        justify-content: center;
        align-items: center;
        position: absolute;
        right: 0;
        left: 0;
        top: 0;
        bottom: 0;
    }

    .popup {
        position: fixed;
        top: 150px;
        margin: 0 auto;
        right: 0;
        left: 0;
        width: 400px;
        height: 300px;
        background-color: #fff;
        
        border-radius: 2px;
    }
    
    .popup__header {
        width: 100%;
        padding: 15px;
    }
    
    .popup__header-title {
        padding-top: 20px;
        margin: 0 auto;
        text-align: center;
    }
    
    span {
        cursor: pointer;
        position: absolute;
        top: 10px;
        left: 370px;
    }
    
   .popup__content-body {
       padding-left: 30px;
   }
   
   .popup__content input {
       border: 1px solid #D9D9D9;
       width: 350px;
       height: 30px;
       border-radius: 2px;
       padding-left: 15px;
   }
   
   .popup__content-footer {
       padding-left: 30px;
   }
   
   .popup__button {
       margin-top: 20px;
       align-items: center;
       margin-left: 120px;
       background-color: rgb(73,67,205);
       color: #ffffff;
       border: none;
       padding: 10px;
       cursor: pointer;
   }
</style>
