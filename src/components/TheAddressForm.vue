<template>
    <!-- <div class="row"> -->
        
        <div class="row">
        <div class="col-lg-6 col-sm-12 col-md-7">
        <div class="address-form">
        <form 
            action="" 
            v-on:submit.prevent="checkErrors"
            id="addressForm" 
            name="addressForm"
            class="form-inline"
        >
            
            <div class="form-group">
            <!-- <div class="col-lg-1 col-sm-1"> -->
            <img 
                src="https://uploads-ssl.webflow.com/5f127ac8860f158e650f06b5/5f13618db066ca1a332318d1_home%403x.png" 
                alt=""
                width="20"
                class="image"
            >
            </div>
            
            <div class="form-group flex-fill">
            <vue-google-autocomplete
                id="map"
                ref="options"
                classname="form-control input-field"
                placeholder="Enter Your Address"
                v-model="address"
                v-on:placechanged="getSuggestions"
            >
            </vue-google-autocomplete>
            </div>
            <!-- <div class="col-lg-4 col-md-1 col-sm-1"> -->
            <div class="form-group">
            <input 
                type="submit" 
                value="Get Inspection" 
                data-wait="Please wait..." 
                class="btn submit-button">
            </div>
            
        </form>
        </div>
        </div>
        </div>
    <!-- </div> -->
</template>

<script>
// import axios from 'axios';
import VueGoogleAutocomplete from 'vue-google-autocomplete'

export default {
    name: 'TheAddressForm',
    components: {
        VueGoogleAutocomplete
    },
    data:()=>{
        return{
            address:"",
            options:[]
        } 
    },
    methods:{
        getSuggestions(addressData) {
            // axios.get('placesAutoComplete.json')
            //     .then(res=>res.data)
            //     .then(res=>{
            //         this.options= res.predictions
            //         // console.log(this.options)
            //     })
            //     .catch(err=>console.log(err))
            this.address= addressData.route + ','+ addressData.locality;
            console.log(this.address)
                
        },
        checkErrors(){
            console.log(this.address)
            if(this.address.length===0){
                alert("Please use a full, valid address by choosing from the autocomplete dropdown");
            }else{
                this.$router.push({name:'TODO'})
            }
        }
    }
}

</script>


<style >
.address-form {
	position: relative;
	z-index: 0;
	height: 60px;
	max-height: none;
	/* width: 50%; */
	margin: 10px 25px;
    padding:5px;
	border-radius: 50px;
	background-color: #fff;
	box-shadow: 1px 1px 3px 0 #000;
}

img{
    display: inline-block;
    vertical-align: middle;
}

.image{
    max-width: 60px;
    margin-left: 15px;
}
.submit-button {
	height: 45px;
	min-width: 95px;
	/* margin-right: 10px; */
	border-radius: 22px !important;
	background-color: #017afe;
    color: white;
	font-family: "AirbnbCerealBook, sans-serif";
    cursor: pointer;
	font-size: 16px;
    display: inline-block;
}
.input-field{
    display:block;
	border: 1px solid transparent;
    padding:20px 10px;
    margin:0px 10px;
    width:75%;
    flex: 1 1 0;
    width:0;
    
}
.form-control{
    width: 2rem;
    
}


</style>