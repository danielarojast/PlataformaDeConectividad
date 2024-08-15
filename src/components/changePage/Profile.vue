<template>
    <div class="main-container">
        <div class="container-left">
            <div class="Left-top content">
                <p class="subTitle">ABOUT</p>
                <p><i class="bi bi-person-circle"></i> <b>Full name:</b> John Doe</p>
                <p><i class="bi bi-envelope-fill"></i> <b>Status:</b> active</p>
                <p><i class="bi bi-geo-alt"></i> <b>Role:</b> Developer</p>
                <p><i class="bi bi-clock"></i> <b>Country:</b> COL</p>
                <p><i class="bi bi-calendar-event"></i> <b>Language:</b> English</p>
                
                <p class="subTitle">CONTACTS</p>
                <p><i class="bi bi-calendar-event"></i> <b>Language:</b> English</p>
                <p><i class="bi bi-calendar-event"></i> <b>Language:</b> English</p>
                <p><i class="bi bi-calendar-event"></i> <b>Language:</b> English</p>

                <p class="subTitle">TEAMS</p>
                <p><i class="bi bi-calendar-event"></i> <b>Language:</b> English</p>
                <p><i class="bi bi-calendar-event"></i> <b>Language:</b> English</p>
            </div>
            <div class="Left-bottom content">
                <p class="subTitle">OVERVIEW</p>
                <p><i class="bi bi-calendar-event"></i> <b>Language:</b> English</p>
                <p><i class="bi bi-calendar-event"></i> <b>Language:</b> English</p>
                <p><i class="bi bi-calendar-event"></i> <b>Language:</b> English</p>
            </div>
        </div>

        <div class="container-right">
            <div class="Right-first content">
                <h5><i class="bi bi-geo-alt"></i> Activity Timeline</h5>
                <div>
                    <p><b>12 Invoices have been paid</b></p>
                    <p>invoices have been pain to the company</p>
                    <img src="../../assets/images/people.png" alt="invoices">
                </div>
                <div>
                    <p><b>Client Meeting</b></p>
                    <p>Project meeting with the client</p>
                    <img src="../../assets/images/people.png" alt="invoices">
                </div>
                <div>
                    <p><b>Create a new project for client</b></p>
                    <p>6 team members in a project</p>
                    <img src="../../assets/images/people.png" alt="invoices">
                </div>
            </div>
            <div class="Right-second content">
                <div class="content">
                    <h5>Connection</h5>
                    <div class="card-connection">
                        <img src="../../assets/images/perfil.png" alt="invoices" width="50px" style="border-radius: 100%;">
                        <div>
                            <p><b>Name</b></p>
                            <p>45 connections</p>
                        </div>
                    </div>

                </div>
                <div class="content">
                    <h5>Teams</h5>
                    <div class="card-connection">
                        <img src="../../assets/images/perfil.png" alt="invoices" width="50px" style="border-radius: 100%;">
                        <div>
                            <p><b>Name</b></p>
                            <p>45 connections</p>
                        </div>
                    </div>
                </div>
            </div> 
            <div class="Right-third content">
                <h5>Project List</h5>
                <div class="card-connection">
                        <img src="../../assets/images/perfil.png" alt="invoices" width="50px" style="border-radius: 100%;">
                        <div>
                            <p><b>Name</b></p>
                            <p>45 connections</p>
                        </div>
                    </div>
            </div>
        </div>
    </div>
</template>
  
<script setup lang="ts">
    
</script>
  
<style scoped lang="scss">
*{
    margin : 0;
    padding: auto;
    background-color: white;
}
i{
    background-color: transparent;
}
p{
    font-size: 90%;
    color: rgb(141, 140, 140);
    background-color: white;
}
.main-container{
    margin: 1px;
    display:grid;
    grid-template-columns: 30% 68%;
    gap:15px;
    max-width: 100%;

}

.content{
    border: #e1d2d2;
    box-shadow: 0px 1px 10px #e1d2d2;
    flex: 1 1 100px; /* Tamaño mínimo de 200px, y permite que crezca */
    max-width: 100%; /* Las tarjetas no excederán el ancho del contenedor */
    box-sizing: border-box;
    margin-bottom: 20px;
    padding: 15px;
}

/**** LEFT ****/
.container-left p{
    padding-bottom: 10px;
}

/**** RIGHT ****/

/* Right-second */
.Right-second{
    background-color: transparent;
    border: transparent;
    box-shadow: 0px 0px 0px #e1d2d2;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    gap: 15px;
    margin: 0; 
    padding: 0;
}

.card-connection-main{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
}
.card-connection{
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 10px;
    padding: 10px 0;
}



</style >