<template>

  <v-app class="my-0 fluid">

    <v-main>
      <v-container class="my-10 py-0">


    <div class="justify-center mx-lg-16 mx-10">
      <p class="font-weight-bold text-center m2gin" width="50%">Family Tree</p>
      <h3 class="font-weight-bold text-center m2gin">Pomparan Op. Jaksa Juda Hutasoit / Sinta Mauli br. Siregar         
      </h3>
      <p class="text-center m2gin">
        Silsilah hubungan/relationship atau garis keturunan dari Op. Jaksa Juda Hutasoit / Sinta Mauli br. Siregar         
      </p>
    </div>
    
      <VueFamilyTree class="vue-family-tree" :tree="tree" @card-click="dialog == true">
        <template v-if="customCard" v-slot:card="{item}">
          <div class="custom-card" @click="dialog=true">
          <div :style="{backgroundImage: item.image ? `url(${item.image})` :  null}" class="custom-card__image" />
          <div class="custom-card__info">
            <div class="custom-card__name">
              {{ item.name }}
            </div>
            <div v-show="item.age"  class="custom-card__age">
              Age: {{ item.age }}
            </div>
            <div v-show="item.status"  class="custom-card__age">
              Status: {{ item.status }}
            </div>
            <div>
            </div>
          </div>
        </div>
        </template>
         
         <v-dialog  v-model= "dialog" max-width="600px">
     <template v-slot:activator="{ on }">
       <v-btn  v-on="on" x-small class="button-props">Detail</v-btn>
     </template>
    <v-card>
      <v-card-title>
        <h2>Add a New Project</h2>
      </v-card-title>
      <div></div>
      <div></div>
      <div></div>
      <div></div>

    </v-card>
   </v-dialog>
      </VueFamilyTree>

        
  </v-container>
    </v-main>

  </v-app>
  
</template>



