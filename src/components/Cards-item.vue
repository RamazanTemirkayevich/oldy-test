<template>
    <div class="cards-wrapper__items"
        v-for="product in products" :key="product.id"
    >
        <div class="cards-wrapper__items--inform">
            <span>{{ product.status }}</span>
        </div>
        <div class="cards-wrapper__items--img">
            <img :src="product.img" alt="pizza">
        </div>
        <div class="cards-wrapper__items--options">
            <div class="weight">
                <img src="@/assets/icons/weight_icon.svg">
                <p>{{ product.weight }}</p>
            </div>
            <div class="trash">
                <img src="@/assets/icons/buy.svg">
            </div>
            <div class="size">
                <img src="@/assets/icons/size_icon.svg">
                <p>{{ product.size }}</p>
            </div>
        </div>
        <div class="cards-wrapper__items--descr">
            <p class="descr-title">{{ product.name }}</p>
            <p class="descr-text">{{ product.text }}</p>
            <p class="descr-price">{{ product.price }} ₽</p>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            products: [
                {
                    id: 1,
                    status: 'New',
                    img: require("../assets/images/1.png"),
                    weight: '420г',
                    size: '30см',
                    name: 'Пепперони',
                    text: 'пикантная пепперони, томатный соус, моцарелла',
                    price: '395'
                },
                {
                    id: 2,
                    status: 'Sale',
                    img: require("../assets/images/2.png"),
                    weight: '450г',
                    size: '30см',
                    name: 'Четыре сыра',
                    text: 'филе говядины, вяленые помидоры, помидоры, перец сладкий, моцарела',
                    price: '425'
                },
                {
                    id: 3,
                    status: 'New',
                    img: require("../assets/images/3.png"),
                    weight: '410г',
                    size: '30см',
                    name: 'Диабло',
                    text: 'салями, шампиньоны, перец чили, сыр моцарелла, паприка, томатный соус',
                    price: '455'
                },
                {
                    id: 4,
                    status: 'Sale',
                    img: require("../assets/images/4.png"),
                    weight: '460г',
                    size: '30см',
                    name: 'Итальянская',
                    text: 'итальянские травы, пепперони, томатный соус, шампиньоны, моцарелла, маслины',
                    price: '480'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@media (min-width: 320px) {
    .cards-wrapper__items {
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: center;
        width: 130px;
        height: 235px;
        background: #FFFFFF;
        box-shadow: 5px 5px 25px rgba(0, 0, 0, 0.08);
        border-radius: 5px;

        &--inform {
            position: absolute;
            display: flex;
            align-items: center;
            justify-content: center;
            top: 7px;
            right: 8px;
            width: 34px;
            height: 13px;
            filter: drop-shadow(0px 4px 20px rgba(235, 33, 46, 0.3));
            background: linear-gradient(91.85deg, #FF5863 0.1%, #EB212E 101.94%, #EB212E 101.94%);
            border-radius: 2px;

            &>span {
                font-weight: 700;
                font-size: 7px;
                line-height: 10px;
                color: #FFFFFF;
            }
        }

        &--img {
            margin: 35px auto auto auto;
            width: 80%;

            &>img {
                width: 100%;
            }
        }

        &--options {
            margin: -10px auto;
            display: flex;
            width: 90%;
            height: 31px;
            justify-content: space-between;
            align-items: flex-end;

            .weight, .size {
                width: 31.63px;
                display: flex;
                justify-content: space-between;

                &>img {
                    width: 10px;
                }

                &>p {
                    font-weight: 400;
                    font-size: 9px;
                    line-height: 14px;
                    color: #393939;
                }
            }

            .trash {
                display: flex;
                align-items: center;
                justify-content: center;
            }
        }

        &--descr {
            margin: 15px auto auto auto;  
            width: 110px;
            display: flex;
            flex-direction: column;
            align-items: center;

            .descr-title {
                font-weight: 700;
                font-size: 12px;
                line-height: 17px;
                color: #EB212E;
            }

            .descr-text {
                text-align: center;
                font-weight: 400;
                font-size: 6px;
                line-height: 9px;
                color: #6B6B6B;
            }

            .descr-price {
                font-weight: 700;
                font-size: 12px;
                line-height: 22px;
                color: #393939;
            }
        }
    }
}
</style>
