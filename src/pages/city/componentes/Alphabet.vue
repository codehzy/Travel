<template>
  <ul class="list">
    <li class="item"
        v-for="item of letters"
        :key="item"
        :ref="item"
        @touchstart = "handleTouchStart"
        @touchmove = "handleTouchMove"
        @touchend= "handleTouchEnd"
        @click="handleLetterClick"

      >
      {{item}}</li>
  </ul>
</template>

<script>
export default {
  name: 'CityAlphabet',
  props: {
    cities: Object
  },
  computed: {
    letters () {
      const letters = []
      for (let i in this.cities) {
        letters.push(i)
      }
      return letters
    }
  },
  data () {
    return {
      touchStatus: false
    }
  },
  methods: {
    handleLetterClick (e) {
      this.$emit('change', e.target.innerText)
    },
    handleTouchStart () {
      this.touchStatus = true
    },
    handleTouchMove (e) {
      if (this.touchStatus) {
        const touchY = e.touches[0].clientY - 74
        const index = Math.floor((touchY - 74) / 20)
        if (index >= 0 && index < this.letters.length) {
          this.$emit('change', this.letters[index])
        }
      }
    },
    handleTouchEnd () {
      this.touchStatus = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  .list
    display :flex
    flex-direction :column
    justify-content :center
    position :absolute
    top:3rem
    right :0
    buttm:0
    width:.4rem
    .item
      line-height :.4rem
      text-align :center
      color:$bgColor

</style>
