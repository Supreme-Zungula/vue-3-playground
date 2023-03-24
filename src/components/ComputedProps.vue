<template>
  <div>
    <p>Has published books:</p>
  <span>{{ publishedBookMessage }}</span>

  </div>
</template>
<script>
import { reactive, computed } from 'vue'
export default {
  setup(props) {
    const author = reactive({
      name: 'John Doe',
      books: [
        'Vue 2 - Advanced Guide',
        'Vue 3 - Basic Guide',
        'Vue 4 - The Mystery'
      ]
    })

    const publishedBookMessage = computed(() => {
      return author.books.length > 0 ? 'Yes' : 'No'
    })

    
    return {
      author,
      publishedBookMessage
    }
  }
}
</script>
<style lang="">
  
</style>