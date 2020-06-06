<template>
  <div class="home">

    <div class="list">

      <!-- zopakovat pro každý film v seznamu -->
      <div class="film">
        <div class="rank">
          10.
        </div>
        <div class="cover">
          <img src="./../assets/images/pelisky.jpg" alt="Pelíšky">
        </div>
        <div class="meta">
          <h3>Pelíšky</h3>
          <p>1999, 116 min</p>
        </div>
      </div>
      <!-- konec filmu -->

    </div>

  </div>
</template>

<script>
import filmData from './../assets/data.js';

export default {
  name: 'Home',

  data() {
    return {
      filmy: filmData
    }
  }

}
</script>

<style>

.list {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(5, auto);
  grid-auto-flow: column;
  gap: 20px;
}

.film {
  padding: 10px;
  display: flex;
  align-items: center;
  border: 1px solid rgb(40, 0, 100);
  border-radius: 4px;
  box-shadow: 3px 2px 5px rgba(40, 0, 100, 0.2);
}

.rank {
  flex: 0 0 40px;
  font-size: 24px;
  font-weight: bold;
  text-align: center;
  margin-right: 20px;
}

.cover {
  flex: 0 0 40px;
  margin-right: 20px;
}

.cover img {
  width: 40px;
  height: auto;
}

.meta {
  flex: 1;
}

.meta h3 {
  margin: 0 0 5px 0;
  font-size: 16px;
  color: #446;
}

.meta p {
  margin: 5px 0 0 0;
  font-size: 14px;
  color: #888;
}

</style>