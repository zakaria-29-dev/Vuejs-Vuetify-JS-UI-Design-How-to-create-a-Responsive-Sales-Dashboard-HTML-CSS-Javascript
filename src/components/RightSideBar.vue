<template>
  <v-navigation-drawer
    v-model="drawer1"
    app
    color="#000000"
    mini-variant
    mini-variant-width="110"
    right
  >
    <v-avatar class="d-block text-center mx-auto mt-4 mb-10" size="80">
      <v-btn class="ma-2" outlined large fab color="white"> SH </v-btn>
    </v-avatar>

    <v-card flat color="#6F0DFF" class="rounded-xl mx-4 py-10 text-center top">
      <v-btn icon dark class="mb-5">
        <v-icon>fas fa-sort-amount-up-alt</v-icon>
      </v-btn>
      <span class="white--text">Create<br />Order</span>
    </v-card>

    <div
      style="
        position: absolute;
        bottom: 20px;
        margin-left: auto;
        margin-right: auto;
        left: 0;
        right: 0;
        text-align: center;
      "
    >
      <v-btn dark class="changewith mb-3">
        <v-icon class="">mdi-bell</v-icon> </v-btn
      ><br />
      <v-badge bordered color="#6F0DFF" dot overlap>
        <v-btn dark class="changewith">
          <v-icon class="">mdi-android-messages</v-icon>
        </v-btn>
      </v-badge>
    </div>
  </v-navigation-drawer>
</template>

<script>
export default {
  data: () => ({
    selectedItem: 0,
    drawer1: null,
  }),
};
</script>

<style>
.v-btn:not(.v-btn--round).v-size--default.changewith {
  height: 45px !important;
  min-width: 30px !important;
  padding: 0 12px;
}
.top {
  margin-top: 150px;
}
</style>
