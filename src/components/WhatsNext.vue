<template lang="pug">
  div(class="whats-next")
    h2(class="section-header primary--after")
      | What's Next
      v-icon(x-large class="primary--text") help_outline
    v-alert(info v-bind:value="true")
      v-container(fluid)
        v-row(row wrap)
          v-col(xs12 sm12 md8)
            slot
          v-col(xs12 sm12 md4 class="text-sm-right text-xs-center")
            v-btn(class="blue darken-3 white--text" v-bind:href="route" router)
              | {{ text }}
              v-icon(right) chevron_right
</template>

<script>
  export default {
    props: {
      route: String,
      text: String
    }
  }
</script>

<style lang="stylus">
  .whats-next    
    margin-top: 3rem
    p
      margin: 0
      
    h2
      display: flex
      align-items: center
    
    @media screen and (max-width: 64rem)
      .btn
        margin: 2rem 0 0
        width: 100%
</style>