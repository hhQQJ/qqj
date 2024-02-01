<template>
  <div class="box">
    <div class="herosection">
      <div style="opacity: 1;" class="h2 herotype main">Projects</div>
    </div>
    <Projects/>
    <div class="aboutcontentcontainer">
      <div class="aboutcolumns">
        <div class="left">
          <p>1</p>
          <p>关于我</p>
        </div>
        <div class="right">
          I’m David McGillivray, and Studio DMCG Inc is my design practice. I’m a Creative Director and Designer based in
          New York, and have spent the last fourteen years helping to bring brands to life through strategic design.
        </div>
      </div>
      <div class="aboutcolumns">
        <div class="left">
          <p>2</p>
          <p>Who I am</p>
        </div>
        <div class="right">
          I’m David McGillivray, and Studio DMCG Inc is my design practice. I’m a Creative Director and Designer based in
          New York, and have spent the last fourteen years helping to bring brands to life through strategic design.
        </div>
      </div>
      <div class="aboutcolumns">
        <div class="left">
          <p>3</p>
          <p>Who I am</p>
        </div>
        <div class="right">
          I’m David McGillivray, and Studio DMCG Inc is my design practice. I’m a Creative Director and Designer based in
          New York, and have spent the last fourteen years helping to bring brands to life through strategic design.
        </div>
      </div>
      <div class="aboutcolumns">
        <div class="left">
          <p>4</p>
          <p>Who I am</p>
        </div>
        <div class="right">
          I’m David McGillivray, and Studio DMCG Inc is my design practice. I’m a Creative Director and Designer based in
          New York, and have spent the last fourteen years helping to bring brands to life through strategic design.
        </div>
      </div>
      <div class="aboutcolumns">
        <div class="left">
          <p>5</p>
          <p>Who I am</p>
        </div>
        <div class="right">
          I’m David McGillivray, and Studio DMCG Inc is my design practice. I’m a Creative Director and Designer based in
          New York, and have spent the last fourteen years helping to bring brands to life through strategic design.
        </div>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import Projects from '~/components/projects.vue';
</script>
<style lang="scss" scoped>
.box {
  background: #f3f3f3;
}

@media screen and (min-width: 768px) {
  .herosection {
    color: #333;
    font-size: 14px;
    line-height: 20px;
    -webkit-text-size-adjust: 100%;
    text-rendering: optimizeLegibility;
    font-family: 'PP Neue Montreal', sans-serif;
    font-style: normal;
    font-weight: normal;
    -webkit-font-smoothing: antialiased;
    box-sizing: border-box;
    margin-top: 3vw;
    margin-bottom: 2vw;
    padding-left: 2vw;
    padding-right: 1.5vw;
    background-attachment: scroll !important;

    .herotype {
      -webkit-text-size-adjust: 100%;
      text-rendering: optimizeLegibility;
      font-style: normal;
      -webkit-font-smoothing: antialiased;
      box-sizing: border-box;
      border-radius: .5vw;
      align-items: center;
      margin-right: 0;
      padding: 0 1vw .1vw 0;
      font-family: PP Neue Montreal, sans-serif;
      font-weight: 500;
      text-decoration: none;
      display: flex;
      background-attachment: scroll !important;
      color: #000;
      margin-top: 0;
      opacity: 1;

      letter-spacing: -.3vw;
      font-size: 10.5vw;
      line-height: 12vw;
    }
  }

  .cardscroll {
    width: 100%;
    height: 50vw;
    flex-wrap: nowrap;
    margin-bottom: 1vw;
    padding-left: 0;
    display: flex;
    position: relative;
    overflow: hidden;
  }

  .marquee_track {
    color: #333;
    font-size: 14px;
    line-height: 20px;
    -webkit-text-size-adjust: 100%;
    text-rendering: optimizeLegibility;
    font-family: 'PP Neue Montreal', sans-serif;
    font-style: normal;
    font-weight: normal;
    -webkit-font-smoothing: antialiased;
    box-sizing: border-box;
    overflow-x: scroll;
    display: flex;
  }

  .cardlink {
    color: #000;
    border: 1px #000;
    margin-left: 1.5vw;
    margin-right: 1.5vw;
    text-decoration: none;
  }

  .w-inline-block {
    max-width: 100%;
    display: inline-block;
  }

  .cardimage {
    height: 100%;
    justify-content: center;
    align-items: center;
    display: flex;
  }

  .cardlink.hide {
    display: block;
  }

  .h3 {
    border-top: 1.5px #000;
    margin-left: 3vw;
    margin-right: 1.5vw;
    padding-top: 1.5vw;
    padding-left: 0;
    font-family: PP Neue Montreal, sans-serif;
    font-size: 1.5vw;
  }

  .tagblock {
    align-items: center;
    margin-top: 1.5vw;
    margin-bottom: 1vw;
    margin-left: 0;
    padding-left: 3vw;
    display: flex;
    position: relative;
    top: auto;
    bottom: 0%;
    left: 0%;
    right: auto;
  }

  .tag {
    color: #fff;
    border: 1px solid #000;
    border-radius: 6px;
    margin-right: 0.75vw;
    padding: 0.4vw 0.5vw;
    display: block;
  }

  .h4 {
    color: #000;
    font-family: PP Neue Montreal, sans-serif;
    font-size: 1.25vh;
    line-height: 1.25vh;
  }

  .projectcard.firstcard {
    width: 28vw;
    box-shadow: none;
    background-color: #e4e2dd;
    margin-left: 1vw;
    padding-bottom: 2vw;
  }

  .projectcard {
    width: 28vw;
    height: 30vw;
    background-color: #dedede;
    border-radius: 30px;
    flex-direction: column;
    justify-content: space-between;
    padding-top: 7vw;
    padding-bottom: 3vw;
    padding-left: 0;
    display: flex;
    box-shadow: 1px 1px 14px rgba(0, 0, 0, .09);
  }

  .projectcard.americanacard {
    width: 27vw;
    height: 32vw;
    background-color: #fff;
    justify-content: flex-end;
    padding-top: 4vw;
    padding-bottom: 3vw;
    display: flex;
  }

  .aboutcontentcontainer {
    padding-top: 3vw;
    .aboutcolumns {
      border-top: 1px solid #000;
      display: flex;
      padding: 0 3vw;
      .left {
        padding-top: 2vw;
        display: flex;
        width: 50%;

        p:nth-child(1) {
          width: 4vw;
          height: 4vw;
          outline-offset: 0px;
          background-color: rgba(0, 0, 0, 0);
          border: 1px solid #000;
          border-radius: 10vw;
          outline: 1px #000;
          display: flex;
          justify-content: center;
          align-items: center;
          color: #000;
          font-size: 1.5vw;
          font-weight: 400;
          margin-right: 2vw;
        }

        p:nth-child(2) {
          color: #000;
          text-align: right;
          margin-bottom: 0;
          margin-right: 6px;
          font-family: PP Neue Montreal, sans-serif;
          font-size: 1.75vw;
          font-weight: 500;
          line-height: 4vw;
        }
      }
      .right {
        width: 50%;
        color: #000;
        text-align: left;
        letter-spacing: .033vw;
        margin-bottom: 10%;
        font-family: PP Neue Montreal, sans-serif;
        font-size: 1.5vw;
        line-height: 2.5vw;
        padding-top: 3vw;
        text-align: end;
      }
    }
  }
}

