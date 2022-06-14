<template>
  <div>
    <nav class="navbar navbar-expand-md bg-light fixed-top">
      <div class="container">
          <img src="./views/images/logo.svg" class="navbar-brand">  
        <button
                class="navbar-toggler"
                type="button"
                data-bs-toggle="collapse"
                data-bs-target="#navbarTogglerDemo01"
                aria-controls="navbarTogglerDemo01"
                aria-expanded="false"
                aria-label="Toggle navigation"
            >
                <span class="navbar-toggler-icon"></span>
                </button>
        <div class="collapse navbar-collapse" id="navbarTogglerDemo01">
           <ul class="navbar-nav mainnav">
          <li class="nav-item">
            <router-link to="/" class="list">Home</router-link> 
          </li>
          <li class="nav-item">          
         <router-link to="/about" class="list">About</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/services" class="list">Services</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/contact" class="list">Contact</router-link>
          </li>
          </ul> 
       </div>
      </div>
  </nav>
  <router-view/>
  <FooterView />
      </div>
</template>

<script>
import FooterView from './views/FooterView'
export default{
  name:'App',
  components:{
    FooterView
  },
  /*mounted(){
     this.url_data=this.$route.name;
    },
  data(){
    return{
      url_data: null
     //loc:"scn"
    }
  },*/
 
}
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
nav {
  padding: 30px 30px 0px 30px;
  margin-bottom: 0px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

.mainnav{
  margin-left:400px;
}

nav a.router-link-exact-active {
 color:#2f7ef5;
 text-decoration: none;
}

.navbar-brand{
  margin-top:0px;
  padding-top: 0px;
  width:19%;
  height: 90%;
  margin-top:-10px;
  padding-left:30px;
}
.nav-item{
  list-style: none;
}
.list{
  color:rgb(104, 102, 102);
  text-decoration: none;
  padding-left:18px;
  margin-left:28px;
  font-size:16px;
  text-transform: uppercase;
  font-weight: bold;
}
.list:hover{
  color:#2f7ef5;
  text-decoration: none;
}

@media only screen and (max-width:700px){
  
  nav ul li{
    display:block;
    margin-top:10px;
    margin-bottom:10px;
  }
  .navbar-toggler{
    margin-bottom:20px;
  }
  .mainnav{
    margin:auto;
  }
  .nav-item{
    display: block;
    text-align: center;
    padding:5px;
  }
  @media only screen and (max-width:780px){
   .navbar-toggler{
    margin-bottom:20px;
  }
    .mainnav{
    margin:auto;
  }
   .nav-item{
    display: block;
    text-align: center;
    padding:5px;
  }
}
}

</style>
