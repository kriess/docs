<template lang="pug">
  doc-view(v-bind:doc="doc" id="icons")
    component-example(header="Standard (small)" file="icons/1")
    component-example(header="Medium" file="icons/2")
    component-example(header="Large" file="icons/3")
    component-example(header="X-Large" file="icons/4")
    component-example(header="Color" file="icons/5")
    component-example(header="Buttons" file="icons/6")
</template>

<script>
  export default {
    data () {
      return {
        doc: {
          title: 'Icons',
          desc: 'The <code>v-icon</code> component provides a large set of glyphs to provide context to various aspects of your application. Vuetify icons utilize Google\'s Material Icons font library. For a list of all available icons, visit the official <a href="https://material.io/icons/" target="_blank">Material Icons</a> page.',
          props: {
            'v-icon': {
              params: [
                [
                  'medium',
                  'Boolean',
                  'False',
                  'Medium size'
                ],
                [
                  'large',
                  'Boolean',
                  'False',
                  'Large size'
                ],
                [
                  'x-large',
                  'Boolean',
                  'False',
                  'Extra-Large size'
                ],
                [
                  'left',
                  'Boolean',
                  'False',
                  'Places icon on the left'
                ],
                [
                  'right',
                  'Boolean',
                  'False',
                  'Places icon on the right'
                ]
              ]
            }
          }
        }
      }
    },

    mounted () {
      this.$emit('view', this.meta())
    },

    preFetch () {
      return this.methods.meta()
    },

    methods: {
      meta () {
        return {
          title: 'Icon Component | Vuetify.js',
          h1: 'Icons',
          description: 'Icon component for Vuetify Framework',
          keywords: 'vuetify, icons, material design icons'
        }
      }
    }
  }
</script>

<style lang="stylus">
  #icons
    .component-example__container
      > div
        text-align: center

      > div > .icon
        margin: 1rem

      .btn
        margin: 1rem
</style>
