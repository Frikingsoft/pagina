<template>
  <div class="footer">
  <v-sheet color="#0d1117" elevation="3" rounded="lg">
    <v-tabs
      v-model="tab"
      :items="tabs"
      align-tabs="center"
      color="white"
      height="60"
      slider-color="#f78166"
    >
      <template v-slot:tab="{ item }">
        <v-tab
          :prepend-icon="item.icon"
          :text="item.text"
          :value="item.value"
          class="text-none"
        ></v-tab>
      </template>

      <template v-slot:item="{ item }">
        <v-tabs-window-item :value="item.value" class="pa-4">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore voluptatibus! Eaque cupiditate minima, at placeat totam, magni doloremque veniam neque porro libero rerum unde voluptatem!
        </v-tabs-window-item>
      </template>
    </v-tabs>
  </v-sheet>
  </div>
</template>
<script setup>
  import { ref } from "vue"
  const tab = ref('tab-1')
  const tabs= ref ([
        {
          icon: 'mdi-home',
          text: 'Readme',
          value: 'tab-1',
        },
        {
          icon: 'mdi-card',
          text: 'Code of Conduct',
          value: 'tab-2',
        },
        {
          icon: 'mdi-license',
          text: 'MIT License',
          value: 'tab-3',
        },
        {
          icon: 'mdi-shield-lock-outline',
          text: 'Security',
          value: 'tab-4',
        },
      ])
</script>
<style scoped>
  .footer{
    position: fixed;
    width: 100%;
    height: 10vh;
    bottom: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: brown;
  }
</style>
