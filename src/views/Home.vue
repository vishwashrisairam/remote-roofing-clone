<template>

  <div class="home container">
    <div class="benefits-block hidden-xs">
      <div class="benefits">
        <div class="image-container">
          <img 
            src="https://uploads-ssl.webflow.com/5f127ac8860f158e650f06b5/5f1290e8860f155c380f1c02_3039041%403x.png"
            alt="" 
            width="59px">
        </div>
        <div class="benefits-text">
          Free Inspection
        </div>
      </div>
      <div class="benefits">
        <div class="image-container">
          <img 
            src="https://uploads-ssl.webflow.com/5f127ac8860f158e650f06b5/5f1293b423e1bd4b2b89c278_2921571%403x.png"
            alt="" 
            width="59px">
        </div>
        <div class="benefits-text">
          File a Claim
        </div>
      </div>
      <div class="benefits">
        <div class="image-container">
          <img 
            src="https://uploads-ssl.webflow.com/5f127ac8860f158e650f06b5/5f12939072c6226dbd635684_69886%403x.png"
            alt="" 
            width="59px">
        </div>
        <div class="benefits-text">
          Replace or Repair a Roof
        </div>
      </div>
    
    </div>
    <div class="free-inspection-section container">
      <div class="row">
      <div class="col-lg-6 col-md-6 col-sm-6">
        <div class="text-block-heading">
          Get Free Inspection <br/>
          in Seconds
        </div>
        <div class="text-block-content">
          Getting your roof inspected is the first step when getting it repaired. Remote Roofing uses satellite imagery and artificial intelligence to analyze your roof’s damage. It’s all done remotely and in seconds!
          <br/><br/>
          Get your free remote roof inspection to get one step closer to having a new roof.  Learn More
        </div>
    
      </div>
      <div class="col-lg-6 col-md-6  col-sm-6">
        <img 
          src="https://uploads-ssl.webflow.com/5f127ac8860f158e650f06b5/5f13605291b235799b10df7d_group-16%403x.png" 
          sizes="(max-width: 767px) 100vw, (max-width: 991px) 324px, 378px" 
          alt="" 
          width="378"
        />
      </div>
      </div>
    </div>
    <div>
      <h1>Other Sections TODO</h1>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
export default {
  name: 'Home',
  components: {
   
  }
}
</script>

<style scoped>
.benefits-block {
	position: relative;
	top: -60px;
	display: flex;
	height: 150px;
	padding-right: 40px;
	padding-left: 40px;
	justify-content: space-around;
	align-items: center;
	border-radius: 11px;
	background-color: #0059bf;
	box-shadow: 2px 2px 7px 0 rgba(10, 10, 10, 0.5);
}

.benefits{
	position: relative;
	top: 0px;
	display: flex;
	width: 30%;
	height: 130px;
	padding-right: 20px;
	padding-left: 20px;
	justify-content: center;
	align-items: center;
	border-radius: 11px;
	background-color: #0059bf;
}

.image-container{
  display: flex;
  margin-right: 0px;
  padding-right:20px ;
  justify-content: flex-end;
}

.benefits-text{
font-family: "AirbnbCerealBook, sans-serif";
color: #fff;
font-size: 18px;
font-weight: 400;
}
.text-block-heading {
	margin-top: 40px;
	font-family: "AirbnbCerealBold, sans-serif";
  font-weight:700;
	font-size: 30px;
	line-height: 1.2em;
  text-align: left;
}

.text-block-content {
	margin-top: 40px;
  font-weight:400;
  text-align: left;
	font-family: "AirbnbCerealMedium, sans-serif";
}
.address-section{
    margin-top:40px;
    align-content: left;
    display: flex;
}
</style>
