<template>
  <div class="container">
    <div class="section-row">
      <div class="left-col">
        <CardImages />
      </div>
      <div class="right-col">
        <SectionDescription />
        <AccordionSet />
      </div>
    </div>  
  </div>
</template>

<script>
import CardImages from './components/CardImages.vue'
import SectionDescription from './components/SectionDescription.vue'
import AccordionSet from './components/AccordionSet.vue'

export default {
  name: 'App',
  components: { CardImages, SectionDescription, AccordionSet }
}
</script>