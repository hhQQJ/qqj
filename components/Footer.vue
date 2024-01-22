<template>
    <div class="footer">
        <div class="left">
            <p></p>
            <p>Studio DMCG Inc © 2024</p>
        </div>
        <div class="right">
            <p class="animate__animated" :class="{'animate__fadeOutUp': !redBook, 'animate__fadeInUp': redBook}" @click="clickRedBook"  >
                小红书
            </p>
            <p class="animate__animated" :class="{'animate__fadeInDown': !redBook, 'animate__fadeOutDown': redBook}" @click="clickRedBook" >@小红书</p>
        </div>
        <div class="right">
            <p class="animate__animated" :class="{'animate__fadeOutUp': !concat, 'animate__fadeInUp': concat}" @click="clickConact"  >
                联系方式
            </p>
            <p class="animate__animated" :class="{'animate__fadeInDown': !concat, 'animate__fadeOutDown': concat}" @click="clickConact" >wx:123123</p>
        </div>
        <div class="right">
            <p class="animate__animated" :class="{'animate__fadeOutUp': !wechat, 'animate__fadeInUp': wechat}" @click="clickWeChat"  >
                微信
            </p>
            <p class="animate__animated" :class="{'animate__fadeInDown': !wechat, 'animate__fadeOutDown': wechat}" @click="clickWeChat" >123123</p>
        </div>
        <div class="right">
            <p class="animate__animated" :class="{'animate__fadeOutUp': !phone, 'animate__fadeInUp': phone}" @click="clickPhone"  >
                电话
            </p>
            <p class="animate__animated" :class="{'animate__fadeInDown': !phone, 'animate__fadeOutDown': phone}" @click="clickPhone" >123123</p>
        </div>

    </div>
</template>
<script setup>
import "animate.css"
const redBook = ref(true)
const concat = ref(true)
const wechat = ref(true)
const phone = ref(true)

const clickRedBook = () =>{
    redBook.value = !redBook.value
}
const clickConact = () =>{
    concat.value = !concat.value
}
const clickWeChat = () =>{
    wechat.value = !wechat.value
}
const clickPhone = () =>{
    phone.value = !phone.value
}
</script>
<style lang="scss" scoped>
@media screen and (min-width: 768px) {
    .footer {
        display: flex;
        border-top: 1px solid #000;
        padding-top: 0;
        transition: transform .2s;
        height: 300px;
        align-items: center;
        padding: 0 60px;
        background: #f3f3f3;

        .left {
            display: flex;
            width: 60%;

            p:nth-child(1) {
                width: 1vw;
                height: 1vw;
                min-height: 1vw;
                min-width: 1vw;
                background-color: #000;
                border-radius: 20px;
                margin-right: 0.75vw;
                display: flex;
                overflow: visible;
            }

            p:nth-child(2) {
                color: #000;
                font-size: 1.25vw;
                font-weight: 500;
            }
        }

        .right {
            display: flex;
            flex-direction: column;
            justify-content: space-between;

            p {
                color: #000;
                font-size:1.25vw;
                font-weight: 500;
                cursor: pointer;
                position: relative;
                width: 10vw;
                text-align: end;
                img{
                    position: absolute;
                    width: 120px;
                    height: 120px;
                    top: -130px;
                    left: 0;
                    border-radius: 10px;
                }
            }
        }
    }
}

@media screen and (max-width: 768px) {
    .footer {
        border-top: 1px solid #000;
        margin-top: 2vw;
        transition: transform .2s;
        padding-left: 4vw;
        padding-bottom: 2vw;
        display: flex;
        flex-direction: column;

        .left {
            display: flex;
            padding: 5vw 0;

            p:nth-child(1) {
                width: 3vw;
                height: 3vw;
                min-height: 3vw;
                min-width: 3vw;
                margin-right: 2vw;
                padding-top: 0;
                display: flex;
                background-color: #000;
                border-radius: 20px;
            }

            p:nth-child(2) {
                width: 100%;
                justify-content: flex-start;
                padding-left: 0;
                line-height: 4vw;
                font-size: 4vw;
            }
        }

        .right {


            p {
                width: 100%;
                justify-content: flex-start;
                padding-left: 0;
                line-height: 4vw;
                border-top-style: none;
                margin-right: 2vw;
                padding-top: 0;
                padding-bottom: 2vw;
                font-size: 4vw;
                position: relative;
                img{
                    position: absolute;
                    width: 60px;
                    height: 60px;
                    top: -70px;
                    left: 0;
                    border-radius: 10px;
                }
            }
        }
    }
}
</style>