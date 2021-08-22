<template>
  <div class="sub-header">
    <v-row
      class="p-2 mt-0 ml-0 mr-0 mb-0"
      justify="space-between"
      align="center"
    >
      <NuxtLink
        v-for="(item, index) in items"
        :key="index"
        :to="item.url"
        class="sub-header__link text-decoration-none white--text pa-3 col-2 text-center"
      >
        {{ item.title }}
      </NuxtLink>
    </v-row>
  </div>
</template>

<script>
export default {
  data: () => ({
    items: [
      { title: "ABOUT", url: "#" },
      { title: "Jewelry", url: "#" },
      { title: "VIDEO", url: "#" },
      { title: "COLLECTION", url: "#" },
      { title: "EXPERIENCE", url: "#" },
      { title: "FOllow Us", url: "#" }
    ]
  })
};
</script>

<style>
.sub-header {
  background: rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(5px);
}
.sub-header__link {
  border: 1px solid rgba(155, 155, 155, 0.39);
  font-family: Montserrat, sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 20px;
  text-transform: uppercase;
  color: #ffffff;
}
</style>
