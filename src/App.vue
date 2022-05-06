<template>
<!-- The whole container -->

  <div class="container-fluid">
   <div class="row">
     <div class="col-md-5 left-img"></div>
       <div style="background:#E5E5E5;" class="col-md-7 px-5 " >
         <!-- beginning of Page one -->
         <div v-if="state">
          <p class="light-text text-end px-5 mt-5 mb-5">Already have an account?<span><a href="#">Sign In</a></span></p>
          <div>
          <h4 class="title pt-5 px-5">Join Us!</h4>
            <p class="sub-title px-5">To begin this journey, tell us what type of account you’d be opening.</p>
          </div>

   <div class="d-flex mx-5 personal mb-4 mt-5 px-4">
          <div class="polygon-ctn mt-4 ">
            <img class="polygon-img" src="../src/assets/images/Polygon1.png" alt="polygon">
            <img class="polygonsub-img"  src="../src/assets/images/user.png" alt="">
          </div>

            <div class="px-4" @click="showReg">
                <p class="individual mb-0 mt-3">Individual</p>
                <div class="d-flex justify-content-between">
                    <div>
                      <p class="some-text">Personal account to manage all your activities.</p>
                    </div>
                    <div>
                      <img src="../src/assets/images/arrow-right.png" alt="">
                    </div>
                </div>
            </div>
  </div>

      <div class="d-flex mx-5 business px-4">
        <div class="polygon-2-ctn mt-4 ">
          <img src="../src/assets/images/Polygon2.png" alt="">
          <img class="polygonsub-img"  src="../src/assets/images/briefcase.png" alt="">
        </div>
        <div class="px-4 mt-4">
          <p class="bus-text mb-0">Business</p>
          <p class="bus-sub-text">Own or belong to a company, this is for you.</p>
        </div>
      </div>

       </div>
       <!-- end of page one  -->
