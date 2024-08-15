<template>
    <div class="card" style="width: 18rem;">
        <div class="card-body">
            <div class="mainMenu">
                <button ><i class="bi bi-three-dots-vertical" style="margin:8px;"></i></button>
            </div>
            <div class="content-card">
                <div>
                    <img src="../../../assets/images/perfil.png" alt="" style="margin:0;">
                    <div style="margin:15px 0; ">
                        <p><b>{{props.name}}</b></p>
                        <p>{{props.profesion}}</p>
                    </div>
                </div>
                <div class="btn-first">
                    <button class="btn1">{{props.button1}}</button>
                    <button class="btn2">{{props.button2}}</button>
                </div>
                <div class="content-info">
                    <div> 
                      <p><b>{{props.nProjects}}</b></p>
                      <p>project</p></div>
                    <div> 
                      <p><b>{{props.nTasks}}</b> </p>
                      <p>Tasks</p>
                    </div>
                    <div> 
                      <p><b>{{props.nConnections}}</b></p>
                      <p>Connections</p>
                    </div>
                </div>
                <div class="btn-second">
                  <button class="btn3"><i class="bi bi-person-check" style="background-color: #7266ee; color: white;" ></i> Connected</button>
                  <button class="btn4"><i class="bi bi-envelope" style="background-color: #c2beed;"></i></button>
                </div>
            </div>
            
        </div>
    </div>
</template>

<script setup lang="ts">
    interface IProps {
      photo: string
      name: string
      profesion: string
      button1: string
      button2: string
      nProjects: string
      nConnections: string
      nTasks: string
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
    flex: 1 1 290px; /* Tamaño mínimo de 200px, y permite que crezca */
    max-width: 100%; /* Las tarjetas no excederán el ancho del contenedor */
    box-sizing: border-box;
  }
  .card-body {
    display: flex;
    flex-direction: column;
    border-radius: 50px;
  }

  .mainMenu {
  display: flex;
  justify-content: flex-end;
  }

  .content-card {
  display: flex;
  flex-direction: column; /* Alinea los hijos en columna */
  justify-content: center;
  align-items: center;
  }

  .content-card div img{
    border-radius: 200%;
    width: 100px;
    height: 100px;
  }

  .btn-first {
    margin-bottom: 15px;
    display: flex;
    justify-content: space-between;
    gap: 10px;
  }

  .btn-first button {
    padding: 0 30px;
  }

  .btn1 {
    background-color: #ff914d4e ;
    color: #ff914d;
    padding: 0 30px ;
  }
  
  .btn2 {
    background-color: #064cbd3c;
    color: #064cbd;
    }

  .content-info{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    gap: 20px;
    margin: 10px 0 20px 0;
  }
  .content-info div{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
  }
  .btn-second{
    display: flex;
    justify-content: space-between;
    gap: 10px;
  }
  .btn3{
    background-color: #7266ee; 
    color: white;
  }
  .btn3:hover{
    transform: translateY(-1px); /* Eleva el botón */
    box-shadow: 0 2px 8px rgba(131, 64, 159, 0.2); /* Sombra para el efecto de elevación */
  }
  .btn4{
    background-color: #c2beed; 
    color: white;
  }
  .btn4:hover{
    transform: translateY(-1px); /* Eleva el botón */
    box-shadow: 0 2px 8px rgba(131, 64, 159, 0.2); /* Sombra para el efecto de elevación */
  }
  .btn4 i{
    color: rgb(83, 83, 83)
  }
</style>