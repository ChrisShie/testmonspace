<template>
  <b-container id="index">
    <section id="tab1">
        <b-card
            overlay
            img-src="https://picsum.photos/900/250/?image=3"
            img-alt="Card Image"
            text-variant="white"
            title="Image Overlay"
            sub-title="Subtitle"
          >
            <b-card-text>
              Some quick example text to build on the card and make up the bulk of the card's content.
            </b-card-text>
          </b-card>
    </section>
    <section id="tab2" class="shadow-box">
      <b-row>
        <b-col>
          <h1>Kategori Pilihan</h1>
          <b-card-group>
            <b-card
                align="center"
                overlay
                img-src="https://picsum.photos/400/400/?image=20"
                img-alt="Card Image"
              >
                <b-card-text>
                  <b>Makanan</b><br/>Kering
                </b-card-text>
              </b-card>
              <b-card
                align="center"
                overlay
                img-src="https://picsum.photos/400/400/?image=20"
                img-alt="Card Image"
              >
                <b-card-text>
                  <b>Aksesoris</b><br/>Laptop
                </b-card-text>
              </b-card>
              <b-card
                align="center"
                overlay
                img-src="https://picsum.photos/400/400/?image=20"
                img-alt="Card Image"
              >
                <b-card-text>
                  <b>Figure</b>
                </b-card-text>
              </b-card>
              <b-card
                align="center"
                overlay
                img-src="https://picsum.photos/400/400/?image=20"
                img-alt="Card Image"
              >
                <b-card-text>
                  <b>Coffee & Tea</b><br/>Maker
                </b-card-text>
              </b-card>
          </b-card-group>
        </b-col>
        <b-col>
          <div>
            <h1>Top-Up & Tagihan</h1>
            <b-link class="float-right">Lihat Semua</b-link>
          </div>
        </b-col>
      </b-row>
      <b-row class="mt-3">
        <b-col>
          <b-button pill variant="outline-secondary">Tag Name</b-button>
        </b-col>
      </b-row>
    </section>
    <section>
      <b-alert show variant="primary" dismissible >Primary Alert</b-alert>
    </section>
    <section id="tab3">
      <h1>Paling Banyak Dicari</h1>
      <b-card-group>
       <b-card v-for="i in [1,2,3,4]" :key="i" no-body class="shadow-box" style="max-width: 540px;">
        <b-row no-gutters>
          <b-col md="4">
            <b-card-img src="https://picsum.photos/400/400/?image=20"></b-card-img>
          </b-col>
          <b-col md="8">
            <b-card-body>
              <b-card-text>
                <h1>Nama</h1>
                <p>Desc</p>
              </b-card-text>
            </b-card-body>
          </b-col>
        </b-row>
      </b-card>
      </b-card-group>
    </section>
    <section id="tab4">
      <b-row>
        <b-col>
          <div>
            <h1>Official Store</h1>
            <b-link class="float-right">Lihat Semua</b-link>
          </div>
           <b-img src="https://picsum.photos/1024/400/?image=41" fluid alt="Responsive image"></b-img>
        </b-col>
        <b-col>
          <h1>Top Trending</h1>
          <b-card-group>
            <b-card
                v-for="i in [1,2,3]" :key="i"
                align="center"
                img-src="https://picsum.photos/400/400/?image=20"
                img-alt="Card Image"
              >
                <b-card-text>
                  <b>Makanan</b><br/>Kering
                </b-card-text>
              </b-card>
          </b-card-group>
        </b-col>
      </b-row>
    </section>
    <section id="tab4">
      <b-card no-body>
        <b-tabs pills>
          <b-tab title="Tab 1" active>
              <b-card-group deck>
                <b-card title="Title" img-src="https://picsum.photos/300/300/?image=41" img-alt="Image" img-top>
                  <b-card-text>
                    This is a wider card with supporting text below as a natural lead-in to additional content.
                    This content is a little bit longer.
                  </b-card-text>
                  <template v-slot:footer>
                    <small class="text-muted">Last updated 3 mins ago</small>
                  </template>
                </b-card>
            </b-card-group>
          </b-tab>
          <b-tab title="Tab 2">
              b
          </b-tab>
        </b-tabs>
      </b-card>
    </section>
  </b-container>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
    section{
        margin-top: 24px;
        h1{
            display: inline-block;
            font-size: 24px;
            margin-bottom: 15px;
        }
    }
    .shadow-box{
        border-radius: 10px;
        box-shadow: 0 0 5px rgba(0,0,0,.3);
        &#tab2{
            padding: 15px 20px;
        }
    }
    .card {
        border: none;
        border-radius: 10px;
        margin: 0 5px 0 5px;
        &:first-child{
            margin-left: 0;
        }
        &:last-child{
            margin-right: 0;
        }
        h1{
            font-size: 20px;
        }
        .card-img{
            border-radius: 10px;
        }
    }
    #tab3{
        .card-group{
           .card{
               border-radius: 10px;
               .card-img{
                   border-radius: 10px;
                   margin: 5px;
               }
                .card-body{
                    padding: 10px;
                }
            } 
        }
        
    }
</style>
