<template>
  <div id="app">
    <main id="site_main">
      <div class="container">
        <div class="content">
          <div class="content-top">
            <button>Current series</button>
          </div>
          <div class="content-bot">
            <div class="content-cards">

              <div class="content-card" v-for="(card, index) in cards" :key="index">
                <div class="content-card-img">
                  <img :src="card.thumb" alt=""/>
                </div>
                <div class="content-card-text">
                  <h4>{{card.series}}</h4>
                </div>
              </div>

            </div>
            <!-- /.content-cards -->
          </div>
          <!-- /.content-bot -->
        </div>
        <!-- /.content -->

        <div class="info-buy">
          <div class="cards">
            <div class="card" v-for="(card, index) in cards" :key="index">
              <div class="card-img">
                <img :src="card.image" alt="" />
              </div>
              <div class="card-text">
                <p>{{ card.text }}</p>
              </div>
            </div>
            <!-- /.card -->
          </div>
          <!-- /.cards -->
        </div>
        <!-- /.info-buy -->
      </div>
      <!-- /.container -->
    </main>
    <!-- /#site_main -->
  </div>
</template>

<script>
export default {
  name: "MainComponent",
  props: {
    msg: String,
  },

  data() {
    return {
      cards: [
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        },
      ],
    };
  },

  // data() {
  //   return {
  //     cards: [
  //       {
  //         image: require("@/assets/img/buy-comics-digital-comics.png"),
  //         text: "Digitals comics",
  //       },

  //       {
  //         image: require("@/assets/img/buy-comics-merchandise.png"),
  //         text: "dc merchandise",
  //       },

  //       {
  //         image: require("@/assets/img/buy-comics-subscriptions.png"),
  //         text: "subsctiption",
  //       },

  //       {
  //         image: require("@/assets/img/buy-comics-shop-locator.png"),
  //         text: "comic shop locator",
  //       },

  //       {
  //         image: require("@/assets/img/buy-dc-power-visa.svg"),
  //         text: "dc power visa",
  //       },
  //     ],
  //   };
  // },
};
</script>

<style scoped lang="scss">
@import "@/assets/sass/style.scss";

img {
  width: 100%;
}

#site_main {
  .container {
    width: 100%;

    .content {
      height: 1000px;
      background-color: $bg-main;
      display: flex;
      align-items: center;
      flex-direction: column;
      width: 100%;
      position: relative;

      .content-top {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        aspect-ratio: 1 / 0.21;
        background-image: url(@/assets/img/jumbotron.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        z-index: 1;

        button{
          border: none;
          background-color: $primary-color;
          color: $text-light;
          font-weight: 600;
          font-size: 16px;
          text-transform: uppercase;
          padding: 0.5rem 0.75rem;
          position: absolute;
          bottom: -1rem;
          left: 18%;
        }
      }

      .content-bot {
        width: 100%;
        position: absolute;
        top: 350px;
        left: 0;

        .content-cards {
          display: flex;
          row-gap: 1rem;
          column-gap: 1.5rem;
          flex-wrap: wrap;
          width: 70%;
          margin: 0 19%;

          .content-card {
            width: calc(100% / 6 - 2rem);
            column-gap: 1.5rem;
            // width: 130px;
            // height: 200px;
            // border: 2px solid black;
            // background-color: red;

            .content-card-img {
              // background-color: blue;

              img {
                // width: 150px;
                // height: 200px;
                object-fit: cover;
              }
            }

            .content-card-text {
              h4 {
                color: $text-light;
                font-weight: 600;
                font-size: 15px;
                padding: 1rem 0;
                text-transform: uppercase;
              }
            }
          }
        }
      }

      h3 {
        color: $text-light;
        margin-left: 20%;
        font-size: 24px;
      }
    }

    .info-buy {
      width: 100%;
      background-color: $primary-color;
      z-index: 1;
      // padding: 1.5rem 0;

      .cards {
        margin: 0 20%;
        display: flex;

        .card {
          display: flex;
          padding: 2.5rem 0;

          .card-img {
            text-align: center;
            // margin-top: 0.65rem;
            img {
              // width: 40px;
              height: 40px;
            }
          }

          .card-text {
            // padding: 1.5rem 1rem 1.5rem 1rem;
            margin: 1rem;

            p {
              width: 150px;
              font-size: 11px;
              text-transform: uppercase;
              color: $text-light;
            }
          }
        }
        /* /.card */
      }
      /* /.cards */
    }
  }
}
</style>

