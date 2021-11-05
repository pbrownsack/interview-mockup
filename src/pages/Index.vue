<template>
  <Layout>

    <Hero />
    <CardSection />
    <ImageSlider />

  </Layout>
</template>

<script>
import Hero from '~/components/Hero.vue';
import CardSection from '~/components/CardSection.vue';
import ImageSlider from '~/components/ImageSlider.vue';

export default {
  metaInfo: {
    title: 'Hello, world!'
  },
  components: {
    Hero,
    CardSection,
    ImageSlider
  }
}
</script>
