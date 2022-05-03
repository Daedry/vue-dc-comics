<template>
  <div id="app">
    <header id="site_header">
      <nav>
        <div class="nav-left">
          <div class="logo">
            <img src="../assets/img/dc-logo.png" alt="" />
          </div>
        </div>
        <div class="nav-right">
          <ul>
            <li><a href="#">characters</a></li>
            <li><a href="#">comics</a></li>
            <li><a href="#">movies</a></li>
            <li><a href="#">tv</a></li>
            <li><a href="#">games</a></li>
            <li><a href="#">collectibles</a></li>
            <li><a href="#">videos</a></li>
            <li><a href="#">fans</a></li>
            <li><a href="#">news</a></li>
            <li><a href="#">shop</a></li>
          </ul>
        </div>
      </nav>
    </header>
    <!-- /#site_header -->
  </div>
</template>

<script>
// import CssColors from './CssColors.vue'

export default {
  name: "HeaderComponent",
  components: {
    //   CssColors
  },
};
</script>

<style lang="scss" scoped>

@import "@/assets/sass/variables";

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#site_header {

  nav {
    width: 100%;
    height: 95.5px;
    background-color: $text-light;
    // background: #000;
    display: flex;
    justify-content: space-evenly;

    .nav-left {
      margin: 0.45rem;

      .logo {

        img {
          width: 65px;
        }
      }
    }

    .nav-right {
      margin: 2rem 0 2.5rem 0;

      ul {
        display: flex;
        li {
          list-style: none;
          padding: 0 0.5rem;

          a {
            padding: 1rem 0 2.58rem;
            text-decoration: none;
            text-transform: uppercase;
            font-size: 12px;
            color: $text-nav;
            font-weight: 600;
            &:hover{
                color: $primary-color;
                border-bottom: 5px solid $primary-color;
            }
            &.active{
                color: $primary-color;
            }
           
          }
        }
      }
    }
  }
}
</style>




