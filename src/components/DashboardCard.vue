<template>
  <div class="container pt-5">
    <v-card color="#3853D8" height="150px" tile flat class="f-flex align-center justify-center" dark>
      <v-row>
        <v-col cols="12" sm="12">
          <h4 class="text-white text-center mt-16">MEN'S LIFESIYLE SHOES</h4> 
        </v-col>
        
        <v-col cols="12" sm="12">
          <v-breadcrumbs :items="items" class="justify-center mt-n1 text-white" dark>
            <template v-slot:divider>
              <v-icon color="#7C92FE">mdi-chevron-right</v-icon>
            </template>
          </v-breadcrumbs>
        </v-col>
      </v-row>
    </v-card>
    <v-card tile class="mx-16 mt-n2 card1" color="white">
      <v-row>
        <v-col class="pr-0" cols="12" sm="8">
          <v-card height="250px" tile flat color="#3890D8">
            <v-row>
              <v-col cols="12" sm="6" class="pl-8 pt-5">
                <v-btn color="black" dark class="withoutupercase" small tile>
                  new
                </v-btn>
                <h6 class="text-white mt-8">MOUNTAIN BIKE</h6>
                <h3 class="text-white mt-5">Trek Speed Concept</h3>
                <v-btn class="withoutupercase px-8 mt-3 text-white" rounded color="#4C9CD8" dark>
                  More Info
                </v-btn>
              </v-col>
              <v-colo cols="12" sm="6">
                <v-img src="main1.jpg" height="300" width="300" contain class="mt-n2"></v-img>
              </v-colo>
            </v-row> 
          </v-card>
        </v-col>
        
        <v-col class="pl-0" cols="12" sm="4">
          <v-card height="250px" tile flat color="#6857E1">
            <v-row>
              <v-col cols="12" sm="6" class="pl-8 pt-5">
                <v-btn color="black" dark class="withoutupercase" small tile>
                  new
                </v-btn>
                <h6 class="text-white mt-8">DOWN JECKET</h6>
                <h5 class="text-white mt-5">Sale Collection 2015</h5>
                <v-btn class="withoutupercase px-8 mt-3 text-white" rounded color="#8375E7" dark>
                  More Info
                </v-btn>
              </v-col>
              <v-colo cols="12" sm="6">
                <v-img src="nikebg.jpg" height="300" width="180" contain></v-img>
              </v-colo>
            </v-row> 
          </v-card>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12" sm="3" class="mt-n6 pr-0">
          <v-toolbar flat outlined>
            <v-toolbar-title><strong>Filter</strong></v-toolbar-title>
            <v-spacer></v-spacer>
            <v-divider vertical></v-divider>
            <v-btn icon class="ml-1">
              <v-icon color="#3853D8">
                mdi-sync
              </v-icon>
            </v-btn>
          </v-toolbar>
        </v-col>
        
        <v-col cols="12" sm="3" class="mt-n6 px-0">
          <v-toolbar flat outlined>
            <v-title>SPORT BY:
              <span>Price $-$$</span>
            </v-title> 
            <v-spacer></v-spacer>
            <v-btn icon class="mr-4">
              <v-icon color="black" >mdi-menu-down</v-icon>
            </v-btn>
          </v-toolbar>
        </v-col>
        
        <v-col class="mt-n6 px-0" cols="12" sm="3">
          <v-toolbar flat outlined class="">
            <v-title>SHOW:<span> 12</span></v-title>
            <v-spacer></v-spacer>
            <v-btn icon class="mr-4">
              <v-icon color="black">mdi-icon-down</v-icon>
            </v-btn>
          </v-toolbar>
        </v-col>
        
        <v-col cols="12" sm="3" class="mt-n6 pl-0">
          <v-toolbar flat outlined>
            <v-btn icon class="mr-1">
              <v-icon color="#3853D8">mdi-apps</v-icon>
            </v-btn>
            <v-divider vertical></v-divider>
            <v-btn icon class="mx-1">
              <v-icon color="grey">mdi-format-list-bulleted</v-icon>
            </v-btn>
            <v-divider vertical></v-divider>
            <v-toolbar-tittle class="ml-2">
              <v-title>COMPARE :</v-title>
            </v-toolbar-tittle>
            <v-spacer></v-spacer>
            <v-badge color="#3853D8" content="3" class="mr-2"></v-badge>
          </v-toolbar>
        </v-col>
        
        <v-col cols="3" class="py-0 pr-0 mt-n3">
          <v-card flat outlined tile>
            <v-toolbar flat>
              <v-icon icon="black" class="mr-2">mdi-chevron-down</v-icon>
              <strong>CATEGORIES</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon> 
            </v-toolbar>
            <v-list dense class="mt-n5">
              <v-list-item v-for="style in styles" :key="style.title">
                <div class="d-flex justify-lg-space-between">
                  <v-list-item-content>
                    <v-list-item-title v-text="style.title" class="ml-8"></v-list-item-title>
                  </v-list-item-content>
                  
                  <v-list-item-action>
                    <v-list-item-item-sublitle v-text="style.count" class="ml-8"></v-list-item-item-sublitle>
                  </v-list-item-action>
                </div>
              </v-list-item>
            </v-list>
          </v-card>
          
          <v-card flat outlined tile>
            <v-toolbar flat>
              <v-icon class="mr-2" color="black">mdi-chevron-down</v-icon>
              <strong>PRICE</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon>
            </v-toolbar>
            
            <v-toolbar flat>
              <v-text-field placeholder="$50" filled rounded dense class="mx-2"></v-text-field>
              <v-text-field placeholder="$40" filled rounded dense class="mx-2"></v-text-field>
            </v-toolbar>
            
            <v-range-slider color="blue" max="40" min="-30"></v-range-slider>
          </v-card>
          
          <v-card flat outlined tile>
            <v-toolbar flat>
              <v-icon color="black" class="mr-2">mdi-chevron-down</v-icon>
              <strong>BRAND</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon>
            </v-toolbar>
            
            <v-list dense class="mt-5">
              <v-list-item v-for="brand in brands" :key="brand.title">
                <div class="d-flex justify-lg-space-between align-content-center">
                  <v-list-item-content>
                    <v-list-item-title v-text="brand.title" class="ml-6"></v-list-item-title>
                  </v-list-item-content>
                  
                  <v-list-item-action>
                    <v-checkbox color="primary" v-modal="brand.state"></v-checkbox>
                  </v-list-item-action>
                </div>
                
              </v-list-item>
            </v-list>
          </v-card>
          <v-card flat outlined>
            <v-toolbar flat>
              <v-icon color="black" class="mr-2">mdi-chevron-down</v-icon>
              <strong>COLOR</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon>
            </v-toolbar>
            <v-chip-group>
              <v-chip class="ml-2" color="black" text-color="black"></v-chip>
              <v-chip filter color="#E6E6E6" text-color="white"></v-chip>
              <v-chip filter color="#FFB500" text-color="white"></v-chip>
              <v-chip filter color="#F27229" text-color="white"></v-chip>
              <v-chip filter color="#EB3427" text-color="white"></v-chip>
              <v-chip filter color="#923FA3" text-color="white"></v-chip>
              <v-chip filter color="#EB3427"  text-color="white"></v-chip>
              <v-chip filter color="#5EB524" text-color="white"></v-chip>
              <v-chip filter color="#7C5F4D" text-color="white"></v-chip>
            </v-chip-group>
          </v-card>
          
          <v-card flat outlined>
            <v-toolbar flat>
              <v-icon color="black" class="mr-2">mdi-chevron-down</v-icon>
              <strong>SIZE</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon>
            </v-toolbar>
            <v-chip-group column multiple active-class="blue white--text" class="ml-2">
              <v-chip v-for="size in sizes" :key="size" :value="size" class="size">
                {{ size }}
              </v-chip>
            </v-chip-group>
          </v-card>
        </v-col>
        
        <v-col cols="9" class="mt-n3">
          <row class="d-flex flex-wrap">
            <v-col cols="12" sm="4" v-for="(clothe, i) in clothes" :key="i" class="clothe.class">
              <v-hover v-slot:default="{hover}">
                <v-card height="300" align="center">
                  <v-card-actions>
                    <v-spacer></v-spacer>
                    <v-btn color="black" small dark>{{clothe.solid}}</v-btn>
                  </v-card-actions>
                  <v-img width="100" height="170" contain :src="clothe.image" alt="product img"></v-img>
                  <v-card-text class="mt-n4">
                    <strong :class="hover ? `red--text` : `black--text`">{{clothe.title}}</strong>              
                  </v-card-text>
                  <strong small>{{ clothe.desc }}</strong>
                  
                  <!-- HOVER -->
                  <v-expand-transition>
                    <div v-if="hover" class="d-flex transition-fast-in-fast-out blue v-card--reveal display-3 white-text" style="height: 100%;">
                      <v-btn rounded color="white">
                        <v-icon>mdi-cart-outlined</v-icon>
                        Buy
                      </v-btn>
                      
                      <v-btn fab small color="white" class="ml-2">
                        <v-icon color="black">mdi-content-copy</v-icon>
                      </v-btn>
                      
                      <v-btn fab small color="white" class="ml-2">
                        <v-icon color="black">mdi-heart-outline</v-icon>
                      </v-btn>
                      
                    </div>
                  </v-expand-transition>
                </v-card>
              </v-hover>
            </v-col>
          </row>
        </v-col>

        <v-col cols="12" sm="3" class="mt-n3 pr-0 pb-0">
          <v-toolbar flat outlined>

          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n3 pr-0 pb-0">
          <v-toolbar flat outlined>
           <v-btn icon class="mr-1">
              <v-icon color="grey">mdi-chevron-up</v-icon>
           </v-btn>
           <v-divider vertical></v-divider>
           
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n3 px-0 pb-0">
          <v-toolbar flat outlined class="text-center">
            <v-pagination v-model="page" :length="4"></v-pagination>
          </v-toolbar>
        </v-col>

        
      </v-row>
    </v-card>
  </div>
