<template>
<div>
    <!-- Header -->
       <div class="header bg-gradient-success py-7 py-lg-8 pt-lg-9">
        <b-container>
            <div class="header-body text-center mb-7">
                <b-row class="justify-content-center">
                    <b-col xl="5" lg="6" md="8" class="px-5">

                    </b-col>
                </b-row>
            </div>
        </b-container>

    </div>
 <div class="container-fluid mt-5" style=" background-color: #4b4746; margin:auto !important;" >
<div class="row"> 
  <img src="./assets/newLOgo-white.png" alt="Company logo" style="     position: relative;
  margin: auto;   max-width: 500px;    padding: 65px; ">
</div>

   </div>
  <b-container class="page-contet mt--8 pb-5">

    <b-row class="justify-content-center mt-5">
      <b-col lg="7" md="10">
        <b-card
          no-body
          class="bg-white border-0 mb-0 "
          style="background: linear-gradient(87deg, rgb(75 71 70) 0px, rgb(75 71 70) 100%)  !important"
        >
          <b-card-header class="bg-transparent pb-5 ">
            <div class="text-muted text-center mt-2 mb-3">
              <h2 style="color:white;">معلومات الوصل</h2>
            </div>
          </b-card-header>
          <b-card-body class="px-lg-5 py-lg-5">
            <b-form role="form">
              <div>
                   <div class="inst-input mt-3">
                  <p>رقم الوصل</p>
                  <input v-model="receiptNo" class="paid-input" placeholder="  " required />
<br>
                </div>
                <div class="inst-input mt-3">
                  <p>المبلغ</p>
                  <input v-model="amount" class="paid-input" placeholder="  " required />
<br>
                </div>
                
                <br />
                <br />
                <br />
               
