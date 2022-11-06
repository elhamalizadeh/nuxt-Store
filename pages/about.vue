<template>
  <NuxtLayout>
    <Menu />
    <h1>About page</h1>
    some page content
  </NuxtLayout>
</template>

<script>
export default {
  head: {
    title: 'about-us',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'we are a bookstore that sell best books'
      }
    ]
  }

}
</script>
