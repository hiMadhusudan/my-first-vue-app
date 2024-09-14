<template>
  <div class="container">
    <div class="image">
      <img :src="imgUrl" alt="img">
    </div>
    <input type="text" :placeholder="inpText" v-model="inputUrl">
    <button @click="setUrl">{{ btnText }}</button>
  </div>
  
</template>

<script>
  export default {
    name: 'App',
    data () {
      return {
        inpText : "Enter image url",
        btnText : "Load Image",
        inputUrl : "",
        imgUrl : "https://pbs.twimg.com/media/GXEW8IJW4AAgNR0?format=jpg&name=large"
      }
    },
    methods: {
      setUrl () {
        this.imgUrl = this.inputUrl
        console.log(this.url)
      }
    }
  }
</script>

<style>
  .container {
    display: flex;
    flex-direction: column;
    height: 80vh;
    width: 60vh;
    border:4px ridge rgb(14, 69, 109);
    margin: 9vh auto;
    padding: 10px;
    background-color: rgb(42, 70, 121);
  }

  .image {
    height: 90%;
    width: 100%;
    /* border: 1px solid black; */
    background-color: white;
  }

  .image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .container button {
    text-align: center;
    font-size: 20px;
    margin: 10px 0;
    color: antiquewhite;
    background-color: rgb(32, 102, 167);
    border: none;
    padding: 5px;
  }
  .container button:hover {
    background-color: rgb(0, 97, 188);
    cursor: pointer;
  }
</style>