<p>التاريخ</p>
                  <input v-model="date" class="paid-input" type="date" id="birthday" name="birthday" />
                <div class="inst-input justify-content-center mt-3">
                <p>استلمت من السيد</p>
                  <input class="paid-input" v-model="client" placeholder="" required />

                </div>
                  <div class="inst-input justify-content-center mt-3">
                <p>مبلغ وقدره  </p>
                  <input class="paid-input" v-model="lettersAmount" placeholder=" " required />

                </div>
                <br />

                <br />

               
                <div class="inst-input justify-content-center mt-3">
                   <p>رقم البناية </p>
                  <input class="paid-input" v-model="buildingNo" placeholder="  " required />

                    <p>رقم الطابق </p>
                  <input class="paid-input" v-model="level" placeholder="  " required />

                    <p>رقم الشقة </p>
                  <input class="paid-input" v-model="flatNo" placeholder="  " required />
                    <p> المساحة </p>
                  <input class="paid-input" v-model="area" placeholder="  " required />

                    <p> الاتجاه </p>
                  <input class="paid-input" v-model="direction" placeholder="  " required />

                    <p> سعر الشقة </p>
                  <input class="paid-input" v-model="price" placeholder="  " required />

                    <p> المبلغ الواصل </p>
                  <input class="paid-input" v-model="delivered" placeholder="  " required />

                    <p> المبلغ المتبقي </p>
                  <input class="paid-input" v-model="due" placeholder="  " required />

                </div>
                <br />

                <br />
                 <p> المسلّم </p>
                  <input class="paid-input" v-model="client" placeholder="  " required />

                <p class="placetext">اسم المحاسب</p>
                <input type="letters" v-model="accountant" class="paid-input" required />
                <br />
                
                  <p> المدير المفوض </p>
                  <input class="paid-input" v-model="manager" placeholder="  " required />
                <br />
                <b-row class="equations">
                 
                </b-row>
              </div>
              <button class="mt-4" style=" border: 1px solid white; color:white; padding: 12px; background-color: transparent; border-radius: 15px;" @click="print">طباعة</button>
            </b-form>

  
  <v-html>
      <div id="printMe" class="row"
      style="padding: 15px;  font-family: 'Cairo', sans-serif !important; ">
      <div>
          <div>
              <div  class="row bodyPrint"
                  style="box-shadow: #4b4746 0px 0px 0px 1000px inset !important">
                  <div class="col" style="    position: relative;
                  margin-top: 3rem !important;
                  right: -7px;"> 
                    <h6 style="color:white;">  0780 553 1245</h6>

                    <h6 style="color:white;">0780 456 3215 </h6>
                  </div>
                  <div class="col mt-2"> <img src="./assets/newLOgo-white.png" alt="Company logo"
                          style="    margin-bottom: 15px;
                          max-width: 296px "></div>
                          <div class="col " style="position: relative;
                          margin-top: 3rem!important; left: 135px;">
                  <h6 style="color:white;">  شركة فانتاج العقارية للبيع والبناء</h6>

                  <h6 style="color:white;">Vantage Real Estate </h6>
                          </div>

                  </div>
          </div>

          <br>

          <div class="table-responsive" style="overflow-x: clip !important; padding: 25px;">

              <div class="row" style="position: relative; margin-top: -38px;     margin-bottom: -13px;">

                  <div class="col" sm="4 mt-2 ">
                      <button
                          style="     border: 1px solid lightgrey;   border-radius: 0px; background: transparent; height: 39px;">
                          No:{{receiptNo}}</button>

                  </div>
                  <div class="col" sm="4 mt-2 "> </div>

                  <div class="col" sm="4 mt-2 ">
                      <h4
                          style="color:white !important; box-shadow: #906248 0px 0px 0px 1000px inset !important; padding:5px; text-align:center;">
                          وصل قبض</h4>
                  </div>

                  <div class="col" sm="4 mt-2 "> </div>
                  <div class="col" sm="4 mt-2 "> 
                      <button
                          style="    font-weight: 900;
                          border-radius: 0px;
                          background: transparent;
                          height: 39px;
                          border: .5 px solid grey;
                          position: relative;
                  
                          border: 1px solid lightgrey;
                          left: 80px;">
                          $         {{amount}} : المبلغ </button>
                 

                        </div>

                </div>
              <div class="row mt-2">
                  <b-button class="mt-2"
                      style="color: black;  border: 1px solid lightgrey; border-radius: 0px; background: transparent; height: 39px; position: relative; left: 15px; bottom: 7px; ">
                      {{date}} 
                  </b-button>

                </div>
                <div class="row">

                  <div class="col-10">
                      <h5 style="border:.5px solid lightgray; padding:5px; text-align: end;">
                         {{client}} مبلغ وقدره  {{lettersAmount}} </h5>
                      </div>
                  <div class="col" style="    margin: inherit;">
                      <h5 style="margin-top: 9px;">: استلمــــت من السيــــد </h5>

                  </div>
                </div>

              <h5 style="    text-align: end;">العـــــــــــــــــــــــــــــــــائد
                  للشقـــــــــــــــــــــــــة المـــــــــــــــــبينة
                  مواصــــــــــــــفاتها أدنـــــــــــــــاه و فـــــــــــــي
                  التـــــــــــــــــــــــــــــــاريخ اعــــــــــــــــــلاه</h5>
                  <div class="row">
                  <table class="table table-bordered">
                      <thead>
                          <tr class="tr-class">
                              <th> &nbsp;الاتجاه</th>

                              <th>المساحة</th>

                              <th>رقم الشقة</th>
                              <th>الطابق</th>
                              <th> رقم البناية</th>

                          </tr>
                      </thead>
                      <tbody>
                          <tr>
                              

                              <td scope="row">{{direction}}</td>

                              <td>{{area}}</td>

                              <td class="mt-3"> {{flatNo}}</td>
                              <td>{{level}}</td>
                              <td>{{buildingNo}}</td>

                          </tr>

                      </tbody>
                  </table>
                </div>

              <div class="mt-1">
                  <div class="row" style="text-align:left; margin-bottom: -6px; ">
                    <div class="col" ></div>
                    <div class="col"  style="display: contents;">
                          <h6
                              style="color:white; position: relative; height: 38px; border:.5ps solid lightgray; box-shadow: #906248 0px 0px 0px 1000px inset !important; padding:7px;">
                              $</h6>

                          <button
                              style="      width: 120px;   border: 1px solid lightgrey;   border-radius: 0px;  border-radius: 0px; background: transparent; height: 39px;">
                              {{price}}
                          </button>

                        </div>
                        <div class="col-2" >
                          <h6 style="text-align: end;"> سعر الشقة</h6>
                        </div>

                    </div>

                    <div class="row"  style="text-align:left; margin-bottom: -6px; display: flex;  ">
                      <div class="col" ></div>
                      <div class="col" style="display: contents;">

                          <h6
                              style="color:white; position: relative; height: 38px; border:.5ps solid lightgray; box-shadow: #906248 0px 0px 0px 1000px inset !important; padding:7px;">
                              $</h6>

                          <button
                              style="    width: 120px;    border: 1px solid lightgrey;   border-radius: 0px; border-radius: 0px; background: transparent; height: 39px;">
                              {{delivered}}
                          </button>

                        </div>
                        <div class="col-2" >
                          <h6 style="text-align: end;"> المبلغ الواصل</h6>
                  </div>

                </div>

                <div class="row" style="text-align:left; margin-bottom: -6px; ">
                  <div class="col" ></div>
                      <div class="col" style="display: contents;">
                          <h6
                              style="color:white; position: relative; height: 38px;  border:.5ps solid lightgray; box-shadow: #906248 0px 0px 0px 1000px inset !important; padding:7px;">
                              $</h6>
                          <button
                              style="     width: 120px; border: 1px solid lightgrey;   border-radius: 0px; border-radius: 0px; background: transparent; height: 39px;">
                              {{due}}
                          </button>

                        </div>
                        <div class="col-2" >
                          <h6 style="text-align: end;"> المبلغ المتبقي </h6>
                        </div>
                      </div>

              </div>
              <div class="row"
                  style="text-align:right;  margin-bottom: -6px;  margin-top: 59px; display: flex;">
                  <div class="col" >
                      <h5 style="    margin-right: 18px;"> المدير المفوض / اضافة لوظيفته</h5>
                      <h5>{{manager}}</h5>
                    </div>

                    <div class="col" style="    left: -30px;">
                      <h5 style="    margin-right: 18px;"> المحاسب </h5>
                      <h5>{{accountant}}</h5>
                    </div>
                    <div class="col">
                      <h5 style="    margin-right: 18px;"> المسّلم </h5>
                      <h5>{{client}}</h5>
                    </div>

                  </div>

                  <div class="row mt-3 bodyPrint" 
                  style="box-shadow: rgb(75 71 70) 0px 0px 0px 1000px inset !important; margin-top:2px; padding: 1px; height: 74px; display: flex;">
                  <div class="col mt-3" sm="2" style="color:white;">
                      <p>0770 588 6662</p>

                      <p style="position: relative; bottom: 22px">0750 555 3933</p>
                    </div>
                    <div class="col mt-3" sm="1" style="color:white;">
                      <p style="position: relative;
                      left: -128px; margin-top: 8px !important;">
                          فرع بغداد</p>

                        </div>

                        <!-- <div class="col" sm="2" style="color:white;">
                      <p>0770 533 6662 </p>

                      <p style="position: relative; bottom: 22px">0750 555 3833</p>
                    </div> -->

                    <!-- <div class="col" style="color:white;">
                      <p style="margin-left: -20px !important; margin-top: 8px !important;">
                          فرع الموصل</p>

                        </div>

                        <div class="col" style="color:white;">
                      <p>0770 344 6662</p>
                      <p style="position: relative; bottom: 22px">0770 344 6662</p>
                    </div>

                    <div class="col " style="color:white;">
                      <p style="margin-left: -20px !important; margin-top: 8px !important;">
                          فرع دهوك</p>

                        </div> -->

                        <div class="col mt-3" style="    display: grid;     position: relative;
                        left: 314px;">
                      <img src="./assets/instagram.png" alt="Company logo"
                          style="max-height: 22px;" />
                      <img src="./assets/facebook.png" alt="Company logo"
                          style="max-height: 21px; position:relative; bottom: 13px; " />
                        </div>

             <div class="col mt-3"  style=" color: white;
             position: relative;
             left: 192px;
         ">

                      <p style="    margin-left: -96px !important; "> vantage.iq</p>
                      <p
                          style="    margin-left: -96px !important; position: relative; bottom: 15px">
                         vantage.iq</p>

             </div>

            </div>

          </div>
      </div>


  </div></v-html>
     
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </b-container>
  </div>
