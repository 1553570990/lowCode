<style lang="scss" scoped>
.container {
  display: flex;
  &__left {
    width: 300px;
    height: 1500px;
    &__drag {
      &__item {
        margin-bottom: 10px;
        width: 50px;
        height: 50px;
        border: 1px solid black;
      }
    }
  }
  &__right {
    width: 1000px;
    height: 1500px;
    background-color: red;
    margin-left: 20px;
  }
}
</style>
<template>
  <div>
    <div class="container">
      <div class="container__left">
        <draggable class="container__left__drag">
          <div class="container__left__drag__item" v-for="(list1Item, index) in list1" :key="index">
            {{ list1Item.name }}
          </div>
        </draggable>
      </div>
      <div class="container__right"></div>
    </div>
  </div>
</template>

<script>
import draggable from 'vuedraggable'
export default {
  data() {
    return {
      list1: [
        { name: 'a', age: '' },
        { name: 'b', age: '' },
        { name: 'c', age: '' },
        { name: 'd', age: '' },
        { name: 'e', age: '' },
        { name: 'f', age: '' },
        { name: 'g', age: '' },
        { name: 'h', age: '' },
        { name: 'i', age: '' },
        { name: 'j', age: '' },
        { name: 'k', age: '' },
        { name: 'l', age: '' },
        { name: 'm', age: '' }
      ]
    }
  },
  components: {
    draggable
  }
}
</script>
