<!-- components/Header.vue -->
<template>
    <header style="z-index: 99999;" :class="{ 'scrolled': scrolled }" class="app-header">
        <NuxtLink to="/">
            <div class="left">
                <p></p>
                <p>www.dmcg.co</p>
            </div>
        </NuxtLink>
        <div class="center">Designing Digital Experiences & Identities</div>
        <div style="display: flex;height: 100%;align-items: center;">
            <div v-show="isProjects" class="right" style="margin-right: 10px; cursor: pointer;" @click="showDiv">
                <img class="rightimg1"
                    src="https://assets-global.website-files.com/62fd28cdd386f6a9d130721f/62fee8cbe0991374a0bc37c9_ProjectsIcon.svg"
                    alt="">
                <img class="rightimg2"
                    src="https://assets-global.website-files.com/62fd28cdd386f6a9d130721f/62ffcb314d13cfdd2b1604be_InfoIconWhite.svg"
                    alt="">
                <p>Projects</p>
            </div>
            <NuxtLink to="/work-with-me">
                <div class="right">
                    <img class="rightimg1"
                        src="https://assets-global.website-files.com/62fd28cdd386f6a9d130721f/62feea125290864330eeb1cb_InfoIcon.svg"
                        alt="">
                    <img class="rightimg2"
                        src="https://assets-global.website-files.com/62fd28cdd386f6a9d130721f/62ffcb314d13cfdd2b1604be_InfoIconWhite.svg"
                        alt="">
                    <p>info</p>
                </div>
            </NuxtLink>
        </div>

        <transition name="slide-down">
            <div v-if="isVisible" class="sliding-div">
                <!-- 内容 -->
                <div class="projects-header">
                    <div class="projects-left">
                        Selected Projects
                    </div>
                    <div style="cursor: pointer;" @click="showDiv" class="projects-right">
                        <img src="https://assets-global.website-files.com/62fd28cdd386f6a9d130721f/62fef381579c845bbaa75bab_Close.svg"
                            alt="">
                    </div>
                </div>
                <Projects />
            </div>
        </transition>
    </header>
</template>
  
<script setup>
import Projects from '~/components/projects.vue';
import { ref, onMounted,watchEffect } from 'vue';

const scrolled = ref(false);
const isProjects = ref(false);
const route = useRoute()
watchEffect(() => {
      if (route.href === '/work-with-me') {
        isProjects.value = true;
      } else {
        isProjects.value = false;
      }
    });
onMounted(() => {
    window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll);
});

const handleScroll = () => {
    scrolled.value = window.scrollY > 20;
};
const isVisible = ref(false)
const showDiv = () => {
    isVisible.value = !isVisible.value
}
</script>
  
<style lang="scss" scoped>
@media screen and (min-width: 768px) {
    .app-header {
        width: 100%;
        box-sizing: border-box;
        display: flex;
        padding-left: 2vw;
        justify-content: space-between;
        align-items: center;
        padding: 0 50px;
        height: 95px;
        position: fixed;
        top: 0;
        left: 0;
        background-color: #f3f3f3;
        /* 背景颜色 */
        transition: height 0.3s, border-color 0.3s;
        /* 添加高度和边框颜色过渡动画 */
        border-bottom: 1px solid transparent;
        /* 初始边框颜色为透明 */
        color: #000;

        .left {
            width: 200px;
            display: flex;
            align-items: center;
            cursor: pointer;
            padding: 0 20px;

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
            }
        }

        .left:hover {
            transition: background-color 0.5s ease;
            background-color: #000;
            height: 3vw;
            border-bottom-style: none;
            margin-top: 1vw;
            margin-bottom: 1vw;
            padding-top: 0;
            padding-bottom: 0;
            border-radius: 12px;

            p:nth-child(1) {
                width: 1vw;
                height: 1vw;
                min-height: 1vw;
                min-width: 1vw;
                background-color: hsl(132, 80%, 38%);
                border-radius: 20px;
                margin-right: 0.75vw;
                display: flex;
                overflow: visible;
            }

            p:nth-child(2) {
                color: #ffffff;
            }
        }

        .center {
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
        }

        .right {
            display: flex;
            align-items: center;
            padding-left: 1vw;
            cursor: pointer;

            .rightimg1 {
                width: 1.25vw;
                margin-right: 1vw;
            }

            .rightimg2 {
                display: none;
            }

            p {
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
            }
        }

        .right:hover {
            transition: background-color 0.5s ease;
            background-color: #000;
            height: 3vw;
            border-bottom-style: none;
            margin-top: 1vw;
            margin-bottom: 1vw;
            padding-top: 0;
            padding-bottom: 0;
            border-radius: 12px;
            padding-left: 1vw;

            .rightimg1 {
                display: none;
            }

            .rightimg2 {
                display: block;
                width: 1.25vw;
                margin-right: 1vw;
            }

            p {
                color: #fff;
            }
        }
    }

    .app-header.scrolled {
        height: 95px;
        /* 滚动后的高度 */
        border-bottom-color: #000;
        /* 滚动后的边框颜色 */
    }

    .sliding-div {
        width: 100%;
        height: 400px;
        background-color: white;
        transition: transform 0.5s ease-in-out;
        position: absolute;
        left: 0;
        top: 95px;

        .projects-header {
            display: flex;
            border-top: 1px solid #000;
            border-bottom-style: none;
            justify-content: space-between;
            align-items: center;
            align-items: center;
            box-sizing: border-box;
            padding: 1vw 0;
            .projects-left {
                font-size: 1.9vh;
                line-height: 2.5vw;
                padding: 1vw 3vw;
            }

            .projects-right {
                width: 2vw;
                height: 2vw;
                padding-right: 2vw
                img {
                    width: 100%;
                    height: 100%;
                }
            }
        }
    }

    .slide-down-enter-active,
    .slide-down-leave-active {
        transition: transform 0.5s ease-in-out;
    }

    .slide-down-enter,
    .slide-down-leave-to {
        transform: translateY(-100%);
    }
}


