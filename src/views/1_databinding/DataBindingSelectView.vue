<template>
    <div>
        <select name="" id="" v-model="selectedCity">
          <option value=""></option>
          <option value="02">서울</option>
          <option value="031">경기</option>
          <option value="051">부산</option>
          <option value="055">경남</option>
        </select>
    </div>
</template>

<script>
export default {
  components: {},
  data () {
    return {
      selectedCity: '02'
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    myFunction() {
      console.log(this.userId)
    },
    changeData() {
      this.userId = '으이그'
    }
  }
}
</script>

<style>

</style>
