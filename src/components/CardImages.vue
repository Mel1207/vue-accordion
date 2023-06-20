<template>
  <div v-for="cardImage in cardImages" :key="cardImage.id" :class="cardImage.imgClass"></div>
</template>

<script>
export default {
  setup() {
    const cardImages = [
      { 
        id: 1,
        imgName: 'Exibit 1',
        imgClass: 'img1'
      },
      { 
        id: 2,
        imgName: 'Exibit 2',
        imgClass: 'img2'
      },
      { 
        id: 3,
        imgName: 'Exibit 3',
        imgClass: 'img3'
      }
    ]

    return {
      cardImages
    }
  }
}
</script>