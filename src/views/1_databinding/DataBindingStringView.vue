<template>
    <div>
        <h1> {{ userName }}님 환영합니다</h1>
        <p>{{ message }}</p>
    </div>
</template>

<script>
export default {
  data () {
    return {
      userName: 'Toto',
      message: 'Hello world!',
      arr: [],
      obj: {}
    }
  }
}
</script>>
<style scoped>
/* scoped를 선언하게 되면 이 파일에만 스타일을 적용한다 */
.text-red{
    color: red
}
</style>
