<template>
  <div class="issue-item">
    <span>{{ item.id }}</span>
    <span>{{ item.name }}</span>
    <span>{{ item.price }}</span>
  </div>
</template>

<script>
export default {
  name: 'IssueItem',
  props: {
    item: Object
  }
}
</script>

<style scoped lang="scss">
  .issue-item {
    border: 1px solid lightgray;
    padding: 8px;
    span {
      padding-right: 15px;
    }
  }
</style>
