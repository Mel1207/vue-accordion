<template>
  <div class="acc-wrapper" v-for="item in accItems" :key="item.id">
    <div class="acc-title" @click="toggleAcc(item)">
      <p>What is company vission ?</p>

      <div>
        <img src="../../assets/icon-acc-close.svg" alt="icon close" v-if="item.isOpen">
        <img src="../../assets/icon-acc-open.svg" alt="icon open" v-if="!item.isOpen">
      </div>
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
    const toggleAcc = (item) => {
      item.isOpen = !item.isOpen
    }

    const accItems = ref([
      {
        id: 1,
        accTitle: 'Title 1',
        accContent: 'Many desktop publishing packages and web page editors now use Lorem Ipsum as their default model text, and a search for lorem ipsum will uncover many web sites still in their infancy.',
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
      accItems,
      toggleAcc
    }
  }
}
</script>