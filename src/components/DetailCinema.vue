<template>
    <div class="container">
        <div class="movie" v-for="(data, index) in movie" :value="data" :key="index">
            <div class="movie-item" v-if="filmId == data.id">
                <h1 class="page-title">Movie Details</h1>
                <img v-bind:src="data.image"  class="img-fluid img-movie" v-bind:alt="data">
                <div>
                    <h1>{{data.title}}</h1>
                    <h2>IMDb : {{data.rating}}</h2>
                    <h4>{{data.release}} | {{data.duration}} | {{data.genre}} | {{data.age}}</h4>
                    <br/><br/>
                    <p>Director : {{data.director}}</p>
                    <p>Cast by : {{data.cast}}</p>
                    <h4>SYNOPSYS</h4>
                    <p class="desc">{{data.desc}}</p>
                </div>
            </div>
        </div>
        <div class="back">
            <router-link to='/'><button class="btn-back">BACK TO HOME</button></router-link>
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
  data() {
    return {
      filmId: this.$route.params.id,
      movie: [
        {
          id: 1,
          image: Img1,
          title: 'Kajeng Kliwon',
          rating: '0,0/10',
          release: 'Now Playing',
          duration: '-',
          genre: 'Drama , Horror',
          age: '17+',
          director: 'Bambang Drias',
          cast: 'Amanda Manopo, Christ Laurent, Vincent Andrianto, Muthia datau, Indah Kalalo, Cathrine Wilson, Egi fedly, Weda Nanda, Deva Wisesa, Atikah Suheimi',
          desc: 'Agni (Amanda Manoppo) seorang dokter muda asli Bali, akan menikahi kekasihnya, Nicho (Chris Laurent) seorang fotografer dari Jakarta.',
        },
        {
          id: 2,
          image: Img2,
          title: 'Little Woman',
          rating: '8,6/10',
          release: 'June 24, 2019 (Indonesia)',
          duration: 'Now Playing',
          genre: 'Drama, Romance',
          age: '13+',
          director: 'Greta Gerwig',
          cast: 'Saoirse Ronan, Emma Watson, Florence Pugh, Eliza Scanlen, Timothee Chalamet, Laura Dern, Meryl Streep, Chris Cooper, Louis Garrel, Tracy Letts, James Norton, Bob Odenkirk',
          desc: 'Little Women berkisah tentang empat remaja putri kakak beradik yang memiliki obsesi dan cita-cita. Keempatnya mengambil jalan masing-masing demi apa yang mereka yakini.',
        },
        {
          id: 3,
          image: Img3,
          title: 'Toko Barang Mantan',
          rating: '8,6/10',
          release: 'Now Playing',
          duration: '98 Minutes',
          genre: 'Comedy, Romance',
          age: '13+',
          director: 'Viva Westi',
          cast: 'Reza Rahadian, Marsha Timothy, Iedil Dzuhrie Alaudin, Dea Panendra, Syifa Hadju, Niken Anjani, Brigitta Cynthia, Chrismanto Ronaldo (Cemen), Ibob Tarigan, Martin Anugrah, Fendy Chow, Stella Cornelia,',
          desc: 'Toko Barang Mantan adalah toko jual-beli barang-barang mantan bagi orang-orang yang ingin move-on dari mantannya. Sebagai pencetus ide, pendiri dan pemiliknya, Tristan rela meninggalkan kuliah hukumnya demi bisa fokus mengembangkan toko ini bersama sahabatnya, Amel dan Rio. Berbagai macam kisah-kisah sedih, lucu dan absurd tentang barang-barang tersebut menjadi makanan mereka sehari-hari. Tristan bangga dengan toko ini meskipun akhir-akhir ini sepi dan mulai bermasalah secara finansial. ',
        },
        {
          id: 4,
          image: Img4,
          title: 'Brahms : The Boy II',
          rating: '6,5/10',
          release: 'July 31, 2019 (Indonesia)',
          duration: '86 Minutes',
          genre: 'Horror, Mystery, Thriller',
          age: '17+',
          director: 'Matt Berenson, Roy Lee, Gary Lucchesi',
          cast: 'Katie Holmes, Owain Yeoman, Ralph Ineson, Christopher Convery, Anjali Jay, Oliver Rice, Natalie Moon, Joely Collins, Charles Jarman, Joanne Kimm, Ellie King',
          desc: 'Luke Hobbs and Deckard Shaw, Hatties brother, are both informed of the missing virus and are reluctantly assigned to work together to track it down. After a brief meeting at a CIA black site at Leadenhall Building, Deckard goes to Hatties house for information, while Hobbs manages to find Hattie, after a brief scuffle, he brings her to the CIA office, as Deckard then returns. The office is attacked, and Hattie is taken by Brixton, whom Deckard recognizes as an old colleague-turned-enemy hed previously shot and supposedly killed. Hobbs and Deckard pursue and rescue Hattie during an ensuing car chase, managing to escape from Brixton, who crashes into a double-decker bus. However, Brixton frames all three as traitors via Eteons control of global news media.',
        },
        {
          id: 5,
          image: Img5,
          title: 'I am Mother',
          rating: '7,7/10',
          release: 'October 19, 2018 (Indonesia)',
          duration: '2h 16min',
          genre: 'Drama, Music, Romance',
          age: '17+',
          director: 'Bradley Cooper',
          cast: 'Lady Gaga, Bradley Cooper, Sam Elliott, and many more.',
          desc: 'Jackson "Jack" Maine, a famous country-rock singer, privately battling an alcohol and drug addiction, plays a concert. His main support is Bobby, his manager and older half-brother. After a show, Jack goes out for drinks and visits a drag bar where he witnesses a tribute performance to Edith Piaf by Ally, who works as a waitress and singer-songwriter. Jack is amazed by her performance, and they spend the night talking to each other, where Ally discloses to him her unsuccessful efforts in pursuing a professional music career. Ally shares with Jack some lyrics she has been working on, and Jack tells Ally she is a talented songwriter and should perform her own material.',
        },
        {
          id: 6,
          image: Img6,
          title: '4 Mantan',
          rating: '6,2/10',
          release: 'June 6, 2018 (Indonesia)',
          duration: '2h 8min',
          genre: 'Action, Adventure, Sci-Fi',
          age: '13+',
          director: 'J.A. Bayona',
          cast: 'Chris Pratt, Bryce Dallas Howard, Rafe Spall, and many more.',
          desc: 'In 2018, a U.S. Senate hearing in Washington, D.C. debates whether Isla Nublars dinosaurs should be saved from an impending volcanic eruption. Mathematician Dr. Ian Malcolm testifies that the dinosaurs should be allowed to die to correct John Hammond wrongfully cloning them. Meanwhile, Jurassic Worlds former operations manager, Claire Dearing, has established the Dinosaur Protection Group to save the animals. After the Senate rules against rescuing the animals, Hammonds former partner, Benjamin Lockwood, summons Claire to his Northern California estate. Lockwood and his aide, Eli Mills, reveal a plan to relocate the dinosaurs to a new island sanctuary. Claire is needed to reactivate the parks dinosaur tracking system to locate the animals, particularly Blue, the last surviving Velociraptor. Though they are now estranged, Claire recruits Owen Grady, Jurassic Worlds former Velociraptor trainer, to help capture her.',
        },
        {
          id: 7,
          image: Img7,
          title: 'Sonic The Hedhegog',
          rating: '8,0/10',
          release: 'October 30, 2018 (Indonesia)',
          duration: '2h 14min',
          genre: 'Biography, Drama, Music',
          age: '17+',
          director: 'Bryan Singer',
          cast: 'Rami Malek, Lucy Boynton, Gwilym Lee, and many more.',
          desc: 'Bohemian Rhapsody is a 2018 biographical drama film about Freddie Mercury, the lead singer of the British rock band Queen. It was directed by Bryan Singer from a screenplay by Anthony McCarten, and produced by Graham King and Queen manager Jim Beach. It stars Rami Malek as Mercury, with Lucy Boynton, Gwilym Lee, Ben Hardy, Joe Mazzello, Aidan Gillen, Tom Hollander, Allen Leech, and Mike Myers in supporting roles. Queen members Brian May and Roger Taylor served as consultants. A British-American venture, the film was produced by 20th Century Fox, Regency Enterprises, GK Films, and Queen Films, with Fox serving as distributor. The film follows the singers life from the formation of the band up to their 1985 Live Aid performance at the original Wembley Stadium.',
        },
        {
          id: 8,
          image: Img8,
          title: 'Bhoot : The Haunted Ship',
          rating: '6,6/10',
          release: 'May 24, 2017 (Indonesia)',
          duration: '2h 9min',
          genre: 'Action, Adventure, Fantasy',
          age: '13+',
          director: 'Joachim Rønning, Espen Sandberg',
          cast: 'Johnny Depp, Geoffrey Rush, Javier Bardem, and many more.',
          desc: 'Thirteen years after the events of At Worlds End, twelve-year-old Henry Turner boards the Flying Dutchman and informs his father, Will Turner, that the curse which binds Will to the Dutchman and only permits him to step on land once a decade can be broken by the Trident of Poseidon. Henry intends to recruit Captain Jack Sparrow to help find it, but Will believes this is impossible and orders Henry to leave. Will and the Dutchman then disappear into the sea, but Henry vows to find Jack and the Trident. Nine years later, Henry is a sailor in the British Royal Navy. The ship sails into the supernatural Devils Triangle and stumbles upon the wreck of the Silent Mary, whose ghostly crew led by Spanish pirate-hunter Captain Salazar attack. Salazar spares Henrys life to deliver a message to Jack: Salazar is coming for him.',
        },
      ],
    };
  },
};
</script>
<style scoped>
    .container {
        width: auto;
    }
    .movie-item {
        padding: 5px 20px;
        width: auto;
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-auto-rows: minmax(50px, auto);
        text-align: left;
        background-color: #ffeaa7;
    }
    .page-title {
        grid-column: 1/3;
        text-align: center;
        padding: 10px;
        background-color: #ffeaa7;
        color: #cd6133;
        font-family: 'Times New Roman', Times, serif;
    }
    .back {
      text-align: center;
      padding-bottom: 50px;
      background-color: #ffeaa7;
    }
    .btn-back {
        background-color: #474787;
        color: #fff;
        border: 0px;
        border-radius: 60px;
        text-align: center;
        margin: 5px 2px;
        padding: 20px 15px;
        cursor: pointer;
        transition: 0.3s;
        margin: 20px;
        width: 300px;
    }
    .btn-back:hover {
        background-color: transparent;
        border: 2px solid #474787;
        color: #474787;
    }
    .img-movie {
        width: 370px;
        box-shadow: 0 20px 25px 0 rgba(0,0,0,0.2);
        transition: 0.3s ease;
        margin-left: 120px;
    }
    .desc {
        text-align: justify;
    }
</style>