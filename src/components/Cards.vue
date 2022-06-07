<template>
    <div class="cards-container">
        <h1 class="cards-title">Пицца</h1>
        <div class="cards-wrapper">
            <CardsItem/>       
        </div>
    </div>
</template>

<script>
import CardsItem from './Cards-item.vue'
export default {
    components: {
        CardsItem
    }
}
</script>

<style lang="scss" scoped>
    @media (min-width: 320px) {
        .cards-container {
            margin: auto;
            width: 290px;
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            justify-content: center;
        }

        .cards-title {
            margin-left: 0;
        }

        .cards-wrapper {
            width: 271px;
            height: 489px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-direction: row;
            flex-wrap: wrap;
            margin: auto;
        }
    }
</style>