</template>

<script>

export default {
  data: () => ({
    page: 1,
    items: [
    {
      text: "Home",
      disabled: false,
      href: "breadcrubs_home"
    },
    {
      text: "Catalog",
      disabled: false,
      href: "breadcrubs_catalog"
    },
    {
      text: "Men",
      disabled: false,
      href: "breadcrubs_men"
    },
    {
      text: "Shoes",
      disabled: false,
      href: "breadcrubs_shoes"
    },
    ],
    styles: [
    { title: 'Lifestyle',
    count: '1',
  },
  { title: 'Running',
  count: '23',
},
{ title: 'Training & Gym',
count: '45',
},
{ title: 'Basketball',
count: '11',
},
{ title: 'Football',
count: '15',
},
{ title: 'Soccer',
count: '32',
},
{ title: 'Baseball',
count: '8',
},
{ title: 'Golf',
count: '15',
},
{ title: 'Sketboarding',
count: '22',
},
],
brands: [
{ title: 'Lifestyle',
state: 'true',
},
{ title: 'Running',
state: 'false',
},
{ title: 'Training & Gem',
state: 'true',
},
{ title: 'Basketball',
state: 'false',
},
],
sizes: [
'35', '36', '37', '38', '39', '40', '41', '42', '43', '44', '45','46',
],
clothes: [
{ class: 'pa-0',
solid: '-8%',
image: 'nike__item2.png',
title: 'Bulbasaur',
desc: 'Lorem ipsum dolor sit amet',
},
{ class: 'pa-0',
solid: '-7%',
image: 'nike__item3.png',
title: 'KD 8 EXT',
desc: 'Lorem ipsum dolor sit amet',
},
{ class: 'pa-0',
solid: '-8%',
image: 'nike__item1.png',
title: 'KD 8 EXT',
desc: 'Lorem ipsum dolor sit amet',
},
{ class: 'pa-0',
solid: '-8%',
image: 'nike__item2.png',
title: 'KD 8 EXT',
desc: 'Lorem ipsum dolor sit amet',
},
{ class: 'pa-0',
solid: '-8%',
image: 'nike__item3.png',
title: 'KD 8 EXT',
desc: 'Lorem ipsum dolor sit amet',
},
{ class: 'pa-0',
solid: '-7%',
image: 'nike__item4.png',
title: 'KD 8 EXT',
desc: 'Lorem ipsum dolor sit amet',
},
{ class: 'pa-0',
solid: '-8%',
image: 'nike__item1.png',
title: 'KD 8 EXT',
desc: 'Lorem ipsum dolor sit amet',
},
{ class: 'pa-0',
solid: '-7%',
image: 'nike__item2.png',
title: 'KD 8 EXT',
desc: 'Lorem ipsum dolor sit amet',
},
{ class: 'pa-0',
solid: '-9%',
image: 'nike__item3.png',
title: 'KD 8 EXT',
desc: 'Lorem ipsum dolor sit amet',
},
{ class: 'pa-0',
solid: '-12%',
image: 'nike__item4.png',
title: 'KD 8 EXT',
desc: 'Lorem ipsum dolor sit amet',
},
{ class: 'pa-0',
solid: '-7%',
image: 'nike__item1.png',
title: 'KD 8 EXT',
desc: 'Lorem ipsum dolor sit amet',
},
{ class: 'pa-0',
solid: '-11%',
image: 'nike__item2.png',
title: 'KD 8 EXT',
desc: 'Lorem ipsum dolor sit amet',
},
],
})
}
</script>

<style>
.container {
  padding-top: 10px !important;
}
.v-btn.withoutupercase {
  text-decoration: none;
}
.v-chip.v-size--default {
  border-radius: 50px !important;
  font-size: 14px !important;
  height: 40px !important;
  width: 40px !important;
}
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: .5;
  position: absolute;
  widows: 100%;
}
.card1 {
  z-index: 10;
}
.card2 {
  z-index: 0;
}
</style>