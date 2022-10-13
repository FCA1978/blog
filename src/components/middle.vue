<template>
  <div class="middle">
    <h2 className="message"><span @click="jumpClick()">了解真相，你才能获得真正的自由</span></h2>    
  </div>      
</template>
<script lang="ts" setup>
  import axios from 'axios'

  axios.get('http://139.159.245.209:5000/api/WeatherForecast/get')
  .then(function (response) {
    // handle success
    console.log(response);
  })
  .catch(function (error) {
    // handle error
    console.log(error);
  })
  .then(function () {
    // always executed
  });

  const jumpClick = () => window.open('https://juejin.cn/user/4222578354040471/posts','_blank')
</script>
<style lang="scss" scoped>
.middle {
  display: flex;
  align-items:center;
  justify-content: center;
  margin-top: 80px;
  color: var(--vp-c-brand);
  cursor: pointer;
  text-decoration: underline;
  &:hover {
    color: var(--vp-c-brand-dark);
  } 
}
</style>
