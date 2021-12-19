<template>
  <div class="home">
    <div v-for="book in books" :key="book.id">
      <div class="book">
        <h3>{{ book.title }}</h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur aspernatur consectetur doloremque sunt ducimus enim iure animi fugit nulla et! Perferendis autem deleniti quo eum corrupti reiciendis voluptatem ab ducimus?</p>
        <div class="icons">
          <span>upvote or downvote this book: </span>
          <span class="material-icons">thumb_up</span>
          <span class="material-icons">thumb_down</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const books = ref([
      { title: 'Magic Tree House', id: 1 },
      { title: 'Harry Potter-The Chamber of Secrets', id: 2 },
      { title: 'California 1542-1850', id: 3 },
    ])

    return { 
      books
    }
  }
}
</script>
