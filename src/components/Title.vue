<template>
    <h2>
        {{title}}
    </h2>
</template>

<script>
export default {
  name: "Title",
  props: {
    title: String
  }
}
</script>

<style scoped>
h2 {
    text-decoration: underline;
    font-size: 50px;
    font-family: Raleway-Bold;
    margin-bottom: 50px;
    padding-top: 100px;
}
</style>