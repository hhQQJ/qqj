<template>
    <div class="box">
        <div class="contetn">
            <div class="banner">
                <img :src="dataList.imageSrc1">
            </div>
            <p class="banner-text">{{ dataList.textContent }}</p>
            <div class="text-list">
                <div class="left">
                    <p v-for="(item, index) in dataList.splitContent.left" :key="index">
                        {{ item }}
                    </p>
                </div>
                <div class="right">
                    {{ dataList.splitContent.right }}
                </div>
            </div>
            <div class="img-list">
                <img v-for="(item, index) in dataList.imageList" :key="index" :src="item.imgItem" alt="">
            </div>
            <div class="nuxtPage">
                <h2>
                    <p>View the next project</p>
                    <img src="https://assets-global.website-files.com/62fd28cdd386f6a9d130721f/63026dc1b0d76c4fde3a1767_nextproject.svg"
                        loading="lazy" alt="">
                </h2>
                <div class="nextprojectblock" @click="nextClick">
                    <div class="left">
                        <img src="https://assets-global.website-files.com/62fd28cdd386f6a9d130721f/6302702409a3221a313e4c31_FormatNExt.png"
                            loading="lazy" width="50" alt="" class="image-13">
                        <p>Format</p>
                    </div>
                    <div class="right">
                        <p>eCommerce</p>
                        <p>Visual Language</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
const route = useRoute()
onMounted(() => {
    console.log(route.params.id)
    if (route.params.id === 1) {
        // 根据id给dataList不同的数据
    }
})
const dataList = ref(
    {
        imageSrc1: '/page-1.png',
        textContent: 'A large glass of wine in a single serve bottle, made in small, sustainably farmed batches with no additives.',
        splitContent: {
            left: ['Credits', 'Additional Design by Ananya Arora', 'Photography by Thomas Albdorf', 'Industrial Design Naman Nanda', 'Glass Design by Karim Rashid'],
            right: 'With the bottle silhouette already fabricated, I worked with the founding team to design a brand around it that would feel anything but usual. Starting with the name, moving through to the core identity, and setting the direction for photography while fleshing out the full visual language in a digital context and beyond.',
        },
        imageList: [
            {
                imgItem: 'https://assets-global.website-files.com/62fd28cdd386f6a9d130721f/62ffe7bd1c419cf97db7b687_UsualBottles-p-2600.png'
            },
            {
                imgItem: 'https://assets-global.website-files.com/62fd28cdd386f6a9d130721f/62ffe9471c419c32c8b7d3e8_UsualCans.png'
            },
            {
                imgItem: 'https://assets-global.website-files.com/62fd28cdd386f6a9d130721f/62ffe9a3cc51c7a855c48a3c_03.png'
            },
            {
                imgItem: 'https://assets-global.website-files.com/62fd28cdd386f6a9d130721f/62ffe566590f937c7c0f1180_05.png'
            },
        ]
    }
)
const nextClick = () =>{
    if(route.params.id === 8){
        navigateTo('/details/1')
    }else{
        navigateTo('/details/' + (Number(route.params.id) + 1))
    }
}
</script>
<style lang="scss" scoped>
.box {
    width: 100%;
    background-color: #f3f3f3;
    box-sizing: border-box;
}

@media screen and (min-width: 768px) {
    .contetn {
        box-sizing: border-box;
    }

    .banner {
        box-sizing: border-box;
        height: 38vw;
        border-radius: 3vw;
        padding: 0 3vw;

        img {
            width: 100%;
            height: 100%;
            box-sizing: border-box;
            border-radius: 3vw;
        }
    }

    .banner-text {
        color: #000;
        font-family: PP Neue Montreal, sans-serif;
        font-size: 2.2vw;
        font-weight: 400;
        line-height: 4vw;
        border-bottom: 1px solid #000;
        padding-bottom: 4vw;
        padding-left: 4vw;
        padding-right: 4vw;
    }

    .text-list {
        display: flex;
        padding: 0 3vw;
        border-top-style: none;
        margin-bottom: 0;
        padding-top: 3vw;
        padding-bottom: 6vw;

        .left {
            width: 50%;

            p {
                letter-spacing: .03vw;
                padding-top: 0.5vw;
                font-size: 1vw;
                line-height: 1.5vw;
            }
        }

        .right {
            width: 50%;
            color: #000;
            letter-spacing: .03vw;
            font-family: PP Neue Montreal, sans-serif;
            font-size: 1.5vw;
            font-weight: 400;
            line-height: 2.5vw;
        }
    }

    .img-list {
        background: #fff;

        img {
            width: 100%;
            height: 100%;
            padding-top: 15vw;
            padding-bottom: 15vw;
        }
    }

    .nuxtPage {
        border-top: 1px solid #000;

        h2 {
            color: #000;
            border-radius: 0.5vw;
            align-items: center;
            margin-right: 0;
            padding: 0 1vw 0.1vw 0;
            font-family: PP Neue Montreal, sans-serif;
            font-size: 1.25vw;
            font-weight: 500;
            line-height: 1.25vw;
            text-decoration: none;
            display: flex;
            line-height: 20px;
            margin: 2vw 0 0 4vw;

            img {
                margin-left: 1vw;
            }
        }

        .nextprojectblock {
            cursor: pointer;
            border-radius: 2vw;
            align-items: center;
            margin-left: 4vw;
            margin-right: 4vw;
            text-decoration: none;
            display: flex;
            background-color: #000;
            margin-top: 2vw;
            padding: 3vw 4vw;
            max-width: 100%;
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 4vw;

            .left {
                display: flex;

                img {
                    width: 6vw;
                }

                p {
                    color: #fff;
                    flex-direction: row;
                    flex: 0 auto;
                    align-items: center;
                    font-family: PP Neue Montreal, sans-serif;
                    font-size: 2.5vw;
                    font-weight: 400;
                    display: flex;
                    padding-left: 5vw;
                }
            }

            .right {
                display: flex;

                p {
                    color: #fff;
                    padding: 0.75vw 1vw;
                    border: 1px solid #000;
                    border-radius: 6px;
                    margin-right: 0.75vw;
                    cursor: pointer;
                    color: #fff;
                    font-size: 1.5vh;
                    border: #fff 1px solid;
                }
            }
        }
    }
}

