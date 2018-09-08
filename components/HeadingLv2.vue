<template>
  <h2 class="heading-lv2">{{ text }}</h2>
</template>

<script>
export default {
  name: 'HeadingLv1',
  props: {
    text: {
      type: String,
      default: 'Heading'
    }
  }
}
</script>

<style lang="scss" scoped>
.heading-lv2 {
  color: inherit;
  font-size: 20px;
}
</style>
