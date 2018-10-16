<template>
  <div>
    
    <h1>This is the index.vue inside of /users/_id folder.</h1>
    <h2> single user with ID {{ $route.params.id }}</h2>
    </div>


</template>

<script>
export default {
  validate(data) {
    // console.log(data)
    // return true

    // if(data.params.id > 0 && data.params.id < 10) {
    //   return data.params.id
    // } else {
    //   return false
    // }

    // or regex test:
    return /^\d+$/.test(data.params.id)
  },
    data() {
    return {
    }
  }

}
</script>
