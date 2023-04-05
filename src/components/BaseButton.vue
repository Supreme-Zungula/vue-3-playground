<template>
  <button>Click</button>
</template>
<script>
export default {
  setup(props, context) {
    console.log(context.attrs);
  },
}
</script>