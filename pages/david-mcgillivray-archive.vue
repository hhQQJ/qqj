<template>
    <div class="box">
        <div class="banner">
        
        </div>
        <div class="w-dyn-list">
            <div class="item">
                <img src="https://assets-global.website-files.com/6302c0b32d2f070ebc81e898/6302c0da09a32204a743d6b2_Group%201135.jpg"
                    alt="">
            </div>
            <div class="item">
                <img src="https://assets-global.website-files.com/6302c0b32d2f070ebc81e898/6302c12824ba58804b2e4784_Group%201188.jpg"
                    alt="">
            </div>
            <div class="item">
                <img src="https://assets-global.website-files.com/6302c0b32d2f070ebc81e898/6302c11979dc34ca0a938a51_Group%201136.jpg"
                    alt="">
            </div>
            <div class="item">
                <img src="https://assets-global.website-files.com/6302c0b32d2f070ebc81e898/6302c131c32fa75d5e1c92b6_Group%201150.jpg"
                    alt="">
            </div>
            <div class="item">
                <img src="https://assets-global.website-files.com/6302c0b32d2f070ebc81e898/6302c577f01cad098c80ee67_allhandsthumb2%201.jpg"
                    alt="">
            </div>
            <div class="item">
                <img src="https://assets-global.website-files.com/6302c0b32d2f070ebc81e898/6302c58137665d759090f233_wildpsotings.jpg"
                    alt="">
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@media screen and (min-width: 768px) {
    .banner {
        align-items: flex-start;
        padding-right: 3vw;
        border-bottom-style: none;
        justify-content: space-between;
        border-bottom: 1px #000;
        flex-direction: row;
        padding-top: 3vw;
        padding-bottom: 3vw;
        display: flex;
        font-size: 10.75vw;
    }

    .w-dyn-list {
        width: 100%;
        display: flex;
        flex-wrap: wrap;

        .item {
            width: 28%;
            padding-left: 10px;
            padding-right: 10px;
            height: 31vw;
            border-radius: 2vw;
            margin: 1vw 1vw 3vw;
            padding-top: 1.5vw;
            padding-left: 2vw;
            cursor: pointer;

            img {
                width: 100%;
                height: 100%;
                border-radius: 2vw;
            }
        }
    }
}

@media screen and (max-width: 768px) {
    .banner {
        border-bottom-style: none;
        justify-content: space-between;
        padding-top: 6vw;
        margin-bottom: 4vw;
        padding-bottom: 7vw;
        display: flex;
        width: auto;
        margin-left: 4vw;
        font-size: 22vw;
        line-height: 20vw;
    }

    .w-dyn-list {
        display: flex;
        flex-direction: column;
        align-items: center;

        .item {
            margin-bottom: 5vw;
            padding-top: 2vw;
            width: 88vw;
            height: 88vw;
            border-radius: 2vw;

            img {
                width: 100%;
                height: 100%;
                border-radius: 2vw;
            }
        }

    }
}

.box {
    background-color: #f3f3f3;
}</style>