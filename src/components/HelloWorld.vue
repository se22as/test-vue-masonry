<template>
  
  <div
    class="grid"
    v-masonry="containerId"
    transition-duration="0.3s"
    item-selector=".grid-item">
    <div
      v-masonry-tile class="grid-item"
      v-for="(image, i) in imagesArray"
      v-bind:key="i">
      <img
        :src=image
        :data-key=i
        alt="Small preview">
    </div>
  </div>
</template>

<script>
import Vue from 'vue';
import { VueMasonryPlugin } from 'vue-masonry';

Vue.use(VueMasonryPlugin);

export default {
  name: 'HelloWorld',
  data() {
    return {
      
      imagesArray: [
        'https://homepages.cae.wisc.edu/~ece533/images/airplane.png',
        'https://homepages.cae.wisc.edu/~ece533/images/arctichare.png',
        'https://homepages.cae.wisc.edu/~ece533/images/baboon.png',
        'https://homepages.cae.wisc.edu/~ece533/images/barbara.png',
        'https://homepages.cae.wisc.edu/~ece533/images/boat.png',
        'https://homepages.cae.wisc.edu/~ece533/images/cat.png',
        'https://homepages.cae.wisc.edu/~ece533/images/fruits.png',
        'https://homepages.cae.wisc.edu/~ece533/images/frymire.png',
        'https://homepages.cae.wisc.edu/~ece533/images/girl.png',
        'https://homepages.cae.wisc.edu/~ece533/images/goldhill.png',
        'https://homepages.cae.wisc.edu/~ece533/images/lena.png',
        'https://homepages.cae.wisc.edu/~ece533/images/monarch.png',
        'https://homepages.cae.wisc.edu/~ece533/images/peppers.png',
        'https://homepages.cae.wisc.edu/~ece533/images/pool.png',
        'https://homepages.cae.wisc.edu/~ece533/images/sails.png',
        'https://homepages.cae.wisc.edu/~ece533/images/serrano.png',
        'https://homepages.cae.wisc.edu/~ece533/images/tulips.png',
        'https://homepages.cae.wisc.edu/~ece533/images/watch.png',
        'https://homepages.cae.wisc.edu/~ece533/images/zelda.png'
      ],
      containerId: 0,
    };
  },
  
}
</script>


