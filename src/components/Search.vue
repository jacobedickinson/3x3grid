<template>
  <div class="app">
    <div class="search-wrapper">
      <input type="text" v-model="search" placeholder="Search title.." />
      <br />
      <br />
    </div>
    <div class="wrapper">
      <div class="card" v-for="game in filteredList">
        <a v-bind:href="game.link" target="_blank">
          <img v-bind:src="game.img" style="max-width: 3em;" />
          {{ game.title }}
        </a>
      </div>
    </div>
  </div>
</template>

<script>
class Game {
  constructor(title, link, author, img) {
    this.title = title;
    this.link = link;
    this.img = img;
  }
}
export default {
  data: function () {
    return {
      search: "",
      postList: [
        new Game(
          "GTA",
          "https://www.rockstargames.com/grandtheftauto/",
          "",
          "https://1000logos.net/wp-content/uploads/2018/03/GTA-Logo.png"
        ),
        new Game(
          "Zelda",
          "https://www.zelda.com/",
          "",
          "https://upload.wikimedia.org/wikipedia/commons/2/2a/Zelda_Logo.svg"
        ),
        new Game(
          "OverWatch",
          "https://playoverwatch.com/en-gb/",
          "",
          "https://upload.wikimedia.org/wikipedia/en/thumb/5/51/Overwatch_cover_art.jpg/220px-Overwatch_cover_art.jpg"
        ),
        new Game(
          "Sonic",
          "https://www.sonicdrivein.com/",
          "",
          "https://pbs.twimg.com/profile_images/1245027802287468545/TGO8O6_a.jpg"
        ),
        new Game(
          "Spyro",
          "https://www.spyrothedragon.com/",
          "",
          "https://upload.wikimedia.org/wikipedia/en/thumb/5/53/Spyro.png/220px-Spyro.png"
        ),
        new Game(
          "Cod",
          "https://www.googleadservices.com/pagead/aclk?sa=L&ai=DChcSEwj7x67s9vnrAhUDqncKHWX8C70YABAAGgJlZg&ohost=www.google.com&cid=CAESQOD2ba2JowKIK5-wlNcadsE948jM3iJhaP9GxUGFOGU5HFCiJofeyd0U7ld8nGqzhrJj5DhKI4bgnsECQMU_X9Y&sig=AOD64_3NEYUiQUxoNo0tAzbhaWeIHDQwEA&q&adurl&ved=2ahUKEwjb5KPs9vnrAhVH2qQKHb6eAmoQ0Qx6BAggEAE",
          "",
          " https://www.callofduty.com/content/dam/atvi/callofduty/cod-touchui/warzone/social/wz-social-share.jpg"
        ),
        new Game(
          "Fortnite",
          "https://www.epicgames.com/fortnite/en-US/home",
          "",
          "https://cdn02.nintendo-europe.com/media/images/10_share_images/games_15/nintendo_switch_download_software_1/H2x1_NSwitchDS_Fortnite_Chapter2Season4_image1280w.jpg"
        ),
        new Game(
          "APEX",
          "https://www.ea.com/games/apex-legends",
          "",
          "https://psmedia.playstation.com/is/image/psmedia/apex-legends-listing-thumb-01-ps4-en-06feb19_1549464045151?$Icon$"
        ),
        new Game(
          "PUBG",
          "https://www.pubg.com/",
          "",
          "https://gamespot1.cbsistatic.com/uploads/scale_medium/1576/15769789/3246445-imagepu.jpg"
        ),
        new Game(
          "HyperScape",
          "https://www.ubisoft.com/en-gb/game/hyper-scape",
          "",
          "https://store.ubi.com/dw/image/v2/ABBS_PRD/on/demandware.static/-/Sites-masterCatalog/default/dwd4621a01/images/large/5ed4f98e5cdf9a1528a8c206.jpg?sw=341&sh=450&sm=fit"
        ),
      ],
    };
  },
  computed: {
    filteredList() {
      return this.postList.filter((game) => {
        return game.title.toLowerCase().includes(this.search.toLowerCase());
      });
    },
  },
};
</script>
<style scoped>
.wrapper {
  max-width: 3em;
  margin: auto;
}
</style>