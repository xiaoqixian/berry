<template>
  <a class="post" :href="path">
    <article>
      <div class="category">{{ category }}</div>
      <div class="thumbnail" v-if="thumbnail != null">
        <img loading="lazy" alt="Image Not Found" :src="thumbnail"/>
      </div>

      <div class="content" :style="content_style">
        <div class="title">
          <h2>{{ title }}</h2>
        </div>
        <div class="date">{{ date }}</div>
        <div class="tags">
          <div class="tag"
            v-for="(tag, index) in tags"
            v-show="index < 7">
            {{ tag }}
          </div>
        </div>
      </div>
    </article>
  </a>
</template>

<script>
const content_without_thumb = "padding: 1rem; padding-top: 3.5rem;"
const content_with_thumb = "padding: 1rem;"

export default {
  name: "Post",
  props: {
    path: String,
    category: String,
    thumbnail: String,
    title: String,
    date: String,
    tags: Array
  },
  setup: function(props) {
    return {
      content_style: props.thumbnail == null ? content_without_thumb : content_with_thumb
    }
  }
}
</script>

<style scoped>
.post article {
  overflow: hidden;
  position: relative;
  margin-bottom: 1.5rem;
  border-radius: 1rem;
  background-color: white;
  transition-property: box-shadow;
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
  transition-duration: 300ms;
  color: black;
}

.post article:hover {
  box-shadow: rgba(0, 0, 0, 0.1) 0px 10px 15px -3px, rgba(0, 0, 0, 0.05) 0px 4px 6px -2px;
}

.post .category {
  position: absolute;
  top: 1rem;
  left: 1rem;
  z-index: 10;
}

.post .thumbnail {
  position: relative;
  width: 100%;
  background-color: rgb(248, 248, 248);
  padding-bottom: 50%;
}

.post .thumbnail img {
  object-fit: cover;
  position: absolute;
  height: 100%;
  width: 100%;
  left: 0;
  top: 0;
  right: 0;
  bottom: 0;
  color: transparent;
}

.post .content .title {
  display: flex;
  justify-content: space-between;
}

.post .content .date {
  display: flex;
  margin-bottom: 1rem;
  gap: 0.5rem;
  align-items: center;
}

.post .content .tags {
  display: flex;
  gap: 0.5rem;
}
.post .content .tags .tag {
  padding: 0.25rem 0.5rem;
  border-radius: 50px;
  font-size: 0.75rem;
  line-height: 1rem;
  font-weight: 400;
  color: rgb(133, 133, 133);
  background-color: rgb(232, 232, 232);
  cursor: pointer;
}

</style>
