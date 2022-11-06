<template>
  <div>
    <Menu />
    <div class="container gy-5">
     <div class="col-6 gy-5" v-for="user in users" :key="user.id">
 <usercardview :user="user" />
    </div>

    </div>
    </div>
</template>

<script>
import axios from 'axios'
import { ref } from 'vue'
import usercardview from '@/components/cardview.vue'
export default {
  components: {
    usercardview
  },
  setup () {
    const users = ref([])
    function getusers () {
      axios.get('https://jsonplaceholder.typicode.com/users').then(function (response) {
        users.value = (response.data)
      }).catch(function (error) {
        console.log(error)
      })
    }
    getusers()
    return { users }
  }
}
</script>
