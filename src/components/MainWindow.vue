<template>
  <main>
    <div id="main-grid">
      <div id="tags">
        <div id="tags-top">Tags</div>
        <div id="tag-list">
          <a v-for="tag in tags">{{tag}}</a>
        </div>
      </div>
      <mid />
    </div>
  </main>
</template>

<script>
  import Mid from './Mid.vue'
  const tags = ["rust", "cpp", "python", "分布式"]

  export default {
    setup: function() {
      return {
        tags
      }
    },
    components: {
      Mid
    }
  }
</script>

<style scoped>
main {
  margin: 0 auto;
  width: 100%;
  max-width: 1120px;
  padding: 0 1rem;
  display: block;
}

#main-grid {
  grid-template-columns: repeat(12, minmax(0, 1fr));
  padding: 0;
  display: grid;
  gap: 1.5rem;
}

#tags {
  overflow: scroll;
  position: sticky;
  grid-column: span 2 / span 2;
  scrollbar-width: none;
}

#tags-top {
  padding: 0.25rem;
  margin-bottom: 0.75rem;
  font-weight: 400;
  font-size: 1.5rem;
  font-weight: bold;
}

#tag-list {
  overflow: scroll;
  scrollbar-width: none;
}
#tag-list a {
  display: block;
  padding: 0.25rem 1rem;
  margin-top: 0.25rem;
  margin-bottom: 0.25rem;
  border-radius: 0.75rem;
  font-size: 0.875rem;
  line-height: 1.25rem;
  color: rgb(133, 133, 133);
  flex-shrink: 0;
  cursor: pointer;
}
</style>
