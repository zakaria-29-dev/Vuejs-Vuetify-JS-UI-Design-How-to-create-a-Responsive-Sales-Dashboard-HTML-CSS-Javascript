<template>
  <v-app :style="{ background: $vuetify.theme.themes.dark.background }">
    <SideBar :drawer="drawer" />
    <RightSideBar />
    <v-container>
      <v-toolbar flat color="rgba(0,0,0,0)">
        <v-btn
          icon
          dark
          class="d-lg-none d-xl-flex"
          @click.stop="drawer = !drawer"
        >
          <v-icon>mdi-menu</v-icon>
        </v-btn>
        <v-spacer></v-spacer>
        <v-text-field
          label="Search on maufarm"
          class="pt-5 d-none d-sm-flex"
          dark
          filled
          prepend-inner-icon="mdi-magnify"
          solo
          flat
          background-color="transparent"
          rounded
          outlined
        ></v-text-field>
        <v-spacer></v-spacer>
        <v-btn dark class="mr-2">
          <v-icon left>fas fa-filter</v-icon>
          Filtre
        </v-btn>
        <v-btn dark class="mr-2">
          <v-icon left>fas fa-upload</v-icon>
          Export
        </v-btn>
      </v-toolbar>
      <h1 class="white--text">SALES</h1>
      <p class="grey--text">
        A Great Way To Generate All The Motivation You Need To Get Fit
      </p>
      <v-app-bar dark color="rgba(0,0,0,0)" flat class="">
        <v-tabs color="#6F0DFF">
          <v-tabs-slider color="#6F0DFF"></v-tabs-slider>

          <v-tab class="withoutupercase">Fultillment Status View</v-tab>
          <v-tab class="withoutupercase">Real-time Trackning</v-tab>
          <v-tab class="withoutupercase">Sales View</v-tab>
          <v-tab class="withoutupercase">Balances</v-tab>
          <v-tab class="withoutupercase">Transactions</v-tab>
          <v-tab class="withoutupercase">Engagement Rate</v-tab>
        </v-tabs>
        <v-spacer></v-spacer>
        <v-btn dark text class="d-none d-sm-flex">
          <v-icon left>mdi-magnify</v-icon>
          SEARCH
        </v-btn>
        <v-btn rounded color="white" class="black--text">
          List
          <v-icon right>mdi-format-list-bulleted</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon>mdi-apps</v-icon>
        </v-btn>
      </v-app-bar>
      <v-divider color="grey"></v-divider>
      <v-toolbar flat color="rgba(0,0,0,0)">
        <v-divider vertical color="green" inset></v-divider>
        <v-toolbar-title class="white--text ml-4">Alert</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-chip
          class="ma-1 d-none d-sm-flex"
          color=""
          label
          text-color="white"
          dark
        >
          <v-avatar color="white" rounded class="mr-2">
            <v-img src="1.png" contain></v-img>
          </v-avatar>
          Nike new golf
        </v-chip>
        <v-chip
          class="ma-1 d-none d-sm-flex"
          color=""
          label
          text-color="white"
          dark
        >
          <v-avatar color="white" rounded class="mr-2">
            <v-img src="2.png" contain></v-img>
          </v-avatar>

          Sneakers printemps
        </v-chip>
        <v-spacer></v-spacer>
        <v-btn dark class="mr-2 withoutupercase d-none d-sm-flex">
          See All (10)
        </v-btn>
        <v-btn dark class="mr-2" outlined>
          <v-icon left>mdi-chevron-left</v-icon>
          <v-icon right>mdi-chevron-right</v-icon>
        </v-btn>
      </v-toolbar>
      <v-row class="mt-n14">
        <v-col
          cols="12"
          xs="12"
          sm="6"
          md="4"
          lg="3"
          v-for="(shoe, i) in shoes"
          :key="i"
        >
          <v-card
            class="mx-auto my-12 rounded-xl"
            max-width="374"
            color="#151515"
          >
            <v-img height="170" :src="shoe.image"></v-img>
            <v-toolbar color="transparent" class="mt-n7" flat>
              <v-avatar color="white" rounded class="mr-2">
                <v-img :src="shoe.pic" contain></v-img>
              </v-avatar>
              <v-spacer></v-spacer>
              <v-avatar color="black" rounded class="mr-2" dark>
                <div class="three">
                  <div class="four">
                    <span class="white--text caption">{{ shoe.price }}</span>
                  </div>
                  <div class="five">
                    <span class="green--text caption">HOLD</span>
                  </div>
                </div>
              </v-avatar>
            </v-toolbar>
            <v-card-title class="grey--text caption">{{
              shoe.id
            }}</v-card-title>
            <v-card-title class="grey--text text-grey-darken-1 caption mt-n6">{{
              shoe.date
            }}</v-card-title>
            <v-card-text class="white--text text-grey-darken-1 mt-n2">{{
              shoe.marque
            }}</v-card-text>

            <v-card-text class="mt-n4">
              <v-chip-group
                active-class="deep-purple accent-4 white--text"
                column
              >
                <v-chip label dark>{{ shoe.pay1 }}</v-chip>
                <v-chip label dark>{{ shoe.pay2 }}</v-chip>
                <v-spacer></v-spacer>
                <v-avatar size="40">
                  <v-img :src="shoe.avatar"></v-img>
                </v-avatar>
              </v-chip-group>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
      <v-toolbar flat color="rgba(0,0,0,0) " class="mt-n14">
        <v-divider vertical color="orange" inset></v-divider>
        <v-toolbar-title class="white--text ml-4"
          >Recent Orders</v-toolbar-title
        >
        <v-spacer></v-spacer>
        <v-chip
          class="ma-1 d-none d-sm-flex"
          color=""
          label
          text-color="white"
          dark
        >
          <v-avatar color="white" rounded class="mr-2">
            <v-img src="2.png" contain></v-img>
          </v-avatar>
          Nike new
        </v-chip>
        <v-chip
          class="ma-1 d-none d-sm-flex"
          color=""
          label
          text-color="white"
          dark
        >
          <v-avatar color="white" rounded class="mr-2">
            <v-img src="3.png" contain></v-img>
          </v-avatar>

          Zoom JO
        </v-chip>
        <v-chip
          class="ma-1 d-none d-sm-flex"
          color=""
          label
          text-color="white"
          dark
        >
          <v-avatar color="white" rounded class="mr-2">
            <v-img src="4.png" contain></v-img>
          </v-avatar>

          Jordon BZ
        </v-chip>
        <v-spacer></v-spacer>
        <v-btn dark class="mr-2 withoutupercase d-none d-sm-flex">
          See All (129)
        </v-btn>
        <v-btn dark class="mr-2" outlined>
          <v-icon left>mdi-chevron-left</v-icon>
          <v-icon right>mdi-chevron-right</v-icon>
        </v-btn>
      </v-toolbar>
      <v-row class="mt-n10">
        <v-col
          cols="12"
          xs="12"
          sm="6"
          md="3"
          v-for="(order, i) in orders"
          :key="i"
        >
          <v-card
            class="mx-auto my-12 rounded-lg"
            max-width="374"
            color="#151515"
          >
            <v-toolbar color="transparent" class="mt-n6" flat>
              <v-avatar color="white" rounded class="mr-2">
                <v-img :src="order.pic" contain></v-img>
              </v-avatar>
              <v-spacer></v-spacer>
              <v-avatar color="black" rounded class="mr-2" dark>
                <div class="three">
                  <div class="four">
                    <span class="white--text caption">{{ order.price }}</span>
                  </div>
                  <div class="six">
                    <span class="orange--text caption">HOLD</span>
                  </div>
                </div>
              </v-avatar>
            </v-toolbar>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
