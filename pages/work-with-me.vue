<template>
    <div class="box">
        <div class="banner">
          Brands Driving by Design
        </div>
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
<style scoped>
.box{
    background-color: #f3f3f3;
}

@media screen and (min-width: 768px) {
    .banner{
    padding-top: 3vw;
    margin-left: 2vw;
    padding-bottom: 3vw;
    color: #000;
    letter-spacing: 0;
    margin-top: 0;
    font-size: 9vw;
    font-weight: 500;
    line-height: 11vw;
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
      }
    }
  }
}
@media screen and (max-width: 768px) {
    .banner{
        width: auto;
    margin-left: 4vw;
    font-size: 22vw;
    line-height: 20vw;
    color: #000;
    border-top: 1px solid #000;
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