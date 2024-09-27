<script>
  export default {
    data() {
      return {
        columnNum: null,
        rowNum: null,
        startVisibility: true,
        makeFieldVisibility: false,
      }
    },

    methods: {
      changeField() {
        this.startVisibility = false;
        this.makeFieldVisibility = true;
      }
      
    }
  }
</script>

<template>
  <div class="container">
    <h1 class="main_header">Конструктор схем</h1>
    <div class="frame" >
      <div class="img_box" v-if="startVisibility">
        <p class="text">Создай свой уникальный дизайн</p>
        <button class="start" @click="changeField()">Начать работу</button>
      </div>
      <div class="makeField" v-if="makeFieldVisibility">
        <p>Введите размеры поля</p>
        <input class="" type="text" value="Строки">
        <span>x</span>
        <input type="text" value="Столбцы">
      </div>
    </div>
  </div>
  
</template>

<style scoped>

  .container {
    position: relative;
    display: flex;
    flex-wrap: wrap;
    width: 100vw;
    height: 80vh;
    max-width: 920px;
    max-height: 651px;
    justify-content: center;
    align-items: center;
    color: #2b281d;
  }

  .container > .main_header {
    position: absolute;
    top: -7%;
  }

  .frame {
    background: #647c56;
    border: 10px solid #c7b598;
    border-radius: 15px;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  

  .main_header {
    font-size: 7vh;
    text-align: center;
    color: #2b281d;
    background-color: #647c56;
    padding-left: 15px;
    padding-right: 15px;
    text-transform: uppercase;
    order: 0;
  }

  .img_box {
    background-image: url(./assets/bg1.png);
    width: 97%;
    height: 95%;
    max-width: 900px;
    max-height: 630px;
    border-radius: 5px;
    
  }

  p {
    font-size: 2vw;
    text-align: right;
    margin-top: 10%;
    margin-right: 5%;
  }

  .start {
    background-color: transparent;
    border: 3px solid #647c56;
    border-radius: 5px;
    width: 25%;
    height: 8%;
    margin-left: 55%;
    margin-top: 15px;
    font-family: Georgia, serif;
    font-size: 18px;
  }

  .start:hover {
    background-color: #c7b598;
    border: 3px solid #c7b598;
  }
</style>