@media screen and (max-width: 768px) {
    .box {
        width: 100%;
        background-color: #fff;
        box-sizing: border-box;
    }

    .contetn {
        box-sizing: border-box;
    }

    .banner {
        box-sizing: border-box;
        height: 38vw;
        border-radius: 3vw;
        padding: 2vw 4vw;
        height: 47vh;

        img {
            width: 100%;
            height: 100%;
            box-sizing: border-box;
            border-radius: 2vw;
        }
    }

    .banner-text {
        margin-top: 3vw;
        margin-bottom: 3vw;
        font-size: 6vw;
        line-height: 8vw;
        padding: 0 4vw;
        border-bottom: 1px solid #000;
    }

    .text-list {
        display: flex;
        flex-direction: column;
        border-top-style: none;
        margin-bottom: 0;
        padding-top: 3vw;
        padding-bottom: 6vw;

        .left {
            padding: 4vw 3vw;
            border-bottom: 1px solid #000;

            p {
                width: 100%;
                color: #000;
                letter-spacing: .2vw;
                font-size: 3vw;
                line-height: 4vw;
            }
        }

        .right {
            border-bottom: 1px solid #000;
            letter-spacing: .25vw;
            margin-bottom: 8vw;
            padding-left: 0;
            font-size: 4vw;
            line-height: 6vw;
            padding: 4vw 3vw;
        }
    }

    .img-list {
        background: #fff;

        img {
            width: 100%;
            height: 100%;
            padding-top: 15vw;
            padding-bottom: 15vw;
        }
    }

    .nuxtPage {
        border-top: 1px solid #000;

        h2 {
            color: #000;
            border-radius: 0.5vw;
            align-items: center;
            margin-right: 0;
            padding: 0 1vw 0.1vw 0;
            font-family: PP Neue Montreal, sans-serif;
            font-size: 4vw;
            font-weight: 500;
            line-height: 1.25vw;
            text-decoration: none;
            display: flex;
            line-height: 20px;
            margin: 2vw 0 0 4vw;

            img {
                margin-left: 1vw;
                max-width: 100%;
            }
        }

        .nextprojectblock {
            cursor: pointer;
            border-radius: 2vw;
            align-items: center;
            margin-left: 4vw;
            margin-right: 4vw;
            text-decoration: none;
            display: flex;
            background-color: #000;
            margin-top: 2vw;
            padding-top: 8vw;
            padding-bottom: 8vw;
            max-width: 100%;
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 4vw;
            .left {
                display: flex;

                img {
                    width: 10vw;
                    margin-left: 10vw;
                }

                p {
                    width: 60vw;
                    color: #fff;
                    padding-top: 1vw;
                    line-height: 2vw;
                    font-size: 6vw;
                    color: #fff;
                    flex-direction: row;
                    flex: 0 auto;
                    align-items: center;
                    font-family: PP Neue Montreal, sans-serif;
                    font-weight: 400;
                    display: flex;
                    justify-content: center;
                }
            }

            .right {
                display: none;

                p {
                    color: #fff;
                    padding: 0.75vw 1vw;
                    border: 1px solid #000;
                    border-radius: 6px;
                    margin-right: 0.75vw;
                    cursor: pointer;
                    color: #fff;
                    font-size: 1.5vh;
                    border: #fff 1px solid;
                }
            }
        }
    }
}
</style>