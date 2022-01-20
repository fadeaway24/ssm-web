<template>
  <div class="vue0014">
    <div v-for="item in productData" :key="item.id">
      <component :is="`My${item.type}`"></component>
    </div>
  </div>
</template>

<script>
import Text from './model/Text';
import Image from './model/Image';
import Video from './model/Video';

export default {
  data() {
    return {
      productData: [
        {
          id: 1,
          type: 'Video',
        },
        {
          id: 2,
          type: 'Text',
        },
        {
          id: 3,
          type: 'Image',
        },
        {
          id: 4,
          type: 'Text',
        },
      ],
    };
  },
  components: {
    MyText: Text,
    MyImage: Image,
    MyVideo: Video,
  },
};
</script>

<style></style>
