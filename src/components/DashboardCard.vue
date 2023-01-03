<template>
    <v-container fluid>
       <v-card color="#3853D8" height="150px" tile flat class="f-flex align-center justify-center" dark>
        <v-row>
            <v-col cols="12" sm="12">
               <h4 class="text-center">MEN'S LIFESIYLE SHOES</h4> 
            </v-col>

            <v-col cols="12" sm="12">
                <v-breadcrumbs :items="items" class="justify-center mt-n1" dark >
                   <template v-slot:divider>
                    <v-icon color="#7C92FE">mdi-chevron-right</v-icon>
                   </template>
                </v-breadcrumbs>
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
</style>