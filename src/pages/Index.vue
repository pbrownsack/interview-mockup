<template>
  <Layout>

    <Hero />
    <CardSection />
    <ImageSlider />
    <ImageModal v-if="this.$store.modalOpen" v-bind:image="this.$store.imageSrc" />

  </Layout>
</template>

<script>
import Hero from '~/components/Hero.vue';
import CardSection from '~/components/CardSection.vue';
import ImageSlider from '~/components/ImageSlider.vue';
import ImageModal from '~/components/ImageModal.vue'

export default {
  metaInfo: {
    title: 'TeamCreate'
  },
  components: {
    Hero,
    CardSection,
    ImageSlider,
    ImageModal
  }
}
</script>