import RightSideBar from "../components/RightSideBar.vue";
import SideBar from "../components/SideBar";

export default {
  name: "Home",
  data: () => ({
    selection: 1,
    drawer: true,
    shoes: [
      {
        image: "3.jpg",
        pic: "1.png",
        price: "$465",
        id: "ID: CK1911159967352",
        date: "02.12.2021, 3:34 AM",
        marque: "Nike Air MAx",
        pay1: "LUXEMBURG",
        pay2: "ITALY",
        avatar: "https://cdn.vuetifyjs.com/images/lists/1.jpg",
      },
      {
        image: "9.jfif",
        pic: "2.png",
        price: "$714",
        id: "ID: CK1911159967621",
        date: "02.12.2021, 4:12 AM",
        marque: "AIR Jordon",
        pay1: "FUTURE",
        pay2: "WAR",
        avatar: "https://cdn.vuetifyjs.com/images/lists/2.jpg",
      },
      {
        image: "8.jpg",
        pic: "3.png",
        price: "$982",
        id: "ID: CK1911159967532",
        date: "02.12.2021, 6:24 AM",
        marque: "Adidas GR",
        pay1: "LONDON",
        pay2: "ALGERIA",
        avatar: "https://cdn.vuetifyjs.com/images/lists/3.jpg",
      },
      {
        image: "7.jpg",
        pic: "4.png",
        price: "$394",
        id: "ID: CK1911159968663",
        date: "02.12.2021, 7:51 AM",
        marque: "Puma New",
        pay1: "SRILANKA",
        pay2: "PALAU",
        avatar: "https://cdn.vuetifyjs.com/images/lists/4.jpg",
      },
    ],
    orders: [
      {
        pic: "5.png",
        price: "$465",
      },
      {
        pic: "6.png",
        price: "$714",
      },
      {
        pic: "7.png",
        price: "$982",
      },
      {
        pic: "8.png",
        price: "$394",
      },
    ],
  }),
  components: {
    SideBar,
    RightSideBar,
  },
  methods: {},
};
</script>
<style scoped>
.v-tab.withoutupercase {
  text-transform: none !important;
}
.v-tabs {
  width: 50% !important;
}
.v-btn.withoutupercase {
  text-transform: none !important;
}
/*div{
  display:inline-block;
  float:left;
  color:#fff;
  font-size:10px;
}*/

.three {
  width: 50px;
  height: 50px;
}

.four {
  width: 50px;
  height: 25px;
  background: black;
}
.five {
  width: 50px;
  height: 25px;
  background: #042a0f;
}
.six {
  width: 50px;
  height: 25px;
  background: #2c2107;
}
</style>
