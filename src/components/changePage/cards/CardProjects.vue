<template>
    <div class="card" style="width: 18rem;">
        <div class="card-body">
            <div class="card-top">
              <div class="card-top-title">
                <div class="card-title-left">
                    <div class="card-title-icon">
                        <p><i :class="props.icon" ></i></p>
                    </div>
                    <div class="card-title-right">
                        <h5 class="card-title" style="margin:0;"> {{props.title}}</h5>
                        <p>Client: {{props.client}}</p>
                    </div>
                </div>
                <div style="margin:0;"> 
                  <button style="margin:0; padding: 0;"><i class="bi bi-three-dots-vertical" style="margin:8px;"></i></button>
                </div>
              </div>
              <p class="card-text">{{props.description}}</p>
            </div>
            <div class="card-bottom">
              <div class="botton-conatiner-one">
                <p><b>All Hours:</b> {{props.hours}}</p>
                <p style="background-color: #d7f9e9; color:#00bf63; padding: 2px; border-radius: 5px;">28 Days left</p>
              </div>
              <div class="botton-conatiner-second">
                <div class="botton-conatiner-second-one">
                    <p>Task: {{props.task}}</p>
                    <p>{{props.percentage}}% Complete</p>
                </div>
                <div class="botton-conatiner-second-two">
                    <div class="progress progress-color" role="progressbar" aria-label="Basic example" :aria-valuenow="props.percentage" aria-valuemin="0" aria-valuemax="100">
                        <div :style="{ width: props.percentage + '%' }" class="progress-bar custome-color"></div>
                    </div>
                </div>
                
              </div>
              <div class="botton-conatiner-third">
                <div class="botton-conatiner-third-one">
                    <img src="../../../assets/images/people.png" alt="" style="margin:0;">
                    <p>280 members</p>
                </div>
                <i class="bi bi-star" style="margin:5px;">15</i>
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
        client: string
        hours: string
        task: string
        percentage: number
        members: string
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
    flex: 1 1 293px; /* Tamaño mínimo de 200px, y permite que crezca */
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
  .card-title-left {
    display: flex;
    flex-direction: row;
    width: 90%;
  }
  .card-title-icon i{
    padding: 8px;
    bottom: 0;
    background-color: rgb(246, 239, 246);
  }
  .card-title-right {
    width: 100%;
    padding: 1px;
    margin-left: 10px;
  }
  .card-bottom {
    width: 100%;
    padding: 10px;
    margin-top: 20px;
    border-top-style: solid;
    border-top-width: 1px;
    border-color: #e6e6ed;
  }

  .botton-conatiner-one{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    margin: 10px 0;
  }
  .botton-conatiner-one p{
    margin: 0;
  }

  .botton-conatiner-second-one{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    margin: 10px 0;
  }
  .botton-conatiner-second-one p{
    margin: 0;
  }

  .botton-conatiner-third{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    margin: 10px 0;
    }
  .botton-conatiner-third-one{
    display: flex;
    flex-direction: row;
    align-items: center;
    width: 100%;
    gap: 4px;
    }
    .botton-conatiner-third i{
        width: 40px;
    }
    .custome-color{
        background-color: #7266ee;
    }
    .progress-color{
        background-color: #e6e6ed;
    }
  
</style>