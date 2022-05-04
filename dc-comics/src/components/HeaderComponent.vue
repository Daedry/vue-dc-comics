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
            <li v-for="(el, index) in nav" :key="index">
              <a href="#">
                {{ el.text }}
              </a>
            </li>
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

  data() {
    return {
      nav: [
        {
          id: "",
          text: "characters",
        },
        {
          id: "",
          text: "comics",
        },
        {
          id: "",
          text: "movies",
        },
        {
          id: "",
          text: "tv",
        },
        {
          id: "",
          text: "games",
        },
        {
          id: "",
          text: "collectibles",
        },
        {
          id: "",
          text: "videos",
        },
        {
          id: "",
          text: "fans",
        },
        {
          id: "",
          text: "news",
        },
        {
          id: "",
          text: "shop",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/sass/style.scss";

#site_header {
  nav {
    width: 100%;
    height: 100px;
    background-color: $text-light;
    display: flex;
    justify-content: space-evenly;

    .nav-left {
      margin: 0.75rem;

      .logo {
        img {
          width: 75px;
        }
      }
    }

    .nav-right {
      margin: 2.5rem 0;

      ul {
        display: flex;
        li {
          list-style: none;
          padding: 0 0.5rem;

          a {
            padding: 2.4rem 0;
            text-decoration: none;
            text-transform: uppercase;
            font-size: 12px;
            color: $text-nav;
            font-weight: 600;
            border-bottom: 5px solid transparent;
            transition: 0.35s;
            &:hover {
              color: $primary-color;
              border-bottom: 5px solid $primary-color;
            }
            &.active {
              color: $primary-color;
            }
          }
        }
      }
    }
  }
}
</style>




