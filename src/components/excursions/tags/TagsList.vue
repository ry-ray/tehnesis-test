<template>
  <div class="excursion__tags-box">
    <span v-for="tag in tags" :key="tag.id" class="excursion__tag-box">
      <v-icon v-if="tag.icon !== 'mdi-star'" class="excursion__tag circle"
        >mdi-circle-medium</v-icon
      >
      <v-icon v-if="tag.icon" class="excursion__tag icon">{{
        tag.icon
      }}</v-icon>
      <span class="excursion__tag tag">{{ tag.value }}</span>
    </span>
  </div>
</template>

<script>
export default {
  props: {
    tags: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss" scoped>
.excursion__tags-box {
  max-height: 2em;
  overflow-y: hidden;
}
.excursion__tag-box {
  display: inline-block;
}

.excursion__tag {
  padding-right: 5px;
}
.icon {
  padding-bottom: 0.25em;
}
</style>
