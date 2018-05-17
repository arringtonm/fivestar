<template>
  <div>

  <div>
    <h4>shit v-if method</h4>
    <span v-if="rating2x >= 2 && rating2x < 4">
      <i class="fa fa-star"></i>
    </span>
    <span v-if="rating2x >= 4 && rating2x < 6">
     <i class="fa fa-star"></i><i class="fa fa-star"></i>
    </span>
    <span v-if="rating2x >= 6 && rating2x < 8">
     <i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i>
    </span>
    <span v-if="rating2x >= 8 && rating2x < 10">
     <i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i>
    </span>
    <span v-if="rating2x === 10">
     <i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i>
    </span>
    <span v-if="rating2x %2 === 1">
     <i class="fa fa-star-half"></i>
    </span>
  </div>

  <hr>

  <div>
    <h4>shit array method</h4>
    <div v-html="shitArray">
    </div>
  </div>


 </div>

</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      rating: 3.5,
      shitOutput: ''
    }
  },
  computed: {
    rating2x: function () {
        return this.rating * 2
    },
    shitArray() {
      for (let i = 0; i + 0.5 < this.rating; i++) {
        this.shitOutput = this.shitOutput + '<i class="fa fa-star"></i>'
      }
      // if ((this.rating *2) %2 === 1) { this.shitOutput = this.shitOutput + '<i class="fa fa-star-half">' }
      if (this.rating %1 != 0) { this.shitOutput = this.shitOutput + '<i class="fa fa-star-half">' }

      return this.shitOutput
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

</style>
