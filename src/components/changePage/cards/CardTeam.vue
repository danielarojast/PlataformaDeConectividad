<template>
    <div class="card" style="width: 18rem;">
        <div class="card-body">
            <div class="card-top">
              <div class="card-top-title">
                <h5 class="card-title" style="margin:0;"><i :class="props.icon"></i> {{props.title}}</h5>
                <div style="margin:0;"> 
                  <button style="margin:0; padding: 0;"><i class="bi bi-star" style="margin:5px;"></i></button>
                  <button style="margin:0; padding: 0;"><i class="bi bi-three-dots-vertical" style="margin:8px;"></i></button>
                </div>
              </div>

              <p class="card-text">{{props.description}}</p>
            </div>
            <div class="card-bottom">
              <img src="../../../assets/images/people.png" alt="" style="margin:0;">
              <div style="margin:0;">
                <button class="btn1">{{props.button1}}</button>
                <button class="btn2">{{props.button2}}</button>
              </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
    interface IProps {
        icon: string
        title: string
        description: string
        button1: string
        button2: string
    }

    const props = defineProps<IProps>()
    console.log(props)
</script>

<style lang="scss" scoped>
  *{
    margin : 0;
    padding: auto;
    background-color: white;
  }
  i{
    border-radius: 100% 100%;
    padding: 8px;
  }
  button :hover{
    transform: translateY(-1px); /* Eleva el botón */
    box-shadow: 0 2px 8px rgba(131, 64, 159, 0.2); /* Sombra para el efecto de elevación */
  }
  .card-body {
    font-size: 90%;
    color: rgb(86, 85, 85);
    background-color: white;
  }
  .card {
    padding: 0;
    margin: 4px; 
    border: #e1d2d2;
    box-shadow: 0px 1px 10px #e1d2d2;
    flex: 1 1 310px; /* Tamaño mínimo de 200px, y permite que crezca */
    max-width: 100%; /* Las tarjetas no excederán el ancho del contenedor */
    
    box-sizing: border-box;
  }
  .card-body {
    margin: 0; 
    display: flex;
    flex-direction: column;
    border-radius: 50px;
  }
  .card-top {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    width: 100%;
  }
  .card-top-title {
    padding: 10px 0;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    width: 100%;
  }
  .card-bottom {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    margin-top: 10px;
    width: 100%;
    padding: 10px 0;
  }

  .card-bottom button {
    font-weight:500;
    border-radius: 5px;
    padding: 5px 20px;
    margin-left: 10px;
  }
  .btn1 {
    background-color: #7166ee35;
    color: #7266ee;
  }
  .btn2 {
    background-color: rgba(102, 231, 238, 0.221);
    color: #06b4bd;
  }
</style>