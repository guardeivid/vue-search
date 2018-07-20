<template>
  <li class="ListItem">
    <div class="card">
      <img
        class="card-img-top"
        :src="srcImage"
        alt=""
      />
      <div class="card-body">
        <h5 class="card-title">{{ result7.name }}</h5>
        <p class="card-text">{{ result7.description }}</p>
      </div>
    </div>
  </li>
</template>

<script>

/*
{
  "code": 200,
  "status": "Ok",
  "copyright": "© 2018 MARVEL",
  "attributionText": "Data provided by Marvel. © 2018 MARVEL",
  "attributionHTML": "<a href=\"http://marvel.com\">Data provided by Marvel. © 2018 MARVEL</a>",
  "etag": "66961e7f1fa28ddc49464824e015afb0a97bd046",
  "data": {
    "offset": 0,
    "limit": 20,
    "total": 19,
    "count": 19,
    "results": [{
      "id": 1009220,
      "name": "Captain America",
      "description": "Vowing to serve his country any way he could, young Steve Rogers took the super soldier serum to become America's one-man army. Fighting for the red, white and blue for over 60 years, Captain America is the living, breathing symbol of freedom and liberty.",
      "modified": "2016-09-06T11:37:19-0400",
      "thumbnail": {
        "path": "http://i.annihil.us/u/prod/marvel/i/mg/3/50/537ba56d31087",
        "extension": "jpg"
      },
*/
  export default {
    data({ result7: { name, description, thumbnail }}) {
      const { path, extension } = thumbnail
      const srcImage = `${path}.${extension}`
      return { name, description, srcImage }
    },
    props: {
      result7: Object
    }
  }
</script>

<style scoped>
  .ListItem {
    display: inline-block;
    width: 100%;
    margin: 1rem 0;
  }
</style>
