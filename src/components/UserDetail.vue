<template>
  <div class="red lighten-3 pa-3">
    <h3>자세한 회원 정보를 확인합니다.</h3>
    <p>{{ nameOfChild }}</p>
    <p>{{ sayHello }}</p>
  </div>
</template>

<script>
export default {
    props: {
        // 부모로부터 받기때문에 값을 넣는게 아닌 타입 선언
        nameOfChild: {
            type: String,
            // required: true,
            default: 'aaa'
        }
    },
    computed: {
        sayHello() {
            return this.nameOfChild + ' Hi~~!!'
        }
    },
}
</script>