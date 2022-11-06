<template>
<div>
  <b-card :title="user.name" :sub-title="user.username">
    <b-card-text>
      {{user.name}}
    </b-card-text>

    <b-card-text>Address: {{user.address}}</b-card-text>

    <a href="#" class="card-link">{{user.email}}</a>
    <b-link href="#" class="card-link">{{user.username}}</b-link>
  </b-card>
</div>
</template>
<script>
export default {
  name: 'CardView',
  props: {
    user: Object
  }

}
</script>
