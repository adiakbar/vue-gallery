<template>
  <div>
    <a href="#" @click="emitImage(image)" v-for="image in images">
      <div class="col-md-3 col-sm-4 col-xs-6">
        <img :src="image.thumbnail" alt="" class="img-responsive">
      </div>
    </a>
  </div>  
</template>

<script>
export default {
  props: ['images'],
  methods: {
    emitImage: function (image) {
      this.$emit('emitImage', image)
    }
  }
}
</script>

<style>

</style>
