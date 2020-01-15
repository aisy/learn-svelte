<script>
  import { onMount } from "svelte";
  import NavbarHeader from "../components/NavbarHeader.svelte";
  import HomeItemLists from "../components/HomeItemLists.svelte";
  import Introductions from "../components/Introductions.svelte";
  import Carousel from "../components/Carousel.svelte";

  let name = "ais";
  let dataItem = [];

  onMount(async () => {
    const res = await fetch(
      "https://facebook.github.io/react-native/movies.json"
    );
    dataItem = await res.json();
  });
</script>

<style>
  main {
    text-align: center;
    padding: 0px 25px;
    max-width: 240px;
    margin: 0 auto;
    margin-top: 50px;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  p {
    font-size: 20px;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<NavbarHeader />
<Introductions />

<main>
  <Carousel />
  <HomeItemLists items={dataItem.movies} />
</main>
