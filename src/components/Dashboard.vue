<template>
  <v-container fluid>
    <v-card
      color="#3853D8"
      height="150px"
      tile
      flat
      class="d-flex align-center justify-center"
      dark
    >
      <v-row>
        <v-col cols="12" sm="12">
          <h4 class="text-center">MEN'S LIFESTYLE SHOES</h4>
        </v-col>
        <v-col cols="12" sm="12">
          <v-breadcrumbs :items="items" class="justify-center mt-n7" dark>
            <template v-slot:divider>
              <v-icon color="#7C92FE">mdi-chevron-right</v-icon>
            </template>
          </v-breadcrumbs>
        </v-col>
      </v-row>
    </v-card>
    <v-card tile class="mx-16 mt-n10 card1" color="white">
      <v-row>
        <v-col cols="12" sm="8" class="pr-0">
          <v-card height="250px" tile flat color="#3890D8">
            <v-row>
              <v-col cols="12" sm="4" class="pl-8 pt-5">
                <v-btn color="black" dark class="withoutupercase" small tile>
                  new
                </v-btn>
                <h6 class="white--text mt-8">MOUNTAIN BIKE</h6>
                <h3 class="white--text mt-8">Trek Speed Concept</h3>
                <v-btn
                  rounded
                  color="#4C9CDB"
                  dark
                  class="withoutupercase px-8 mt-10"
                >
                  More Info
                </v-btn>
              </v-col>
              <v-cols cols="12" sm="8">
                <v-img
                  src="bike.png"
                  max-height="400"
                  max-width="400"
                  contain
                  class="mt-n4"
                ></v-img>
              </v-cols>
            </v-row>
          </v-card>
        </v-col>
        <v-col cols="12" sm="4" class="pl-0">
          <v-card height="250px" tile flat color="#6857E1">
            <v-row>
              <v-col cols="12" sm="6" class="pl-8 pt-5">
                <v-btn color="black" dark class="withoutupercase" small tile>
                  new
                </v-btn>
                <h6 class="white--text mt-8">DOWN JACKET</h6>
                <h3 class="white--text mt-8">Sale Collection 2022</h3>
                <v-btn
                  rounded
                  color="#8375E7"
                  dark
                  class="withoutupercase px-8 mt-3"
                >
                  More Info
                </v-btn>
              </v-col>
              <v-cols cols="12" sm="6">
                <v-img
                  src="jacket2.png"
                  max-height="400"
                  max-width="200"
                  contain
                  class="mt-n2"
                ></v-img>
              </v-cols>
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
              <v-icon color="#3853D8"> mdi-sync </v-icon>
            </v-btn>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n6 px-0">
          <v-toolbar flat outlined>
            <v-toolbar-title>
              SPORT BY: <span>Price $-$$</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn icon class="mr-4">
              <v-icon color="black">mdi-menu-down</v-icon>
            </v-btn>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n6 px-0">
          <v-toolbar flat outlined>
            <v-toolbar-title> SHOW: <span>12</span> </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn icon class="mr-4">
              <v-icon color="black">mdi-menu-down</v-icon>
            </v-btn>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n6 pl-0">
          <v-toolbar flat outlined>
            <v-btn icon class="mr-4">
              <v-icon color="black">mdi-apps</v-icon>
            </v-btn>
            <v-divider vertical></v-divider>
            <v-btn icon class="mr-4">
              <v-icon color="grey">mdi-format-list-bulleted</v-icon>
            </v-btn>
            <v-divider vertical></v-divider>
            <v-toolbar-title class="ml-2">
              <strong>COMPARE :</strong>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-badge color="#3853D8" content="3" class="mr-2"></v-badge>
          </v-toolbar>
        </v-col>
        <v-col cols="3" class="py-0 pr-0 mt-n3">
          <v-card flat outlined tile>
            <v-toolbar flat>
              <v-icon color="black" class="mr-2">mdi-chevron-down</v-icon>
              <strong>CATEGORIES</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon>
            </v-toolbar>
            <v-list dense class="mt-n5">
              <v-list-item v-for="style in styles" :key="style.title">
                <v-list-item-content>
                  <v-list-item-title
                    v-text="style.title"
                    class="ml-8"
                  ></v-list-item-title>
                </v-list-item-content>
                <v-list-item-action>
                  <v-list-subtitle v-text="style.count"></v-list-subtitle>
                </v-list-item-action>
              </v-list-item>
            </v-list>
          </v-card>
          <v-card flat outlined tile>
            <v-toolbar flat>
              <v-icon color="black" class="mr-2">msi-chevron-down</v-icon>
              <strong>PRICE</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon>
            </v-toolbar>
            <v-toolbar flat>
              <v-text-field
                placeholder="$ 50"
                filled
                rounded
                dense
                class="mx-2"
              ></v-text-field>
              <v-text-field
                placeholder="$ 1900"
                filled
                rounded
                dense
                class="mx-2"
              ></v-text-field>
            </v-toolbar>
            <v-range-slide color="blue" max="40" min="-30"></v-range-slide>
          </v-card>
          <v-card flat outlined tile>
            <v-toolbar flat>
              <v-icon color="black" class="mr-2">mdi-chevron-down</v-icon>
              <strong>BRAND</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon>
            </v-toolbar>
            <v-list dense class="mt-n-5">
              <v-list-item v-for="brand in brands" :key="brand.title">
                <v-list-item-content>
                  <v-list-item-title
                    v-text="brand.title"
                    class="ml-6"
                  ></v-list-item-title>
                </v-list-item-content>
                <v-list-item-action>
                  <v-checkbox
                    color="primary"
                    v-model="brand.state"
                  ></v-checkbox>
                </v-list-item-action>
              </v-list-item>
            </v-list>
          </v-card>
          <v-card flat outlined tile>
            <v-toolbar flat>
              <v-icon color="black" class="mr-2">mdi-chevron-down</v-icon>
              <strong>COLOR</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon>
            </v-toolbar>
            <v-chip-group column multiple>
              <v-chip
                filter
                outlined
                color="black"
                text-color="black"
                class="ml-2"
              ></v-chip>
              <v-chip
                filter
                color="#E6E6E6"
                text-color="black"
                class="ml-2"
              ></v-chip>
              <v-chip
                filter
                color="#FFB500"
                text-color="white"
                class="ml-2"
              ></v-chip>
              <v-chip
                filter
                color="#F44336"
                text-color="white"
                class="ml-2"
              ></v-chip>
              <v-chip
                filter
                color="#3F51B5"
                text-color="white"
                class="ml-2"
              ></v-chip>
              <v-chip
                filter
                color="#2196F3"
                text-color="white"
                class="ml-2"
              ></v-chip>
              <v-chip
                filter
                color="#009688"
                text-color="white"
                class="ml-2"
              ></v-chip>
              <v-chip
                filter
                color="#4CAF50"
                text-color="white"
                class="ml-2"
              ></v-chip>
              <v-chip
                filter
                color="#FF9800"
                text-color="white"
                class="ml-2"
              ></v-chip>
              <v-chip
                filter
                color="#9C27B0"
                text-color="white"
                class="ml-2"
              ></v-chip>
              <v-chip
                filter
                color="#673AB7"
                text-color="white"
                class="ml-2"
              ></v-chip>
              <v-chip
                filter
                color="#3F51B5"
                text-color="white"
                class="ml-2"
              ></v-chip>
            </v-chip-group>
          </v-card>
          <v-card>
            <v-toolbar flat>
              <v-icon color="black" class="mr-2">mdi-chevron-down</v-icon>
              <strong>SIZE</strong>
              <v-spacer></v-spacer>
              <v-icon color="grey" small>mdi-close</v-icon>
            </v-toolbar>
            <v-chip-group
              column
              multiple
              active-class="blue white--text"
              class="ml-2"
            >
              <v-chip
                v-for="size in sizes"
                :key="size"
                :value="size"
                class="size"
              >
                {{ size }}
              </v-chip>
            </v-chip-group>
          </v-card>
        </v-col>
        <v-col cols="9" class="mt-n3">
          <v-row>
            <v-col
              cols="12"
              sm="4"
              v-for="(clothe, i) in clothes"
              :key="i"
              :class="clothe.class"
            >
              <v-hover v-slot:default="{ hover }">
                <v-card height="300" align="center" flat outlined tile>
                  <v-card-actions>
                    <v-spacer></v-spacer>
                    <v-btn color="black" small dark>{{ clothe.sold }}</v-btn>
                  </v-card-actions>
                  <v-img :src="clothe.image" width="200" height="200" contain />
                  <v-card-text class="mt-n4">
                    <strong :class="hover ? 'red--text' : 'black--text'">{{
                      clothe.title
                    }}</strong>
                  </v-card-text>
                  <v-expand-transition>
                    <div
                      v-if="hover"
                      class="d-flex transition-fast-in-fast-out blue v-card--reveal display-3 white--text"
                      style="height: 100%"
                    >
                      <v-btn rounded color="white">
                        <v-icon>mdi-cart-outlined</v-icon>Buy
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
          </v-row>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n3 pr-0 pb-0">
          <v-toolbar flat outlined></v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n3 pr-0 pb-0">
          <v-toolbar flat outlined>
            <v-btn icon class="mr-1">
              <v-icon>mdi-chevron-up</v-icon>
            </v-btn>
            <v-divider vertical></v-divider>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n3 pr-0 pb-0">
          <v-toolbar flat outlined>
            <v-pagination v-model="page" :length="4"></v-pagination>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n3 pl-0 pb-0">
          <v-toolbar flat outlined>
            <v-btn icon class="mr-1">
              <v-icon>mdi-chevron-down</v-icon>
            </v-btn>
            <v-divider vertical></v-divider>
          </v-toolbar>
        </v-col>
      </v-row>
    </v-card>
    <v-card
      color="#EFF0F2"
      height="250px"
      tile
      flat
      dark
      class="d-flex align-center justify-center mt-n10 card2"
    >
      <v-row>
        <v-col cols="12" sm="12">
          <h4 class="text-center black--text mt-10">
            SUBSCRIBE TO OUR NEWSLETTER
          </h4>
        </v-col>
        <v-col cols="12" sm="12">
          <h6 class="text-center grey--text">
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quae autem
            earum, quo aperiam vel numquam porro laboriosam sit, adipisci odit
            quam quasi voluptatum asperiores quisquam, magni cum fugiat
            recusandae. Necessitatibus?
          </h6>
        </v-col>
        <v-col cols="12" sm="12">
          <v-card flat color="transparent" class="d-flex justify-center">
            <v-text-field
              placeholder="Enter Your Email"
              rounded
              class="shrink"
              background-color="grey"
              filled
              apped-icon="mdi-email-outline"
              dense
            ></v-text-field>
          </v-card>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    page: 1,
    items: [
      {
        text: "Home",
        disabled: false,
        href: "breadcrumbs_home",
      },
      {
        text: "Catalog",
        disabled: false,
        href: "breadcrumbs_catalog",
      },
      {
        text: "Men",
        disabled: false,
        href: "breadcrumbs_men",
      },
      {
        text: "Shoes",
        disabled: false,
        href: "breadcrumbs_shoes",
      },
    ],
    styles: [
      {
        title: "Football",
        count: 23,
      },
      {
        title: "Treasure",
        count: 12,
      },
      {
        title: "Office",
        count: 15,
      },
      {
        title: "Casual",
        count: 10,
      },
      {
        title: "Sport",
        count: 20,
      },
      {
        title: "Outdoor",
        count: 10,
      },
      {
        title: "Party",
        count: 32,
      },
      {
        title: "Running",
        count: 23,
      },
      {
        title: "Training",
        count: 12,
      },
      {
        title: "GYM",
        count: 15,
      },
    ],
    brands: [
      {
        title: "Fifestyle",
        state: true,
      },
      {
        title: "Running",
        state: false,
      },
      {
        title: "Trainig & Gym",
        state: true,
      },
      {
        title: "Basketball",
        state: false,
      },
    ],
    sizes: [
      "35",
      "36",
      "37",
      "38",
      "39",
      "40",
      "41",
      "42",
      "43",
      "44",
      "45",
      "46",
    ],
    clothes: [
      {
        class: "pa-0",
        sold: "-20%",
        image: "1.png",
        title: "KD 8 EXT",
        price: "$ 145.00",
      },
      {
        class: "pa-0",
        sold: "-16%",
        image: "2.png",
        title: "Jordan",
        price: "$ 190.00",
      },
      {
        class: "pa-0",
        sold: "-20%",
        image: "3.png",
        title: "Nike",
        price: "$ 145.00",
      },
      {
        class: "pa-0",
        sold: "-16%",
        image: "4.png",
        title: "Adidas",
        price: "$ 190.00",
      },
      {
        class: "pa-0",
        sold: "-20%",
        image: "5.png",
        title: "Puma",
        price: "$ 145.00",
      },
      {
        class: "pa-0",
        sold: "-16%",
        image: "6.png",
        title: "New Balance",
        price: "$ 190.00",
      },
      {
        class: "pa-0",
        sold: "-20%",
        image: "7.png",
        title: "Converse",
        price: "$ 145.00",
      },
      {
        class: "pa-0",
        sold: "-16%",
        image: "8.png",
        title: "Vans",
        price: "$ 190.00",
      },
      {
        class: "pa-0",
        sold: "-20%",
        image: "9.png",
        title: "Reebok",
        price: "$ 145.00",
      },
      {
        class: "pa-0",
        sold: "-16%",
        image: "10.png",
        title: "New Balance",
        price: "$ 190.00",
      },
      {
        class: "pa-0",
        sold: "-20%",
        image: "11.png",
        title: "Converse",
        price: "$ 145.00",
      },
      {
        class: "pa-0",
        sold: "-16%",
        image: "12.png",
        title: "Vans",
        price: "$ 190.00",
      },
    ],
  }),
};
</script>

<style>
.container {
  padding: 0 !important;
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
  opacity: 0.5;
  position: absolute;
  width: 100%;
}
.card1 {
  z-index: 10;
}
.card2 {
  z-index: 1;
}
</style>