</template>

<script>
import Vue from 'vue';

import VueHtmlToPaper from "vue-html-to-paper";
 
  

    Vue.use(VueHtmlToPaper);

   export default {
      el: '#app',
      data () {
        return {
          amount:'',
          date:'',
          client:'',
          lettersAmount:'',
          direction:'',
          level:'',
          flatNo:'',
          area:'',
          price:'',
          delivered:'',
          due:'',
          manager:'',
          accountant:'',
          buildingNo:'',
          receiptNo:'',
       

          globalOptions: {
            name: '_blank',
            specs: [
              'fullscreen=yes',
              'titlebar=yes',
              'scrollbars=yes'
            ],
            styles: [
              'https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css',
              'https://unpkg.com/kidlat-css/css/kidlat.css'
            ],
            timeout: 1000,
            autoClose: true,
            windowTitle: window.document.title, // whatever's the window title of the opener
          },
          localLandScapeOptions: {
            styles: [
              'https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css',
              'https://unpkg.com/kidlat-css/css/kidlat.css',
              'public/landscape.css', // must be the path of your public folder
            ]
          }
        }
      },
      methods: {
       
   print () {
 
const prtHtml = document.getElementById('printMe').innerHTML;

// Get all stylesheets HTML
let stylesHtml = '';
for (const node of [...document.querySelectorAll('link[rel="stylesheet"], style')]) {
  stylesHtml += node.outerHTML;
}

// Open the print window
const WinPrint = window.open('', '', 'left=0,top=0,width=800,height=900,toolbar=0,scrollbars=0,status=0');

WinPrint.document.write(`<!DOCTYPE html>
<html>
  <head>
    ${stylesHtml}
  </head>
  <body>
    ${prtHtml}
  </body>
</html>`);


WinPrint.focus();
WinPrint.print();

   window.setTimeout(() => {WinPrint.focus(); WinPrint.print()}, 500)

        },
       
       
      },
   };
  </script>


<style>
@import url('https://fonts.googleapis.com/css2?family=Tajawal:wght@500&display=swap');*{font-family: 'Tajawal', sans-serif;}

.header {
    /* background: linear-gradient(87deg, #172b4d 0, #1d2026 100%) !important;*/
    background-image: url('./assets/newLOgo-white.png') !important;
    background-repeat: no-repeat;
    background-repeat: no-repeat !important;
    background-size: cover !important;
    height: max-content !important;
    background-position: bottom !important;
}
p{
  font-size: 15px !important;
  color: white;
}
.paid-input{
      width: 100%;
    padding: 15px;
    border-radius: 11px;
    border: none;
}
#printMe{
  display: none;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}


.table-bordered td,
.table-bordered th {
    border: 1px solid #000000 !important;
}

table thead {
    vertical-align: bottom;
    padding: 0px !important;
    border-bottom: 2px solid #dee2e6;
}

</style>