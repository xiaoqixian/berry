<template>
  <div id="filter">
    <div id="all-posts">
      <div class="wrapper">
        📂 All Posts 
        <svg stroke="black" fill="black" stroke-width="0" viewBox="0 0 24 24" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg"><path fill="none" d="M0 0h24v24H0z"></path><path d="M16.59 8.59L12 13.17 7.41 8.59 6 10l6 6 6-6z"></path></svg>
      </div>
    </div>
    <div class="sort">
      <a data-active="true">Desc</a>
      <a data-active="false">Aesc</a>
    </div>
  </div>
</template>

<style scoped>
#filter {
  background-color: rgb(248, 248, 248);
  display: flex;
  margin-bottom: 1rem;
  justify-content: space-between;
  align-items: center;
  border-bottom: 1px solid rgb(226, 226, 226);
  top: 140px;
  position: sticky;
}

#all-posts {
  position: relative;
}
#all-posts .wrapper {
  display: flex;
  margin-top: 0.5rem;
  margin-bottom: 0.5rem;
  gap: 0.25rem;
  align-items: center;
  font-size: 1.25rem;
  line-height: 1.75rem;
  font-weight: 700;
  cursor: pointer;
}

#filter .sort {
  display: flex;
  gap: 0.5rem;
  font-size: 0.875rem;
  line-height: 1.25rem;
}

#filter .sort a {
  cursor: pointer;
  color: rgb(0, 0, 0);
}
</style>
