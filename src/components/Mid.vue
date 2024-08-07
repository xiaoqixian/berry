<template>
  <div id="mid">
    <div class="search">
      <input type="text" placeholder="search" value=""/>
    </div>
    <post-filter/>
    <div id="posts">
      <post v-for="post in posts" v-bind="post"/>
    </div>
  </div>
</template>

<style scoped>
#mid {
  margin-bottom: 2rem;
  grid-column: span 7 / span 7;
}

#mid .search {
  padding: 0.5rem 1.25rem;
  border-radius: 1rem;
  outline-style: none;
  width: 100%;
  background-color: rgb(237, 237, 237);
  margin-bottom: 1rem;
}
input {
  all: unset;
  box-sizing: border-box;
}
</style>

<script>
import PostFilter from './PostFilter.vue'
import Post from './Post.vue'

const posts = [
  {
    path: "/frontend",
    category: "Frontend",
    thumbnail: "src/assets/images/cover.jpeg",
    title: "Welcome to the berry blog",
    date: "Aug 4, 2024",
    tags: ["Frontend", "Vue"]
  },
  {
    path: "/rust",
    category: "Rust",
    thumbnail: null,
    title: "Rust HTTP framework design",
    date: "Aug 4, 2024",
    tags: ["Rust", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network"]
  },
  {
    path: "/rust",
    category: "Rust",
    thumbnail: null,
    title: "Rust HTTP framework design",
    date: "Aug 4, 2024",
    tags: ["Rust", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network"]
  },
  {
    path: "/rust",
    category: "Rust",
    thumbnail: null,
    title: "Rust HTTP framework design",
    date: "Aug 4, 2024",
    tags: ["Rust", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network"]
  },
  {
    path: "/rust",
    category: "Rust",
    thumbnail: null,
    title: "Rust HTTP framework design",
    date: "Aug 4, 2024",
    tags: ["Rust", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network"]
  },
  {
    path: "/rust",
    category: "Rust",
    thumbnail: null,
    title: "Rust HTTP framework design",
    date: "Aug 4, 2024",
    tags: ["Rust", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network"]
  },
  {
    path: "/rust",
    category: "Rust",
    thumbnail: null,
    title: "Rust HTTP framework design",
    date: "Aug 4, 2024",
    tags: ["Rust", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network", "Network"]
  },
]

export default {
  name: "Mid",
  components: {
    PostFilter,
    Post
  },
  setup: function() {
    return {
      posts
    }
  }
}
</script>
