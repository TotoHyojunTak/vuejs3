<template>
    <div>
        <div>{{ htmlString }}</div>
        <div v-html="htmlString"></div>
    </div>
</template>

<script>
export default {
  components: {},
  data () {
    return {
      htmlString: '<p style="color:red;">Red Characters</p>'
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>

<style>

</style>
