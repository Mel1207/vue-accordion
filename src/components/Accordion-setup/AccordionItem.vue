<template>
  <div class="acc-wrapper" v-for="item in accItems" :key="item.id">
    <div class="acc-title">
      <p>What is company vission ?</p>
      <img src="../../assets/icon-acc-open.svg" alt="icon open">
    </div>
    <div class="acc-content" v-if="item.isOpen">
      {{ item.accContent }}
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  setup() {
    const accItems = ref([
      {
        id: 1,
        accTitle: 'Title 1',
        accContent: 'lorem ipsum dolor sit amet',
        isOpen: true
      },
      {
        id: 1,
        accTitle: 'Title 1',
        accContent: 'lorem ipsum dolor sit amet',
        isOpen: false
      },
      {
        id: 1,
        accTitle: 'Title 1',
        accContent: 'lorem ipsum dolor sit amet',
        isOpen: false
      },
      {
        id: 1,
        accTitle: 'Title 1',
        accContent: 'lorem ipsum dolor sit amet',
        isOpen: false
      },
      {
        id: 1,
        accTitle: 'Title 1',
        accContent: 'lorem ipsum dolor sit amet',
        isOpen: false
      },
    ])


    return {
      accItems
    }
  }
}
</script>