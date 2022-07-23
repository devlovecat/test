<template>
  <div>
    <h1>User 컴포넌트</h1>
    <p>이름 : {{ name }}</p>
    <button @click="changeName()">이름 변경</button>
    <hr>
    <UserDetail :nameOfChild="name"></UserDetail>
    <UserEdit></UserEdit>
  </div>
</template>

<script>
import UserDetail from './UserDetail'
import UserEdit from './UserEdit'
import { ref } from 'vue'

export default {
  components: {
    UserDetail,
    UserEdit
  },
  setup() {
    const name =  ref('뷰제이에스'),
    changeName = () => {
        name.value = 'cho'
    }
    return {
    name,
    changeName
  }
  },
  
}
</script>