<script>
  import VueFamilyTree from "vue-family-tree";
  import judahutasoit from '../assets/Juda-Hutasoit.jpg'
  import sintamauli from '../assets/Sinta-Mauli.jpg'
  import nichole from '../assets/nichole.jpeg'
  import asri from '../assets/asri.jpeg'
  import rachel from '../assets/rachel.jpeg'
  import maria from '../assets/maria.jpeg'
  import charles from '../assets/charles.jpeg'
  import obor from '../assets/obor.jpeg'
  import arnold from '../assets/arnold.jpeg'
  import nora from '../assets/nora.jpeg'

  import toti from '../assets/totti.jpeg'
  import elsa from '../assets/elsa.jpeg'
  import richard from '../assets/richard.jpeg'
  import pretty from '../assets/pretty.jpeg'




  export default {
  name: 'familyTree',
  components: {    
    VueFamilyTree,
    },

  data() {
    return {
      customCard: true,
       dialog: false,

      tree: [
        
        {
           "firstPerson":{
              "name":"Jaksa Juda Hutasoit",
              "image":[judahutasoit],
              "status":"deceased",
              "age":"86"
           },
           "secondPerson":{
              "name":"Sinta Mauli br. Siregar",
              "image":[sintamauli],
              "status":"deceased",
              "age":"84"
           },
           "children":[
              {
                 "firstPerson":{
                    "name":"Mangatas Hutasoit",
                    "image":"",
                    "status":"deceased",
                    "age":"79"
                 },
                 "secondPerson":{
                    "name":"Rugun br. Naibaho ",
                    "image":"",
                    "status":"deceased",
                    "age":"81"
                 },
                 "children":[
                    {
                       "firstPerson":{
                          "name":"Nelly Perak H. br. Hutasoit",
                          "image":"",
                          "status":"alive",
                          "age":"81"
                       },
                       "secondPerson":{
                          "name":"P. Sagala",
                          "image":"",
                          "status":"deceased",
                          "age":"81"
                       },
                       "children":[
                          {
                             "firstPerson":{
                                "name":"Mopul Sagala",
                                "image":"",
                                "status":"alive",
                                "age":"37"
                             },
                             "secondPerson":{
                                "name":"Eka",
                                "image":"",
                                "status":"alive",
                                "age":"34"
                             }
                          },
                          {
                             "firstPerson":{
                                "name":"Rachel Carolina br. Sagala",
                                "image":[rachel],
                                "status":"alive",
                                "age":"37"
                             }
                          }
                       ]
                    },
                    {
                       "firstPerson":{
                          "name":"Nelson Hutasoit",
                          "image":"",
                          "status":"deceased",
                          "age":"81"
                       },
                       "secondPerson":{
                          "name":"Frida br. Sipahutar",
                          "image":"",
                          "status":"deceased",
                          "age":"79"
                       },
                       "children":[
                          {
                             "firstPerson":{
                                "name":"Asrida br. Hutasoit",
                                "image":[asri],
                                "status":"alive",
                                "age":"30"
                             }
                          },
                          {
                             "secondPerson":{
                                "name":"Maria br. Hutasoit",
                                "image":[maria],
                                "status":"alive",
                                "age":"28"
                             }
                          }
                       ]
                    },
                    {
                       "firstPerson":{
                          "name":"Ellen br. Hutasoit",
                          "image":[obor],
                          "status":"alive",
                          "age":"70"
                       },
                       "secondPerson":{
                          "name":"M. Sibuea",
                          "image":"",
                          "status":"deceased",
                          "age":"76"
                       },
                       "children":[
                          {
                             "firstPerson":{
                                "name":"Ellsa br. Sibuea",
                                "image":[elsa],
                                "status":"alive",
                                "age":"30"
                             },
                             "secondPerson":{
                                "name":"Richard Sinabariba",
                                "image":[richard],
                                "status":"alive",
                                "age":"30"
                             }
                          },
                          {
                             "firstPerson":{
                                "name":"Maell Rizky Sibuea",
                                "image":"",
                                "status":"alive",
                                "age":"28"
                             }
                          }
                       ]
                    },
                    {
                       "firstPerson":{
                          "name":"Tumpal hutasoit",
                          "image":"",
                          "status":"alive",
                          "age":"74"
                       },
                       "secondPerson":{
                          "name":"Posmelita br. Sinaga",
                          "image":"",
                          "status":"alive",
                          "age":"72"
                       },
                       "children":[
                          {
                             "firstPerson":{
                                "name":"Angel br. Hutasoit",
                                "image":"",
                                "status":"alive",
                                "age":"20"
                             }
                          },
                          {
                             "firstPerson":{
                                "name":"Anggraeni br. Hutasoit",
                                "image":"",
                                "status":"alive",
                                "age":"18"
                             }
                          },
                          {
                             "firstPerson":{
                                "name":"Jou Marito br. Hutasoit",
                                "image":"",
                                "status":"alive",
                                "age":"16 "
                             }
                          }
                       ]
                    },
                    {
                       "firstPerson":{
                          "name":"Ferry Hutasoit",
                          "image":"",
                          "status":"deceased",
                          "age":"56"
                       }
                    },
                    {
                       "firstPerson":{
                          "name":"Nora br. Hutasoit",
                          "image":[nora],
                          "status":"alive",
                          "age":"54"
                       },
                       "secondPerson":{
                          "name":"Carles Samosir",
                          "image":[charles],
                          "status":"alive",
                          "age":"55"
                       },
                       "children":[{

                        "firstPerson":{
                          "name": "Vania Miranda Br. Samosir",
                          "image": [],
                          "status": "alive",
                          "age": "25"
                        }
                        },
                        {
                          "firstPerson":{
                          "name": "Andrew Oethara Rungguan Samosir",
                          "image": [],
                          "status": "alive",
                          "age": "23"

                          }
                        },
                        {
                          "firstPerson":{
                          "name": "Geofry Noach Samosir",
                          "image": [toti],
                          "status": "alive",
                          "age": "20"

                          }
                        },
                        {
                          "firstPerson":{
                          "name": "Deang Tio Nicole br. Samosir",
                          "image": [nichole],
                          "status": "alive",
                          "age": "19"

                          }

                       }

                       ]
                    },
                    {
                       "firstPerson":{
                          "name":"Arnold Israel Hutasoit",
                          "image":[arnold],
                          "status":"alive",
                          "age":"54"
                       },
                       "secondPerson":{
                          "name":"E br. Sidabutar",
                          "image":"",
                          "status":"alive",
                          "age":"55"
                       }
                    },
                    {
                       "firstPerson":{
                          "name":"Pretty br. Hutasoit",
                          "image":[pretty],
                          "status":"alive",
                          "age":"51"
                       }
                    }
                 ]
              }
           ]
        }
      ],
    }
  },
  methods: {
    cardClick (item) {
      console.log(item);
    }
  }
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  font-size: 12px;

  margin-top: 0px;
  padding-top: 0px;
}

.text-center {
  text-align: center;
  margin-bottom: 32px;
}

.custom-card {
  display: flex;
  align-items: center;
  width: auto;
  min-width: 200px;
  padding: 16px;
  border: 1px solid #ddd;
  border-radius: 10px;
  box-sizing: border-box;
  background-color: #fff;
  cursor: pointer;
  box-shadow: 0 0 1px 2px rgba(#000, 0);
  transition: box-shadow .2s ease;
  &:hover {
    box-shadow: 0 0 8px 2px rgba(#000, .1);
  }
  &__image {
    flex: 0 0 auto;
    width: 60px;
    height: 60px;
    border-radius: 50%;
    background-color: #dedede;
    background-size: cover;
    background-position: 50%;
  }
  &__info {
    padding-left: 16px;

  }
  &__name {
    font-weight: 550;
    font-size: 12px;

  }
  &__age {
    margin-top: 4px;
    font-size: 12px;
  }
}
  .vue-family-tree > div{
    position: absolute;
    width: 100%;
    height: 100%;
    margin-top: 48px;
    margin-bottom: 24px;
   
    
  }

  
  .m2gin {
    margin-bottom: 12px !important;
  }




  .v-input {
    max-width: 150px  !important;
    width: 100%;
    height: 24px;

    border: none;
    border-radius: 16px;
    justify-content: center !important;



    &__control{
      width: 150px !important;
      height: 24px;

      justify-content: center;

    }

    &__slot {
      width: 150px;
      min-height: 32px !important;
      font-size: 12px;

    }


  }



</style>
