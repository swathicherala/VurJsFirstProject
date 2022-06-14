<template>
   <div class="services">
    <img src="./images/services.jpg" class="img-fluid">
    <p class="para">OUR SERVICES</p>
    <ServicesView2 />
  </div>
</template>

<script>
import ServicesView2 from './ServicesView2'
export default{
    name: 'ServicesView',
    components:{
        ServicesView2,
    },
  data(){
    return{
    }
  },
}
</script>

<style scoped>
.services img{
  max-width:100%;
  min-height:500px;
  opacity:0.88;
}
.para{
    left: 0;
  position: absolute;
  text-align: center;
  top: 38%;
  width: 100%;
  font-size:25px;
  font-weight: bold;
  color:black;
}
</style>