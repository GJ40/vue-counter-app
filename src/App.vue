<!-- Composition API - use setup keyword in script tag -->
 <!--
<script setup>

  import {ref} from "vue";
  const count = ref(0);

  //console.log(count);
  const addCount = () => {
    count.value += 1;
  }
  const subCount = () => {
    count.value -= 1;
  }
</script>
-->

<!-- Options API wihtout 'setup' keyword -->
<script>
  export default{
    data(){
      return{
        count: 0
      }
    },
    methods: {
      addCount(){
        this.count = this.count + 1
      },
      subCount(){
        this.count = this.count - 1
      }
    }
  }
</script>

<template>
  <main>
    <div>
      <h4>The current count is....</h4>
      <h1>
        {{ count }}
      </h1>
      <button @click="subCount()">-</button>
      <button @click="addCount()">+</button>
    </div>
  </main>
</template>

<style scoped> /* scoped - adds style only to this component/file */
  main{
    background-color: antiquewhite;
    height: 100vh;
    width: 100vw;
    display: flex;
    align-items: center;
    justify-content: center;
    color: slategray;
    font-size: 2rem;
  }
  div{
    text-align: center;
  }
  button{
    margin-inline: 20px;
    border: none;
    font-size: 1.5rem;
    outline: none;
    background-color: tomato;
    width: 80px;
    border-radius: 10px;
  }
  button:hover{
    background-color: hsl(9, 100%, 70%);
  }
  button:active{
    background-color: hsl(9, 100%, 54%);
  }
</style>
