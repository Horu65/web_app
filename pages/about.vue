<template>
    <h1>About Page</h1>
    <h2>{{ subtitle }}</h2>
</template>

<script>

export default ({
  head() {
    return {
        title: 'About Page',
        meta:[
            { hid: 'description', name: 'description', content: 'これはAboutページです'}
        ]
    }
  },
  data() {
    return {
        id: this.$route.params.id,
        users: [
            {
                id: 1,
                name:'john Doe'
            }
        ]
    }
  },
  computed:{
      user(){
          return this.users.find(user => user.id ==this.id)
      }
  }
})
</script>
