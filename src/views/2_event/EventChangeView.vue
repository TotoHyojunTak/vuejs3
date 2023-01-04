<template>
    <div>
        <select name="" id="" @change="changeCity" v-model="selectedCity">
            <option value="">==도시선택==</option>
            <option value="city.code" :key="city.code" v-for="city in cityList">{{ city.title }}</option>
        </select>
        <select name="" id="">
            <option :value="dong.dongCode" :key="dong.dongCode" v-for="dong in selectedDongList">
                {{ dong.dongTitle }}
            </option>
        </select>
        <select name="" id="">
            <option :value="dong.dongCode" :key="dong.dongCode" v-for="dong in dongList.filter(
                (dong) => dong.code === selectedCity
                )">
                {{ dong.dongTitle }}
            </option>
        </select>
    </div>
</template>

<script>
export default {
  components: {},
  data () {
    return {
      selectedCity: '',
      selectedDongList: [],
      cityList: [
        { code: '02', title: 'Seoul' },
        { code: '053', title: 'Daegu' },
        { code: '064', title: 'Jeju' }
      ],
      dongList: [
        { code: '02', dongCode: '1', dongTitle: 'Gangnam' },
        { code: '02', dongCode: '2', dongTitle: 'Mapo' },
        { code: '02', dongCode: '3', dongTitle: 'Yongsan' },
        { code: '053', dongCode: '1', dongTitle: 'Dongdaegu' },
        { code: '053', dongCode: '2', dongTitle: 'Seodaegu' },
        { code: '064', dongCode: '1', dongTitle: 'Jeju' },
        { code: '064', dongCode: '2', dongTitle: 'Seogwipo' }
      ]
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    changeCity(event) {
      console.log(event.target.tagName)
      this.selectedDongList = this.dongList.filter(dong => dong.code === this.selectedCity)
    }
  }
}
</script>
