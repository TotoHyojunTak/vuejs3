<template>
    <div>
      <input type="text" name="" id="" v-bind:value="userId" readonly /> <br/>
      <input type="text" name="" id="" :value="userId" readonly /> <br />
      <img :src="imgSrc" alt="" style="width:10px; height: auto;" />
      <input type="search" name="" id="" v-model="txt1" />
      <button :disabled="txt1 === ''">조회</button>
    </div>
</template>

<script>
export default {
  components: {},
  data () {
    return {
      userId: '으이그',
      imgSrc: '',
      txt1: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
  }
}
</script>

<style>

</style>
