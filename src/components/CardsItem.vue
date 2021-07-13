<template>
    <li>
        <div class="card-title">
            <span>{{ card.title }}</span>
             <i class="fas fa-ellipsis-v"></i>
        </div>
        <div class="card-body">
            <span class="card-body--span">{{ card.letter }}</span>
        </div>
    </li>
</template>

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

<style scoped>

span {
    font-weight: 600;
}

.card-title {
    padding: 10px;
    display: flex;
    justify-content: space-between;
    background-color: #F0F1F8;
}

.card-body {
    width: 90%;
    padding: 10px;
    border: 1px solid #F2F2F2;
    
}

.card-body--span {
    font-weight: 400;
    
}

li {
    background:#F6FAFB;;
    box-shadow: 0px 4px 12px rgba(188, 188, 188, 0.25);
    border-radius: 3px;
    width: 200px;
    height: 200px;
    margin: 20px;
}
</style>