<template >
    <div class="mainContainer">
      <!-- ----------- LEFT CONTAINER ----------- -->
        <div id="leftContainer">
            <button><i ><img src="../assets/images/logo.png" alt="" style="width: 30px; "></i></button>
            <button><i class="bi bi-calendar4-event"></i></button>
            <button><i class="bi bi-files"></i></button>
            <button><i class="bi bi-cart"></i></button>
            <button><i class="bi bi-chat-text"></i></button>
            <button><i class="bi bi-calendar2-check"></i></button>
            <button><i class="bi bi-person"></i></button>
            <button><i class="bi bi-bar-chart"></i></button>
            <button><i class="bi bi-house-door"></i></button>
            <button><i class="bi bi-bag-dash"></i></button>
            <button><i class="bi bi-file-lock"></i></button>
            <button><i class="bi bi-shield-exclamation"></i></button>
        </div>
        
  
      <!-- ----------- CENTER CONTAINER ----------- -->
      <div id="centerContainer">
        <header>
          <div class="mainheader">
          </div>
          <div class="profilePhoto">
            <img src="../assets/images/perfil.png" alt="">
          </div>
          <div class="profileInfo">
            <div class="profileInfoName">
              <h3>John Doe</h3>
            </div>
            <div class="profileInfoGeneral">
              <div class="profileInfoData">
                <p class="generalFont"><i class="bi bi-palette"></i> Coder</p>
                <p class="generalFont"><i class="bi bi-geo-alt"></i> Medellin</p>
                <p class="generalFont"><i class="bi bi-calendar4-event"></i> Joined April 2021</p>
              </div>
                <button><i class="bi bi-person-check" style="background-color: #7266ee;"></i> Connected</button>
            </div>
          </div>
        </header>
  
        <body>
          <div>
            <div>
              <ChangePage />  <!-- changePage -->
            </div>
            <footer>
                <FooterBody />  <!-- FooterBody -->
            </footer>
          </div>
        </body>
      </div>
  
      <!-- ----------- RIGHT CONTAINER ----------- -->
      <div id="rightContainer">
        <div class="gear">
          <button><i class="bi bi-gear" style="background-color: #7266ee;"></i></button>
        </div>
        <div class="buttons_right">
          <button class="buyNow" >Buy Now</button>
          <button @click="scrollToTop" class="arrow"><i class="bi bi-arrow-up" style="background-color: #7266ee;"></i></button>
        </div>
      </div>
    </div>
    
  </template>
  
  <script setup lang="ts">
    import ChangePage from "@/components/ChangePage.vue";
    import FooterBody from "@/components/FooterBody.vue";

    const scrollToTop = () => {
      window.scrollTo({top: 0, behavior: 'smooth'});
    }
    
  </script>
  
  <style scoped lang="scss">
    
  </style >
  