<template>
    <div class="footerConatiner">
        <p><i class="bi bi-c-circle"></i> 2024 Made with ❤️ By <a href="">Pixinvent</a></p>
        <div>
            <a href="">Lincense</a>
            <a href="">More Themes</a>
            <a href="">Documentation</a>
            <a href="">Support</a>
        </div>
    </div>
</template>
  
<script setup lang="ts">
    
</script>
  
<style scoped lang="scss">
  //FOOTER
.footerConatiner{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 20px 0 50px 0;
    margin: 30px auto 0 auto;
    width: 100%;
}
.footerConatiner p{
    font-size: 70%;
    margin: 0;
}
.footerConatiner p a{
    color: #7266ee;
}
.footerConatiner div{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    margin: 0;
}

.footerConatiner div a{
    font-size: 70%;
    color: #7266ee;
    margin-left: 10px;
}

.footerConatiner div a:hover{
    color: #3d3d3d;
}
</style >