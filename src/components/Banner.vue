<template>
  <div id="container">
    <div id="banner">
      <div id="title-tag">
        Berry-Blog
      </div>
      <div id="nav">
        <div id="theme">
          <span id="sun">☀️ </span>
        </div>
        <div id="about">
          <a href="/about">About</a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
#container {
  padding: 0px;
  box-shadow: rgba(0, 0, 0, 0.05) 0px 1px 2px 0px;
  width: 100%;
  margin-bottom: 32px;
}

#banner {
  flex: none;
  display: flex;
  padding-left: 1rem;
  padding-right: 1rem;
  justify-content: space-between;
  align-items: center;
  max-width: 1120px;
  height: 3rem;
  width: 100%;
  margin: 0px auto;
}

#title-tag {
  width: 10%;
  flex: none;
}

#nav {
  display: flex;
  gap: 0.75rem;
  align-items: center;
}
#theme {
  cursor: pointer;
  display: block;
}
#sun {
  font-weight: 400;
  font-style: normal;
}

#about {
  flex-shrink: 0;
  display: block;
  padding-left: 1rem;
}
#about a {
  color: rgb(0, 0, 0);
}
#about a:hover {
  background: transparent;
}

</style>
