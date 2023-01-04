<template>
    <div>
        <!-- <input type="search" name="" id="" v-model="searchText" @keyup="checkEnter($event)" /> -->
        <input type="search" name="" id="" v-model="searchText" @keyup.enter="doSearch" />
        <button @click="doSearch">조회</button>
        <button type="submit" @click.prevent>조회</button>
    </div>
</template>

<script>
export default {
  components: {},
  data () {
    return {
      sampleData: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    doSearch() {
      console.log(this.searchText)
    },
    checkEnter(event) {
      if (event.keyCode === 13) {
        this.doSearch()
      }
    }
  }
}

</script>
