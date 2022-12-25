<template>
<div >
  <button @click="del">press</button>
<!--  <ul class="menu" v-for="(item,index) in items" :key="index">-->
<!--    <li>{{item}}</li>-->
<!--  </ul>-->
<!--  <button >alternative</button>-->

  <h3 v-if="items.length >= 2">Vue неплох</h3>
  <h3 v-else>Полное говно</h3>
</div>
</template>

<script>
export default {
  name: "test",

  data(){
    return{
      items:['first','second']
    }
  },
  methods:{
    del(){
      this.items.length
      this.items.splice(0,this.items.length)
      console.log(this.items.length)
    }
  }

}
</script>

<style scoped>

button{
  display: block;
  width: 10%;
  margin:auto;
}

.menu{
  display: block;
  width: 20%;
  box-shadow: inset 0 0 1px 1px black;
  margin:auto
}
</style>