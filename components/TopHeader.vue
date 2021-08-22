<template>
  <div class="top-header pt-3">
    <v-row
      class="pa-5 mt-0 px-16 mb-0"
      justify="space-between"
      align="center"
    >
      <NuxtLink to="#" class="top-header__link text-decoration-none white--text"
        >SHOP</NuxtLink
      >
      <img src="~/assets/img/logo 1.png" alt="logo" />
      <NuxtLink to="#" class="top-header__link text-decoration-none white--text"
        >MENU</NuxtLink
      >
    </v-row>
  </div>
</template>

<style>
.top-header {
  background: linear-gradient(180deg, #0f0f0f 0%, rgba(15, 15, 15, 0) 100%);
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
}
.top-header * {
  font-family: Montserrat, sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 22px;
  /* identical to box height */

  letter-spacing: 0.05em;

  color: rgba(255, 255, 255, 0.8);
}
</style>
