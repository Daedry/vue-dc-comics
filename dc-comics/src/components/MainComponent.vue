<template>
  <div id="app">
    <main id="site_main">
      <div class="container">
        <div class="content">
          <h3>Content goes here</h3>
          <!-- /.content -->
        </div>

        <div class="info-buy">
          <div class="cards">

            <div class="card">
              <div class="card-img">
                <img  src="@/assets/img/buy-comics-digital-comics.png" alt="" />
              </div>
              <div class="card-text">
                <p>Digitals comics</p>
              </div>
            </div>
              <!-- /.card -->

              <div class="card">
              <div class="card-img">
                <img src="@/assets/img/buy-comics-merchandise.png" alt="" />
              </div>
              <div class="card-text">
                <p>dc merchandise</p>
              </div>
            </div>
              <!-- /.card -->

              <div class="card">
              <div class="card-img">
                <img src="@/assets/img/buy-comics-subscriptions.png" alt="" />
              </div>
              <div class="card-text">
                <p>Digitals comics</p>
              </div>
            </div>
              <!-- /.card -->

              <div class="card">
              <div class="card-img">
                <img class="sizing-img" src="@/assets/img/buy-comics-shop-locator.png" alt="" />
              </div>
              <div class="card-text">
                <p>Digitals comics</p>
              </div>
            </div>
              <!-- /.card -->

              <div class="card">
              <div class="card-img">
                <img class="align-img" src="@/assets/img/buy-dc-power-visa.svg" alt="" />
              </div>
              <div class="card-text">
                <p>Digitals comics</p>
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
};
</script>

<style scoped lang="scss">
@import "@/assets/sass/variables";

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

img{
  width: 100%;
}

#site_main {
  .container {
    width: 100%;
    
    

    .content {
      height: 80px;
      background-color: $bg-main;
      display: flex;
      align-items: center;

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
            width: 40px;
            height: 35px;
            text-align: center;
            // margin-top: 0.65rem;

            .sizing-img {
              width: 25px;
            }

            .align-img{
              margin-top: 0.5rem;
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

