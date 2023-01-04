<template>
    <div>
      <div>
        <select name="" id="">
          <option value=""></option>
          <option :value="city.code" :key="city.code" v-for="city in cities">
            {{ city.title }}
          </option>
        </select>
      </div>
      <div>
        <table>
          <thead>
            <tr>
              <th>제품번호</th>
              <th>제품명</th>
              <th>수량</th>
              <th>단가</th>
              <th>합계</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="drink in drinkList" :key="drink.drinkId">
              <td>{{ drink.drinkId }}</td>
              <td>{{ drink.drinkName }}</td>
              <td><input type="number" name="" id="" v-model="drink.qty"/></td>
              <td>{{ drink.price }}</td>
              <td>{{ drink.price * drink.qty }}</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
</template>

<script>
export default {
  components: {},
  data () {
    return {
      cities: [
        { title: '서울', code: '02' },
        { title: '경기', code: '031' },
        { title: '대구', code: '051' }
      ],
      drinkList: [
        {
          drinkId: '1',
          drinkName: 'Coke',
          price: 700,
          qty: 1
        }, {
          drinkId: '2',
          drinkName: 'Sprite',
          price: 800,
          qty: 2
        }
      ]
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
