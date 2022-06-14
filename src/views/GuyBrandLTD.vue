
<template>
<div class="main">
  <div class="container">
         <h1 class="text1"> 
      Guybrand Limited
         </h1>    
        
        <hr style="background-color:blue"/>  
          <p class="info">
              Guybrand Limited is a family-run building company. Every home is unique and should be perfectly built and designed to meet your needs. The Guybrand Limited team is made up of talented and experienced building professionals who will discuss all the options available and work with you to develop the best solution for your home.
          </p>   
    <div class="row mt-5">
      <div class="col-md-6 division">
        <p class="text2">When it comes to any building project, there is a wealth of information available and the options can be overwhelming. Whether you’re starting the process of working your way up the property ladder, remodelling your living space, or building a dream home, it can be tricky to know where to start. We are here to support you on every step of the journey.</p>
      </div>
      <div class="col-sm-6 mx-auto">
       <img src="./images/LTD1.jpg" class="images img-fluid">
      </div>
    </div>

    <div class="row mt-5 reverse">
      <div class="col-md-6 division">
         <p class="text2">The Guybrand Limited building expertise is vast. We undertake all types of projects – from new builds, extensions and conversions to high-end renovations, as well as commercial work. Whatever the size or scope of your project, you can be confident that Guybrand Limited will deliver with meticulous care, great value and efficiency.</p>
      </div>
        <div class="col-sm-6 mx-auto">
       <img src="./images/LTD2.jpg" class="images img-fluid">
      </div>
    </div>

    <div class="row mt-5 ">
      <div class="col-sm-6">
        <h1 class="text">
            Read to go?
        </h1>
        <p class="text3">
            If you have architectural plans and are looking for professional builders, find out more about the Guybrand Limited Bespoke Build service.
        </p>
      </div>
      <div class="col-sm-6">
       <h1 class="text">
           Just Starting Out?
       </h1>
       <p class="text3">
           If you’re at the beginning of your journey and need someone to take care of everything, find out more about the Guybrand Limited Design, Planning & Build service.
       </p>
      </div>
   </div>
</div>
</div>
</template> 

<script>
export default{
  name:'GuyBrandLTD',
}
</script>

<style>
.main{
    background-image: url('./images/background.jpg');
    max-width: 100%;
}
p{
  text-indent: 50px;
  text-align: justify;
}
.text,.text1{
    font-size:25px;
    color:orange;
    font-family: Copperplate,Copperplate Gothic Light,fantasy;
    font-weight: bold;
   text-align: center;
   padding:29px;
}
.info{
    text-align: justify;
    word-spacing: 2px;
    font-size: 19px;
    text-indent: 0;
    color:white;
}
.text2{
    text-indent: 0px;
    margin-top:150px;
    color:white;
    font-size:18px;
}
.text3{
    word-spacing: 2px;
    color:white;
    text-indent: 0px;
    font-size:19px;
}
.images{
  width: 900px;
  height:300px
}
.reverse{
  display:flex;
  flex-direction: row-reverse;
}
@media only screen and(max-width:200) {
  .container{
    max-width:100%;
  }
  .text{
    margin:15px 0px;
    text-align: center;
  }
  .text2{
    margin-top:40px;
  }
  .division{
   margin-top:-64px;
  }
}
</style>




