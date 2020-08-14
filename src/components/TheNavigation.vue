<template>
  <div :class = "isFaq?'header-faq':'header'">
    <div class="top-header">
      <div class="pull-left">
        <router-link to="/">
            <img 
            :src="require('@/assets/logo-white.png')" 
            alt
            class="logo"
             />
        </router-link>
      </div>
      <div class="phone-container">
          <div class="phone-icon-container">
            <img
              src="https://uploads-ssl.webflow.com/5f127ac8860f158e650f06b5/5f1297d1c3fecf36271c10a2_483947%403x.png"
              alt
              class="image-phone-icon"
            />
          </div>
          <div class="phone-number-container">
            <a href="tel:18004017716">
              <div class="phone-number">
                <strong >1800-401-7716</strong>
              </div>
            </a>
          </div>
      </div>
    </div>

    <div class="header-caption">
        <nav id="nav">
            <router-link to="/">Home</router-link>
            <router-link to="/faq">FAQ</router-link>
            <router-link to="#services">Services</router-link>
        </nav>
    </div>
    <div class="" v-show="this.$route.path==='/'">
      <div class="header-caption">
          <h1 class="heading">Roof inspections made remote and easy</h1>
          <div class="subheading">Get your roof inspected remotely and connect with our trusted roofers</div>
      </div>
      <div class="address-section">
        <TheAddressForm/>
      </div> 
    </div>
    <div class="faq-content" v-show="this.$route.path==='/faq'">
      <h1 class="faq-title">Get Free Roof Inspection in Seconds</h1>
      <div class="address-section">
        <div class="row">
        <!-- <div class="col-lg-offset-3"></div> -->
        <div class="col-lg-9 offset-lg-3">
        <TheAddressForm />
        </div>
        </div>
      </div> 
    </div>

    

  </div>
</template>

<script>

import TheAddressForm from './TheAddressForm';

export default {
  name: 'Nav',
  components: {
    TheAddressForm,
  },
  data(){
    return {

    }
  },
  computed:{
    isFaq(){
      return this.$route.path==='/faq'
    }
    
  }
}
</script>

<style scoped>
.header {
    background-image: url("https://uploads-ssl.webflow.com/5f127ac8860f158e650f06b5/5f127dcece36df2cd5e4f713_Screen%20Shot%202020-07-17%20at%209.41.58%20PM.png") ;
    background-position: 0px 0px;
    /* position:fixed; */
    background-size: cover;
    padding-bottom: 140px;
    margin-left: auto;
    margin-right:auto;
}

.header-faq {
    background-color:#027aff ;
    background-size: cover;
    padding-bottom: 140px;
    margin-left: auto;
    margin-right:auto;
}
.faq-content{
  flex-direction: column;
  justify-content:center;
}
.top-header{
    padding: 10px 20px;
    justify-content: space-between;
    margin: 0px 20px 20px 20px;
}

.logo{
    width:82px;
    height:30px;
}

.image-phone-icon{
    max-width: 15px;
    margin-right: 5px;
    margin-top: 3px;
}

.phone-container {
  display: flex;
  margin-right: 20px;
  float: right;
}
.phone-number-container{
    padding:5px
}
.phone-number{
    color:#fff;
    border: 0px solid #fff;
    font-weight:400
}

#nav{
    padding: 20px 0px;
    display: flex;
    margin:10px 0px;
}

#nav a {
    font-family:" AirbnbCerealLight, sans-serif";
    color:#fff;
    font-size:20px; 
    margin-right:46px;
    font-weight:400;
}
#nav a.router-link-exact-active{
    text-decoration: underline;
    color:#fff;
    /* padding-left:-5px; */
}

.header-caption{
    padding: 5px 10px ;
    text-align:left;
    margin-left:25px;
}

.heading{
	margin-top: 30px;
	font-family: "AirbnbCerealBold, sans-serif";
	color: #fff;
  font-size:38px;
	font-weight: 700;
}
.subheading {
	font-family: AirbnbCerealLight, sans-serif;
	color: #fff;
	font-size: 18px;
	line-height: 1.5em;
	font-weight: 700;
}

.address-section{
    margin-top:40px;
    margin-left:20px;
    /* display: flex; */
}
.faq-title {
	margin: 10px 20px;
	font-family: "AirbnbCerealBold, sans-serif";
	color: #fff;
	font-weight: 700;
	text-align: center;
  font-size:38px;
  line-height:44px;
}


</style>

