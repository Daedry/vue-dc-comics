<template>
  <footer id="site_footer">
    <div class="container">
      <div class="info-top">
        <div class="infos">
          <div class="info">
            <!-- <ul v-for="(info, index) in infos" :key="index"> -->
            <h5>dc comics</h5>
            <ul>

              <!-- <li>
                <h5>
                  {{ info.title }}
                </h5>
              </li> -->
              <!-- <ul>
                <li v-for="(txt, i) in text" :key="i">
                  <a href="#"> {{ txt[activeText(index)] }} </a>
                </li> -->
                <li><a href="#">Comics</a></li>
                <li><a href="#">Movies</a></li>
                <li><a href="#">TV</a></li>
                <li><a href="#">Games</a></li>
                <li><a href="#">Videos</a></li>
                <li><a href="#">News</a></li>
              <!-- </ul> -->
            </ul>
          </div>

          <div class="info">
            <h5>dc</h5>
            <ul>
              <li><a href="#">Terms Of Use</a></li>
              <li><a href="#">Privacy Policy(New)</a></li>
              <li><a href="#">Ad Choices</a></li>
              <li><a href="#">Advertising</a></li>
              <li><a href="#">Jobs</a></li>
              <li><a href="#">Subscriptions</a></li>
              <li><a href="#">Talent Workshops</a></li>
              <li><a href="#">CPSC Certificates</a></li>
              <li><a href="#">Ratings</a></li>
              <li><a href="#">Shop Help</a></li>
              <li><a href="#">Contact Us</a></li>
            </ul>
          </div>

          <div class="info">
            <h5>sites</h5>
            <ul>
              <ul>
                <li><a href="#">DC</a></li>
                <li><a href="#">MAD Magazine</a></li>
                <li><a href="#">DC Kids</a></li>
                <li><a href="#">DC universe</a></li>
                <li><a href="#">DC Power Visa</a></li>
              </ul>
            </ul>
          </div>

          <div class="info up">
            <h5>Shop</h5>
            <ul>
              <ul>
                <li><a href="#">Shop DC</a></li>
                <li><a href="#">Shop DC Collectibles</a></li>
              </ul>
            </ul>
          </div>
        </div>

        <div class="footer-logo">
          <div class="logo">
            <img src="@/assets/img/dc-logo-bg.png" alt="" />
          </div>
        </div>
      </div>
      <!-- /.info-top -->

      <div class="info-bot">
        <div class="foot-left">
          <a class="btn" href="">sign-up now!</a>
        </div>
        <div class="foot-right">
          <div class="contacts">
            <h3>follow us</h3>
            <ul>
              <li>
                <a href="#">
                  <img src="@/assets/img/footer-facebook.png" alt="" />
                </a>
              </li>
              <li>
                <a href="#">
                  <img src="@/assets/img/footer-twitter.png" alt="" />
                </a>
              </li>
              <li>
                <a href="#">
                  <img src="@/assets/img/footer-youtube.png" alt="" />
                </a>
              </li>
              <li>
                <a href="#">
                  <img src="@/assets/img/footer-pinterest.png" alt="" />
                </a>
              </li>
              <li>
                <a href="#">
                  <img src="@/assets/img/footer-periscope.png" alt="" />
                </a>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <!-- /.info-bot -->
    </div>
    <!-- /.container -->
  </footer>
  <!-- /#site_footer -->
</template>

<script>
export default {
  name: "FooterComponent",
  props: {
    msg: String,
  },

  data: {
    active: 0,
  },

  methods: {
    activeText(i) {
      return (this.active = i);
    },
  },

  data() {
    return {
      infos: [
        {
          title: "dc comics",
          text: [
            "Characters",
            "Comics",
            "Movies",
            "TV",
            "Games",
            "Videos",
            "News",
          ],
        },

        {
          title: "dc",
          text: [
            "Terms Of Use",
            "Privacy Policy(new)",
            "Ad Choises",
            "Advertising",
            "Jobs",
            "Subscriptions",
            "Talent Workshops",
            "CPSC Certificates",
            "Ratings",
            "Shop Help",
            "Contact Us",
          ],
        },

        {
          title: "sites",
          text: [
            "DC",
            "MAD Magazine",
            "DC Kids",
            "DC Universe",
            "DC Power Visa",
          ],
        },
        {
          title: "shop",
          text: ["Shop DC", "Shop DC Collectibles"],
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "@/assets/sass/style.scss";

img {
  width: 100%;
}

#site_footer {
  .container {
    width: 100%;
    height: 400px;
    background-color: #ddd;
    background-image: url("@/assets/img/footer-bg.jpg");
    object-fit: fill;
    position: relative;

    .info-top {
      display: flex;
      overflow-y: hidden;

      .infos {
        display: flex;
        flex-wrap: wrap;
        width: 450px;
        padding-top: 2.5rem;
        margin-left: 18%;
        margin-right: 5rem;

        .info {
          margin-right: 1.75rem;

          h5 {
            text-transform: uppercase;
            color: $text-light;
            font-size: 16px;
            margin-bottom: 0.3rem;
          }

          ul {
            list-style: none;

            li {
              a {
                text-decoration: none;
                color: $text-main;
                font-size: 12px;
              }
            }
          }
        }
        .up {
          margin-top: -7.5rem;
        }
      }

      .footer-logo {
        .logo {
          width: 450px;
          margin-top: -4.6rem;
        }
      }
    }

    .info-bot {
      width: 100%;
      height: 100px;
      background-color: $bg-footer;
      z-index: 100;
      position: absolute;
      bottom: 0;
      left: 0;
      display: flex;
      justify-content: space-around;

      .foot-left {
        margin-right: 10rem;
        margin-left: 3rem;
        padding: 2.5rem;

        a {
          text-decoration: none;
          color: $text-light;
          font-size: 18px;
          text-transform: uppercase;
          padding: 0.75rem;
          border: 2px solid $primary-color;
          font-weight: 500;
        }
      }

      .foot-right {
        .contacts {
          display: flex;
          color: $primary-color;
          font-size: 18px;
          text-transform: uppercase;

          h3 {
            padding: 2.25rem 0.5rem 2rem 0;
          }

          ul {
            display: flex;

            li {
              list-style: none;
              padding: 2.25rem 0.45rem;

              img {
                width: 28px;
              }
            }
          }
        }
      }
    }
  }
}
</style>