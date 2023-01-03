<template>
    <v-container fluid>
       <v-card color="#3853D8" height="150px" tile flat class="f-flex align-center justify-center" dark>
        <v-row>
            <v-col cols="12" sm="12">
               <h4 class="text-white text-center mt-14">MEN'S LIFESIYLE SHOES</h4> 
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
                    <v-col cols="12" class="pl-8 pt-5">
                       <v-btn color="black" dark class="withoutupercase" small tile>
                        nuw
                       </v-btn> 
                       <h6 class="text-white mt-8">MOUNTAIN BIKE</h6>
                       <h3 class="text-white mt-5">Trek Speed Concept</h3>
                    </v-col>
                   </v-row>
                </v-card>
            </v-col>
           </v-row>
       </v-card>
    </v-container>
</template>

<script>

export default {
    data: () => ({
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
        ]
    })
};
</script>

<style>
.container {
    padding: 0px !important;
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