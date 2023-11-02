<template>
  <div>
  <button @click="cun">存</button>
  <button @click="qu">取</button>
  <button @click="shan">删</button>
  <h2>{{ this.a }}</h2>
  ——————————————————————————————————————
  <zi :b="b"></zi>
  <button @click="zii">加</button>
  <button @click="jian">减</button>
  </div>
</template>

<script>
import  zi  from '../components/zi.vue' ;
export default {
 data() {
   return {
    a:'哈',
    b:1
   };
 },
 methods: {
  cun(){
    localStorage.setItem('list', '哈哈哈')
  },
  qu(){
   this.a=localStorage.getItem('list')
  },
  shan(){
    localStorage.clear()
  },
  zii(){
    this.b++
  },
  jian(){
    this.b--
  }
 },
 computed: {},
 filters: {},
 watch: {},
 components:{
  zi
 }
};
</script>

<style lang="scss" scoped>

</style>