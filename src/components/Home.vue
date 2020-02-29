<template>
    <div class="container">
        <div class="header">
            <h1 class="header-title">INDO CINEMA</h1>
            <h3 class="header-subtitle">COmplete Indonesian Cinema Web | Horror | Action | Romance | etc</h3>
        </div>
        <div class="movie" v-for="(data, index) in movie" :value="data" :key="index">
            <div class="movie-item" @click="detailfilm(data.id)">
                <img v-bind:src="data.image" class="img-fluid img-movie" v-bind:alt="data">
            </div>
            <div class="movie-title">
                {{data.title}}
            </div>
        </div>
        <div class="footer">
            <h5>Copyright &copy;2020. Created by Naufal Rinaldi. All rights reserved</h5>
        </div>
    </div>
</template>
<script>
import Img1 from '../assets/movie/kajeng.jpg';
import Img2 from '../assets/movie/Little.jpg';
import Img3 from '../assets/movie/toko.jpg';
import Img4 from '../assets/movie/brahms.jpg';
import Img5 from '../assets/movie/mother.jpg';
import Img6 from '../assets/movie/mantan.jpg';
import Img7 from '../assets/movie/sonic.jpg';
import Img8 from '../assets/movie/bhoot.jpg';
export default {
  data: () => ({
    movie: [
      { id: 1, image: Img1, title:"Kajeng Kliwon" },
      { id: 2, image: Img2, title:"Little Woman" },
      { id: 3, image: Img3, title:"Toko Barang Mantan" },
      { id: 4, image: Img4, title:"Brahms : The Boy II" },
      { id: 5, image: Img5, title:"I Am Mother" },
      { id: 6, image: Img6, title:"4 Mantan" },
      { id: 7, image: Img7, title:"Sonic : The Hedgehog" },
      { id: 8, image: Img8, title:"Bhoot" },
    ],
  }),
  methods: {
    detailfilm(filmId) {
      this.$router.push({ name: 'detail', params: { id: filmId } });
    },
  },
};
</script>
<style scoped>
    .container {
        width: auto;
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-auto-rows: minmax(50px, auto);
    }
    .header {
        padding: 30px;
        grid-column: 1/5;
        background-color: #fdcb6e;
        color: #fff;
        text-align: center;
        padding-bottom: 10px;
    }
    .header-title {
      font-family: monospace;
      font-size: 100px;
      color: #aaa69d;
    }
    .header-subtitle {
        padding-bottom: 50px;
        font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
        font-size: 20px;
        color: #fff;
    }
    .footer {
        padding: 10px;
        grid-column: 1/5;
        background-color: #fdcb6e;
        color: #fff;
        text-align: center;

    }
    .movie {
        padding-top: 60px;
        padding-bottom: 60px;
        text-align: center;
        background-color: #ffeaa7;
    }
    .movie-title {
        padding-top: 20px;
        font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
        font-size : 25px;
    }
    .img-movie {
        width: 250px;
        box-shadow: 0 20px 35px 0 rgba(0,0,0,0.2);
        transition: 0.3s ease;
    }
    .img-movie:hover{
        box-shadow: 0 40px 45px 0 rgba(0,0,0,0.2);
    }
</style>