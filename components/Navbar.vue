<template>
  <div>
    <nav>
      <div class="nav-wrapper">
        <a href="#" class="brand-logo"><TBLogo /></a>
        <a id="nav-mobile" href="#" class="" @click="toggleMenu()">
          <v-mdi name="mdiMenu" />
        </a>
      </div>
      <div v-if="menu" class="Menu">
        <div class="Menu-content">
          <div class="Menu-body">
            <ul>
              <li>
                <router-link to="/">ホーム</router-link>
              </li>
              <li>
                <router-link to="/about">について</router-link>
              </li>
              <li>
                <router-link to="/contact">Contact</router-link>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default{
  data(){
    return{
      menu: false
    }
  },
  methods:{
    toggleMenu(){
      this.menu = !this.menu
    }
  }
}
</script>

<style lang="scss" scoped>
nav{
  width: 100vw;
  position: fixed;
  top: 0;
  left: 0;
  background: #fff;
  box-shadow: 0 0 10px gray;
  margin: 0;
}

.nav-wrapper{
  padding-left: 20px;
  padding-right: 20px;
  padding-top: 10px;
  padding-bottom: 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
ul {
  list-style-type: none;
  display: flex;
  flex-flow: row;
  justify-content: space-around;
  li {
    padding: 5px;
  }
}
.Menu-body{
  ul{
  display: flex;
  flex-flow: row wrap;
  a{
    text-decoration: none;
  }
  li:hover {
    animation: fadeIn 0.5s;
    animation-fill-mode:forwards;
  }
  }
}
@keyframes fadeIn {
  from {
    background: rgba(245, 255, 157, 0);
  }
  to {
    background: rgb(245, 255, 157);
    opacity: 1;
  }
}
</style>