<!--Beginning of second page (registration form) -->
    <div v-if="!state">
      <!-- beginning of form -->
        <div v-if="second">
            <div class="d-flex justify-content-between">
              <div class="back-text">
                <p><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-chevron-left" viewBox="0 0 16 16">
              <path fill-rule="evenodd" d="M11.354 1.646a.5.5 0 0 1 0 .708L5.707 8l5.647 5.646a.5.5 0 0 1-.708.708l-6-6a.5.5 0 0 1 0-.708l6-6a.5.5 0 0 1 .708 0z"/>
              </svg>  Back</p>
              </div>
              <div class="heading-text">
                <p>STEP 01/03</p>
              </div>
            </div>
            <p class="text-end back-text">Personal Info</p>
            <div class="mx-5 form-part text-left">
              <h5 class="formTitle">Register Individual Account!</h5>
                    <p class="formTitle-text">For the purpose of industry regulation, your details are required.</p>
                    <form>
                       <div class="mb-3">
                            <label for="exampleInputName" class="form-label  labelsLabels">Your fullname*</label>
                            <input type="text" class="form-control" id="exampleInputName" aria-describedby="emailHelp" placeholder="Invictus Innocent" required>
                                   
                        </div>
                       <div class="mb-3">

                            <label for="exampleInputEmail1" class="form-label labelsLabels">Email address*</label>
                            <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Enter email address" required>
                                    
                        </div> 
                         <div class="mb-3">
                              <label for="exampleInputPassword1" class="form-label labelsLabels">Create password*</label>
                              <div class="d-flex password-wrapper">
                                  <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Enter Password" required>
                                  <p class="show-text">show</p>
                              </div>
                           </div>  
                            <div class="mb-3 form-check">
                                    <input type="checkbox" class="form-check-input" id="exampleCheck1" required>
                                    <label class="form-check-label labelsLabels" for="exampleCheck1">I agree to terms & conditions</label>
                                </div>
                           <button type="submit" class="btn reg-btn" @click="newpage">Register Account</button>
                                <p class="text-center mt-3" style="color:#BABABA">or</p>
                                <div class="d-flex align-items-center px-4 goolge-point">
                                   <div>
                                      <img src="../src/assets/images/google-icon.png" alt="">
                                   </div>
                                    <div><p class="mx-5 pt-3" style="font-size:20px;">Register with Google</p></div>
                                
                                </div>      
                    </form>
            </div>
        </div>
      <!-- End of form -->
      <!-- Beginning of Third Page -->
      <div v-if="!second">
       <div v-if="third">
         <div class="d-flex justify-content-between">
              <div class="back-text">
                <p><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-chevron-left" viewBox="0 0 16 16">
              <path fill-rule="evenodd" d="M11.354 1.646a.5.5 0 0 1 0 .708L5.707 8l5.647 5.646a.5.5 0 0 1-.708.708l-6-6a.5.5 0 0 1 0-.708l6-6a.5.5 0 0 1 .708 0z"/>
              </svg>  Back</p>
              </div>
              <div class="heading-text">
                <p>STEP 02/03</p>
              </div>
            </div>
            <p class="text-end back-text">Residency Info.</p>

             <div class="mx-5 form-part text-left">
              <h5 class="formTitle">Complete Your Profile!</h5>
                    <p class="formTitle-text">For the purpose of industry regulation, your details are required.</p>
                    <form>
                      
                          <div class="input-group mb-3">
                     <button class="btn btn-outline-secondary dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false"><span><img src="../src/assets/images/Frame.png" alt=""></span> +234</button>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="#">Action</a></li>
                        <li><a class="dropdown-item" href="#">Another action</a></li>
                        <li><a class="dropdown-item" href="#">Something else here</a></li>
                        <li><hr class="dropdown-divider"></li>
                        <li><a class="dropdown-item" href="#">Separated link</a></li>
                    </ul>
                    <input type="text" class="form-control" aria-label="Text input with dropdown button" placeholder="08122801279">
                </div>  

                  <div class="mb-3">
                       <label for="exampleInputAddress" class="form-label">Your address</label>
                       <input type="text" class="form-control" id="exampleInputAddress" aria-describedby="emailHelp" placeholder="Please enter address" required>
                                    
                   </div>
                             <div class="">
                                <p>Country of residence</p>
                              </div>
                               <div class="input-group mb-5">
                                 
                                    <select class="form-select" id="inputGroupSelect04" aria-label="Example select with button addon">
                                        <option selected>Please select</option>
                                        <option value="1">Nigeria</option>
                                        <option value="2">London</option>
                                        <option value="3">Canada</option>
                                    </select>
                                     <!-- <button class="btn btn-outline-secondary" type="button">Button</button> -->
                                </div>
                <!--  -->
                       
                         
                           
                           <button type="submit" class="btn reg-btn mb-3" @click="finalPage">Save & Continue</button>
                              <div class="text-center" style="color:#8692A6;">
                                    <img style="" src="../src/assets/images/lock_24px.png" alt=""><span class="px-2">Your Info is safely secured</span>
                                </div>    
                    </form>
            </div>
       </div>
       <!-- beginning of fourth page -->
       <div v-if="!third">
        <div>
           <div class="d-flex justify-content-between">
              <div class="back-text">
                <p class="mt-5"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-chevron-left" viewBox="0 0 16 16">
              <path fill-rule="evenodd" d="M11.354 1.646a.5.5 0 0 1 0 .708L5.707 8l5.647 5.646a.5.5 0 0 1-.708.708l-6-6a.5.5 0 0 1 0-.708l6-6a.5.5 0 0 1 .708 0z"/>
              </svg>  Back</p>
              </div>
              <div class="heading-text mt-5">
                <p>STEP 03/03</p>
              </div>
            </div>
            <p class="text-end back-text">Bank Verification</p>

                 <div class="mx-5 form-part text-left">
                          <h5 class="formTitle">Complete Your Profile!</h5>
                          <p class="formTitle-text">For the purpose of industry regulation, your details are required.</p>
                    <form>
                      
                     <div class="mb-3">
                          <label for="exampleInputBvn" class="form-label" style="color: #696F79; font-family: 'Inter', sans-serif;">Bank verification number (BVN)</label>
                          <div class="d-flex bvn-class">
                            
                                <input type="text" class="form-control mb-5 border" style="width:100%" id="exampleInputBvn" aria-describedby="emailHelp" placeholder="08122801279" required>
                           
                          <div>
                            <img class="checkImg" src="../src/assets/images/circlecheckfull.png" alt="">
                          </div>
                          </div>
                      </div> 

                      <button type="submit" class="btn reg-btn mb-3" >Save & Continue</button>
                        <div class="text-center" style="color:#8692A6;">
                              <img style="" src="../src/assets/images/lock_24px.png" alt=""><span class="px-2">Your Info is safely secured</span>
                          </div>    
                    </form>
            </div>
        </div>
       </div>
       <!-- End of fourth page  -->
      </div>
      <!-- End of Third Page -->
    </div>

    <!-- End of second page -->
   
 </div>
    
