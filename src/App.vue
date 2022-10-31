<template>
  <v-app>
    <HeaderVue />
    <excursions-list :excursions="excursions" />
  </v-app>
</template>

<script>
import HeaderVue from "./components/Header.vue";
import ExcursionsList from "./components/excursions/ExcursionsList.vue";

export default {
  name: "App",
  components: {
    HeaderVue,
    ExcursionsList,
  },
  data: () => {
    return {
      excursions: [
        {
          id: 1,
          title: "«Город сыра и мира»",
          tags: {
            rating: { id: 1, icon: "mdi-star", value: 5 },
            description: { id: 2, value: "Историческая" },
            transport: { id: 3, icon: "mdi-bus", value: "На автобусе" },
            date: { id: 4, value: "28 марта" },
            duration: {id: 5, icon: "mdi-clock-time-three-outline", value: "9 часов",},
            num: { id: 6, icon: "mdi-account", value: "до 49 человек" },
            place: { id: 7, icon: "mdi-map-marker", value: "Калининград" },
          },
        },
        {
          id: 2,
          title: "Экскурсия в национальный парк «Куршская коса»",
          tags: {
            rating: { id: 1, icon: "mdi-star", value: 5 },
            description: { id: 2, value: "Обзорная" },
            transport: { id: 3, icon: "mdi-bus", value: "На автобусе" },
            date: { id: 4, value: "25 марта" },
            duration: { id: 5, icon: "mdi-clock-time-three-outline", value: "6 часов", },
            num: { id: 6, icon: "mdi-account", value: "до 40 человек" },
            place: { id: 7, icon: "mdi-map-marker", value: "Куршская коса" },
          },
        },
        {
          id: 3,
          title: "«О кирках, рыцарях и замках»",
          tags: {
            rating: { id: 1, icon: "mdi-star", value: 5 },
            description: { id: 2, value: "Историческая" },
            transport: { id: 3, icon: "mdi-bus", value: "На автобусе" },
            date: { id: 4, value: "29 марта" },
            duration: { id: 5, icon: "mdi-clock-time-three-outline", value: "6 часов", },
            num: { id: 6, icon: "mdi-account", value: "до 53 человек" },
            place: { id: 7, icon: "mdi-map-marker", value: "Зеленоградск" },
          },
        },

        {
          id: 4,
          title: "Экскурсия в Янтарный",
          tags: {
            rating: { id: 1, icon: "mdi-star", value: 5 },
            description: { id: 2, value: "Историческая" },
            transport: { id: 3, icon: "mdi-bus", value: "На автобусе" },
            date: { id: 4, value: "29 марта" },
            duration: { id: 5, icon: "mdi-clock-time-three-outline", value: "6 часов"},
            num: { id: 6, icon: "mdi-account", value: "до 80 человек" },
            place: { id: 7, icon: "mdi-map-marker", value: "Янтарный" },
          },
        },
      ],
    };
  },
};
</script>
