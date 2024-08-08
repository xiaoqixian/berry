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
      <div id="profile">
        <div class="content">
          <div class="avatar">
            <img alt="" loading="lazy" decoding="async" data-nimg="fill" style="position:absolute;height:100%;width:100%;left:0;top:0;right:0;bottom:0;color:transparent" src="../assets/images/avatar.png">
          </div>
          <div class="words">
            <div class="name">Kalei</div>
            <div class="role">Full-Heap Developer</div>
            <div class="motto">I love Rust</div>
          </div>
        </div>
        <div class="contact">
          <span class="emoji">💬</span>
           Contact
        </div>
        <div class="links">
          <a v-for="link in links" :href="link.link">
            <img alt="" :src="link.icon"/>
            <div class="name">{{ link.name }}</div>
          </a>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
  import Mid from './Mid.vue'
  const tags = ["rust", "cpp", "python", "分布式"]
  const links = [
    {
      icon: "src/assets/images/github.svg",
      name: "Github",
      link: "https://github.com/xiaoqixian"
    },
    {
      icon: "src/assets/images/email.svg",
      name: "Email",
      link: ""
    }
  ]

  export default {
    setup: function() {
      return {
        tags,
        links
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
  top: 78px;
  grid-column: span 2 / span 2;
  scrollbar-width: none;
  height: calc(100vh - 78px);
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

#profile {
  display: block;
  grid-column: span 3 / span 3;
  position: sticky;
  top: 78px;
  scrollbar-width: none;
  height: calc(100vh - 78px);
}
#profile .content {
  padding: 1rem;
  margin-bottom: 2.25rem;
  border-radius: 1rem;
  width: 100%;
  background-color: white;
}
#profile .content .avatar {
  position: relative;
  width: 100%;
}
#profile .content .avatar::after {
  content: "";
  display: block;
  padding-bottom: 100%;
}
#profile .content .avatar img {
  position: absolute;
  height: 100%;
  width: 100%;
  left: 0;
  top: 0;
  right: 0;
  bottom: 0;
  color: transparent;
  overflow-clip-margin: content-box;
  overflow: clip;
}
#profile .words {
  display: flex;
  padding: 0.5rem;
  flex-direction: column;
  align-items: center;
}
#profile .words .name {
  font-size: 1.25rem;
  line-height: 1.75rem;
  font-weight: 700;
}
#profile .words .role {
  margin-bottom: 1rem;
  font-size: 0.875rem;
  line-height: 1.25rem;
  color: rgb(111, 111, 111);
}

#profile .contact {
  padding: 0.25rem;
  margin-bottom: 0.75rem;
}

#profile .links {
  display: flex;
  padding: 0.25rem;
  flex-direction: column;
  border-radius: 1rem;
  background-color: white;
}

#profile .links a {
  display: flex;
  padding: 0.75rem;
  gap: 0.75rem;
  align-items: center;
  border-radius: 1rem;
  color: rgb(111, 111, 111);
  cursor: pointer;
}

#profile .links a img {
  height: 24px;
}

#profile .links a .name {
  font-size: 0.875rem;
  line-height: 1.25rem;
}

</style>
