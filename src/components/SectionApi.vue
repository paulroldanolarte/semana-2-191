<template>
  <!-- Inicio Noticia 1 -->

  <div>
    <div class="row mt-md-5 mt-sm-5 mt-xs-5">
      <div
        class="col-lg-6 col-xs-12"
        v-for="(movie, index) of movies"
        :key="index"
      >
        <div class="d-flex justify-content-center align-items-center">
          <div class="p-3">
            <!-- <img :src="movie.Poster" alt="movie poster"> -->
            <img
              :src="movie.urlToImage"
              alt="movie poster"
              width="400"
              height="500"
            />
          </div>
          <div></div>

          <div class="p-2">
            <!-- <h2>{{movie.Title}}</h2> -->
            <h2>{{ movie.title }}</h2>
            <hr />

            <p>
              <!-- Durante los duros cambios que ha enfrentado el mundo por cuenta de
              la actual pandemia, la producción de alimentos es quizás la única
              actividad que nunca descansó, pero hay nuevos retos para
              garantizar que el agro mantenga su sostenibilidad y
              competitividad. -->
              {{ movie.description }}
            </p>
          </div>
        </div>
        <div class="d-flex container-fluid justify-content-end pb-2 mt-n2">
          <!-- <button href="https://www.elpais.com.co/informacion-comercial/ingenieria-agronomica-hacia-un-agro-4-0-y-de-mayor-competitividad.html" type="button" class="btn btn-outline-info">Seguir Leyendo</button> -->
          <!-- <a :href="'https://www.imdb.com/title/'+movie.imdbID" class="btn btn-outline-info"> Info </a>    -->
          <a :href="movie.url" class="btn btn-outline-info"> Info </a>
        </div>
      </div>
    </div>
  </div>

  <!-- Fin Noticia 1 -->
</template>

<script>
import axios from "axios";

export default {
  name: "SectionApi",
  data() {
    return {
      movies: null,
    };
  },
  mounted() {
    //
    // http://www.omdbapi.com/?s=farm&type=movie&apikey=b03e19bc
    axios
      .get(
        "http://newsapi.org/v2/everything?q=agroindustria&from=2020-11-06&sortBy=publishedAt&apiKey=cd2fa6b371004161b489913b4ecb00d5"
      )
      .then((response) => {
        // this.movies = response.data.Search.slice(0, 4);
        this.movies = response.data.articles.slice(1, 5);
        console.log(this.movies);
      });
  },
};
</script>


<style scoped>
</style>