@media screen and (max-width: 768px) {
    .app-header {
        width: 100%;
        box-sizing: border-box;
        display: flex;
        padding-left: 2vw;
        justify-content: space-between;
        align-items: center;
        padding: 0 20px;
        height: 47.5px;
        background-color: #f3f3f3;
        /* 背景颜色 */
        transition: height 0.3s, border-color 0.3s;
        /* 添加高度和边框颜色过渡动画 */
        border-bottom: 1px solid transparent;
        /* 初始边框颜色为透明 */
        color: #000;
        position: fixed;
        top: 0;
        left: 0;

        .left {
            display: flex;

            p:nth-child(1) {
                line-height: 20px;
                -webkit-text-size-adjust: 100%;
                text-rendering: optimizeLegibility;
                font-style: normal;
                -webkit-font-smoothing: antialiased;
                color: #000;
                font-family: PP Neue Montreal, sans-serif;
                font-size: 1.5vw;
                font-weight: 500;
                box-sizing: border-box;
                background-color: #000;
                border-radius: 20px;
                overflow: visible;
                align-items: center;
                background-attachment: scroll !important;
                width: 3vw;
                height: 3vw;
                min-height: 3vw;
                min-width: 3vw;
                margin-right: 2vw;
                padding-top: 0;
                display: flex;
            }

            p:nth-child(2) {
                -webkit-text-size-adjust: 100%;
                text-rendering: optimizeLegibility;
                font-style: normal;
                -webkit-font-smoothing: antialiased;
                box-sizing: border-box;
                color: #000;
                border-radius: .5vw;
                align-items: center;
                margin-right: 0;
                padding: 0 1vw .1vw 0;
                font-family: PP Neue Montreal, sans-serif;
                font-weight: 500;
                line-height: 1.25vw;
                text-decoration: none;
                width: 100%;
                flex: 0 auto;
                justify-content: flex-start;
                padding-top: 0;
                padding-bottom: .5vw;
                padding-right: 0;
                font-size: 4vw;
                display: flex;
                background-attachment: scroll !important;
            }
        }

        .right {
            display: flex;

            .rightimg1 {
                font-size: 14px;
                line-height: 20px;
                -webkit-text-size-adjust: 100%;
                text-rendering: optimizeLegibility;
                font-family: 'PP Neue Montreal', sans-serif;
                font-style: normal;
                font-weight: normal;
                -webkit-font-smoothing: antialiased;
                color: #000;
                box-sizing: border-box;
                border: 0;
                vertical-align: middle;
                max-width: 100%;
                display: inline-block;
                width: 3.2vw;
                margin-right: 2vw;
                background-attachment: scroll !important;
            }

            .rightimg2 {
                display: none;
            }
        }
    }


    .app-header .center {
        display: none;
        /* 移动端隐藏中部分 */
    }

    .app-header.scrolled {
        height: 47.5px;
        /* 滚动后的高度 */
        border-bottom-color: #000;
        /* 滚动后的边框颜色 */
    }

    .sliding-div {
        width: 100%;
        height: 400px;
        background-color: white;
        transition: transform 0.5s ease-in-out;
        position: absolute;
        left: 0;
        top: 42.5px;

        .projects-header {
            display: flex;
            border-top: 1px solid #000;
            border-bottom-style: none;
            justify-content: space-between;
            align-items: center;
            align-items: center;
            box-sizing: border-box;

            .projects-left {
                font-size: 3vw;
                line-height: 2.5vw;
                padding: 1vw 3vw;
            }

            .projects-right {
                width: 5vw;
                padding-right: 7vw;
                padding-top: 3vw;

                img {
                    width: 100%;
                    height: 100%;
                }
            }
        }
    }

    .slide-down-enter-active,
    .slide-down-leave-active {
        transition: transform 0.5s ease-in-out;
    }

    .slide-down-enter,
    .slide-down-leave-to {
        transform: translateY(-100%);
    }
}</style>
  