</div>
</div>
</template>

<script>
export default{
  data(){
    return{
      state: true,
      second: true,
      third: true,
    }
  },
  methods:{
    showReg(){
      this.state = false;
    },
    newpage(){
      this.second = false;
    },
    finalPage(){
      this.third = false;
    }
  }
}
</script>

<style scoped>
body{
  font-family: 'Inter', sans-serif;
}
.left-img{
background-image: url(../src/assets/images/backback.png);
height: 100vh;
background-size: cover;
}

.light-text{
  color:#8692A6;
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  font-family: 'Inter', sans-serif;
}

.title{
  color: #000000;
  font-style: normal;
  font-weight: 700;
  font-size: 30px;
  line-height: 36px;
  font-family: 'Inter', sans-serif;

}

.sub-title{
  width: 100%;
  max-width: 28rem;
  color:#8692A6;
  font-weight: 400;
  font-size: 18px;
  font-family: 'Inter', sans-serif;
}

.personal{
background-color: #F5F9FF;

box-shadow: 0px 4px 14px 1px rgba(0, 0, 0, 0.04);
border-radius: 6px;
width: 100%;
height: 100%;
max-height: 7rem;
max-width: 450px;
cursor: pointer;
font-family: 'Inter', sans-serif;
}

.personal:hover{
border: 1px solid #1565D8;
}

.polygon-ctn{
  position: relative;
}

.polygonsub-img{
  position: absolute;
  left: 15px; 
  top:18px;
}

.individual{
  line-height: normal;
  font-weight: 500;
  color: #000000;
}

.some-text{
  color: #8692A6;
font-weight: 500;

}

.polygon-2-ctn{
   position: relative;
}

.business{
/* border: 1px solid #1565D8; */
/* box-shadow: 0px 4px 14px 1px rgba(0, 0, 0, 0.04); */
/* border-radius: 6px; */
width: 100%;
height: 100%;
max-height: 7rem;
max-width: 450px;
cursor: pointer;
font-family: 'Inter', sans-serif;
background: #FFFFFF;
box-shadow: 0px 2px 14px 1px rgba(0, 0, 0, 0.06);
border-radius: 6px;
cursor: pointer;
}

.bus-text{
    line-height: normal;
  font-weight: 500;
  color: #000000;
}

.bus-sub-text{
    color: #8692A6;
font-weight: 500;
}
/* End of Page one styles */
/* Beginning of Page two style */
.back-text{
  color: #8692A6;
  font-weight: 600;
font-size: 16px;
font-family: 'Inter';
}

.heading-text{
  color: #BDBDBD;
  font-weight: 500;
font-size: 14px;
font-family: 'Inter';
}

.form-part{
  /* border: 2px solid red; */
  height: 100%;
  width: 100%;
  max-width: 25rem;
  margin-top: 3rem;
}

.formTitle{
  font-family: 'Inter';
font-weight: 700;
font-size: 25px;
line-height: normal;
color: #000000;
}

.formTitle-text{
  font-family: 'Inter';
font-style: normal;
font-weight: 400;
font-size: 15px;
line-height:normal;
color: #8692A6;
width: 100%;
max-width: 85%
}

.labelsLabels{
font-family: 'Inter';
font-style: normal;
font-weight: 500;
font-size: 14px;
/* line-height: 19px; */
color: #696F79;
}

.password-wrapper{
  position: relative;
}

.show-text{
position: absolute;
right: 10px;
top:8px;
font-family: 'Inter';
font-weight: 400;
font-size: 15px;
color: #000000;
z-index: 99;
background-color: #FFFFFF;
}

.reg-btn{
width: 100%;
height: 50px;
background: #1565D8;
border-radius: 6px;
color:#FFFFFF;

}

.goolge-point{
background: #FFFFFF;
box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.08);
border-radius: 6px;
}

.bvn-class{
 position: relative;
}

.checkImg{
position: absolute;
right: 10px;
top:8px;
}
/* End of Page two style */
</style>