<template>
  <v-container>
    <div
      v-for="excursion in excursions"
      :key="excursion.id"
      class="excursions__items"
    >
      <div class="excursion__item">
        <h4>{{ excursion.title }}</h4>
      </div>
      <tags-list :tags="excursion.tags" />
    </div>
  </v-container>
</template>

<script>
import TagsList from "./tags/TagsList.vue";

export default {
  components: {
    TagsList,
  },
  props: {
    excursions: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss" scoped>
.excursions__items {
  margin-left: auto;
  margin-right: auto;

  min-height: 60px;
  padding: 10px;
  margin-bottom: 15px;

  text-align: center;

  border: 5px solid rgba(98, 0, 234, 0.5);
  border-radius: 10px;
}

.excursion__item {
  font-size: 1.5em;
}
</style>
