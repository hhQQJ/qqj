<template>
  <NuxtLayout>
    <Header /> <!-- 引入头部组件 -->
    <NuxtPage class="page"/>
   <Footer/>
  </NuxtLayout>
</template>
<script setup>
import Footer from '~/components/Footer.vue';
import Header from '~/components/Header.vue';
</script>
<style>
@media screen and (min-width: 768px) {
  .page{
  margin-top: 95px;
}
}
@media screen and (max-width: 768px) {
  .page{
    margin-top: 42.5px 
}
}
* {
    margin: 0;
    padding: 0;
    border: 0;
    font-size: 100%;
    font-weight: normal;
    font-style: normal;
    line-height: 1;
    vertical-align: baseline;
    list-style: none;
}
a {
  color: inherit;
  text-decoration: none;
}
</style>