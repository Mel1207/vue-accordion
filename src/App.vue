<template>
  <div class="container">
    <div class="section-row">
      <div class="left-col">
        <div :class="cardImage.imgClass" v-for="cardImage in cardImages" :key="cardImage.id">
          
        </div>
      </div>
      <div class="right-col">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. At fugiat perferendis repellendus dolores inventore minus vitae maiores deserunt officia deleniti distinctio nesciunt harum nostrum adipisci laborum magnam eligendi mollitia aliquid, pariatur necessitatibus ex impedit! Iure dolore at fugiat voluptates aliquid, ipsam quod ratione, et reiciendis praesentium quos accusantium cum beatae.
      </div>
    </div>  
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {},
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

    console.log(cardImages.imgSrc)
    return {
      cardImages
    }
  }
}
</script>