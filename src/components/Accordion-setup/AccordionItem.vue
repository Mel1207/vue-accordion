<template>
  <div class="acc-wrapper" v-for="item in accItems" :key="item.id">
    <div class="acc-title" @click="toggleAcc(item)">
      <p>{{ item.accTitle }}</p>

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
        accTitle: 'How to apply for sponsorship?',
        accContent: 'Many desktop publishing packages and web page editors now use Lorem Ipsum as their default model text, and a search for lorem ipsum will uncover many web sites still in their infancy.',
        isOpen: true
      },
      {
        id: 1,
        accTitle: 'What are events requirements?',
        accContent: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, galley of type and scrambled it to make a type specimen book.',
        isOpen: false
      },
      {
        id: 1,
        accTitle: 'What are the payment modes accepted?',
        accContent: 'lorem ipsum dolor sit amet Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the  ever since the 1500s book.',
        isOpen: false
      },
      {
        id: 1,
        accTitle: 'What are perks of joining the program?',
        accContent: 'It is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the dummy text ever since the 1500s, when an unknown printer took a galley.',
        isOpen: false
      },
      {
        id: 1,
        accTitle: 'Can I get a reference discount for invites?',
        accContent: 'lorem ipsum dolor sit amet text of the printing and typesetting industry. Lorem Ipsum has been the dummy.',
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