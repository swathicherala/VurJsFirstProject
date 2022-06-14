<template>
  <div class="main">
     <div class="container">
          <h1 class="text">
          Start Your Journey and Get in Touch
      </h1>
      <hr style="background-color:blue"/>
      <p class="servicestext">
          If you are right at the start of your project, or already have plans and are raring to go – we can help! Whether it is major structural alterations or contemporary fit-outs, please don’t hesitate to get in touch to find out more about Guybrand Limited, or to get a no obligation quote.
      </p>
      <br>
      <p class="mb-5 servicestext">
          Please feel free to contact us regarding any of our services using the following details:
      </p>
      <div class="row contact">
          <div class="col-sm-6 flex-item-left">
              <div class="loc" style="padding-right:500px;">
                  <i class="fa-solid fa-location-dot"><span>Address</span></i>
                  
              </div>
                  <div class="same">
                  Guybrand Limited,<br/>
                  Office 973,<br/>
                  58 Peregrine Road,<br/>
                  Illford IG6 3SZ<br/>
                  </div>
          </div>
          <div class="col-sm-6 flex-item-right">
             <div style="padding-right:15px;">
                  <i class="fa-solid fa-phone"></i><span>Landline:</span> <a href="" style="color:orange;">0207 183 0754</a><br/><br/>
             </div>
            <i class="fa-solid fa-envelope"></i><span>Email:</span> <a href="" style="color:orange;">sales@guybrand.co.uk</a>
          </div>
      </div><br/><br/>
       <h1 class="head mb-2">WHERE WE ARE</h1><hr style="background: #2f7ef5;"/>
       <div>
           <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d4955.339005634764!2d0.125367!3d51.61094400000001!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0xd34359e81627c46f!2sToot%20Sweet!5e0!3m2!1sen!2sin!4v1654580600476!5m2!1sen!2sin" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
       </div>
     </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.servicestext{
    color:white;
    font-size:20px;
    text-indent: 0;
}
.text{
    font-size:25px;
    color:orange;
    font-family: Copperplate,Copperplate Gothic Light,fantasy;
    font-weight: bold;
   text-align: center;
}
.same{
    text-align: left;
}
.contact{
    color:orange;
    display: flex;
    flex-direction: row;
    align-items: flex-start;
}
.head{
    font-family: Copperplate,Copperplate Gothic Light,fantasy;
    color: orange;
    font-size: 20px;
    font-weight: bold;
    text-align: center;
}
iframe{
    width:100%;
    height:560px;
    padding-bottom:20px;
}
span{
    font-size:12px;
    font-weight: bold;
}
i{
    color: rgb(7, 7, 156);
    margin-right:2px;
}
i span{
    color:orange;
    text-transform: none;
}
@media only screen and (max-width:500px) {
    .main{
        max-width:900px;
    }
    .container{
        max-width: 531px;
    }
 .contact{
     flex-wrap:nowrap;
 }
 .flex-item-left{
     margin:auto;
     max-width: 24%;
 }
 .loc{
 padding-right:48px;
 }
}

</style>