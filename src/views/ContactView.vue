<template>
   <div class="contact">
    <img src="./images/contact.jpg" class="img-fluid">
    <p class="para">CONTACT US</p>
    <ContactView2 />
  </div>
</template>

<script>
import ContactView2 from './ContactView2'
export default{
    name:'ContactView',
    components:{
      ContactView2,
    },
  data(){
    return{
    }
  },
}
</script>

<style scoped>
.contact img{
  max-width:100%;
  min-height:500px;
  opacity:0.8;
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
@media only screen and (max-width:500px) {
  .contact{
    max-width: 100%;
    padding:0px;
    margin:0px;
  }
  .contact .img-fluid{
    max-width: 124%;
  }
}
</style>