@media screen and (max-width: 768px) {
  .herosection {
    color: #333;
    font-size: 14px;
    line-height: 20px;
    -webkit-text-size-adjust: 100%;
    text-rendering: optimizeLegibility;
    font-family: 'PP Neue Montreal', sans-serif;
    font-style: normal;
    font-weight: normal;
    -webkit-font-smoothing: antialiased;
    box-sizing: border-box;
    margin-top: 3vw;
    margin-bottom: 2vw;
    padding-left: 2vw;
    padding-right: 1.5vw;
    background-attachment: scroll !important;

    .herotype {
      -webkit-text-size-adjust: 100%;
      text-rendering: optimizeLegibility;
      font-style: normal;
      -webkit-font-smoothing: antialiased;
      box-sizing: border-box;
      border-radius: .5vw;
      align-items: center;
      margin-right: 0;
      padding: 0 1vw .1vw 0;
      font-family: PP Neue Montreal, sans-serif;
      font-weight: 500;
      text-decoration: none;
      display: flex;
      background-attachment: scroll !important;
      color: #000;
      margin-top: 0;
      opacity: 1;

      letter-spacing: -.3vw;
      font-size: 10.5vw;
      line-height: 12vw;
    }
  }

  .cardscroll {
    color: #333;
    font-size: 14px;
    line-height: 20px;
    -webkit-text-size-adjust: 100%;
    text-rendering: optimizeLegibility;
    font-family: 'PP Neue Montreal', sans-serif;
    font-style: normal;
    font-weight: normal;
    -webkit-font-smoothing: antialiased;
    box-sizing: border-box;
    width: 100%;
    flex-wrap: nowrap;
    padding-left: 0;
    display: flex;
    position: relative;
    overflow: hidden;
    height: 120vw;
    align-items: center;
    margin-bottom: 0;
    background-attachment: scroll !important;

    .marquee_track {
      color: #333;
      font-size: 14px;
      line-height: 20px;
      -webkit-text-size-adjust: 100%;
      text-rendering: optimizeLegibility;
      font-family: 'PP Neue Montreal', sans-serif;
      font-style: normal;
      font-weight: normal;
      -webkit-font-smoothing: antialiased;
      box-sizing: border-box;
      flex-wrap: nowrap;
      align-items: center;
      margin-top: 0;
      margin-bottom: 0;
      display: flex;
      overflow: scroll;
      height: 115vw;
      padding-top: 3vw;
      padding-bottom: 2vw;
      overflow-y: scroll;
      background-attachment: scroll !important;

      .cardlink {
        margin-left: 4vw;
        margin-right: 2vw;
        color: #000;
        border: 1px #000;
        text-decoration: none;
      }

      .w-inline-block {
        max-width: 100%;
        display: inline-block;
      }

      .projectcard.firstcard {
        width: 65vw;
        padding-top: 12vw;
        margin-right: 2vw;
        padding-bottom: 5vw;
        border-radius: 2vw;
        box-shadow: none;
        background-color: #e4e2dd;
        margin-left: 1vw;
      }

      .projectcard {
        height: 90vw;
        justify-content: space-between;
        flex-direction: column;
        padding-left: 0;
        display: flex;
        width: 65vw;
        padding-top: 12vw;
        margin-right: 2vw;
        padding-bottom: 5vw;
        border-radius: 2vw;
        box-shadow: none;
        background-color: #e4e2dd;
        margin-left: 1vw;

        .cardimage {
          width: 65vw;
          justify-content: center;
          display: flex;
          height: 100%;
          align-items: center;

          img {
            max-width: 100%;
            display: inline-block;
            vertical-align: middle;
          }
        }

        .div-block-5 {
          padding-bottom: 2vw;
          display: flex;
          margin-top: 2vw;
          padding-left: 5vw;

          .h3.extend {
            width: 100%;
            margin-left: 5vw;
          }

          .h3 {
            margin-right: 4vw;
            padding-top: 3vw;
            font-size: 4vw;
            border-top: 1.5px #000;
            padding-left: 0;
            font-family: PP Neue Montreal, sans-serif;
          }
        }

        .div-block-4 {
          padding-bottom: 2vw;
          display: flex;
          margin-top: 2vw;
          padding-left: 0;

          .h3.extend {
            width: 100%;
            margin-left: 5vw;
          }

          .h3 {
            margin-right: 4vw;
            padding-top: 3vw;
            font-size: 4vw;
            border-top: 1.5px #000;
            padding-left: 0;
            font-family: PP Neue Montreal, sans-serif;
          }
        }

        .div-block-2 {
          padding-left: 5vw;
        }

        .div-block-8 {
          margin-left: 6vw;
        }

        .div-block-6 {
          margin-left: 6vw;
        }

        .div-block-8 {
          margin-left: 5vw;
        }

        .div-block-7 {
          margin-left: 5vw;
        }

        .div-block-12 {
          width: 100%;
          display: flex;

          .div-block-2 {
            flex-wrap: wrap;
            display: flex;

            .tagblock {
              align-items: center;
              margin-bottom: 1vw;
              position: relative;
              top: auto;
              bottom: 0%;
              left: 0%;
              right: auto;
              margin-top: 0;
              padding-left: 0;
              padding-right: 4px;
              display: flex;

              .tag {
                border-radius: 3px;
                margin-right: 2vw;
                padding: 1vw 2vw;
                align-items: center;
                display: flex;
                color: #fff;
                border: 1px solid #000;

                .h4.hp {
                  font-size: 2.5vw;
                }

                .h4 {
                  color: #000;
                  font-family: PP Neue Montreal, sans-serif;
                  line-height: 1.25vh;
                }
              }
            }
          }
        }

        .div-block-2 {
          flex-wrap: wrap;
          display: flex;

          .tagblock {
            padding-right: 4px;
            display: flex;
            align-items: center;
            margin-bottom: 1vw;
            position: relative;
            top: auto;
            bottom: 0%;
            left: 0%;
            right: auto;
            color: #000;

            .tag {
              border-radius: 3px;
              margin-right: 2vw;
              padding: 1vw 2vw;
              display: flex;
              align-items: center;
              color: #fff;
              border: 1px solid #000;

              .h4.hp {
                font-size: 2.5vw;
              }

              .h4 {
                color: #000;
                font-family: PP Neue Montreal, sans-serif;
                line-height: 1.25vh;
              }
            }
          }
        }
      }
    }
  }
  .aboutcontentcontainer {
    padding-top: 3vw;
    .aboutcolumns {
      border-top: 1px solid #000;
      display: flex;
      flex-direction: column;
      padding-bottom: 3vw;
    padding-left: 4vw ;
      .left {
        height: 13vw;
        align-items: center;
        margin-top: 3vw;
        margin-bottom: 3vw;
        padding-top: 0;
        display: flex;
        p:nth-child(1) {
          width: 9vw;
          height: 9vw;
          opacity: 1;
          outline-offset: 0px;
          background-color: rgba(0, 0, 0, 0);
          border: 1px solid #000;
          border-radius: 100vw;
          outline: 2px #000;
          align-items: center;
          margin-right: 3vw;
          display: flex;
          margin-bottom: 0;
          display: flex;
          justify-content: center;
          align-items: center;
        }

        p:nth-child(2) {
          font-size: 6vw;
    font-weight: 500;
    line-height: 11vw;
    color: #000;
    text-align: right;
    margin-right: 6px;
    font-family: PP Neue Montreal, sans-serif;
        }
      }
      .right {
        letter-spacing: .25vw;
        font-size: 4vw;
        line-height: 6vw;
        padding-bottom: 40px;
      }
    }
  }
}

</style>