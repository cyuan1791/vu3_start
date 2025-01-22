<script>
export default {
  props: ['title'],
  setup(props) {
    console.log(props.title)
  }
}
</script>

<template>
  <h4>{{ title }}</h4>
</template>