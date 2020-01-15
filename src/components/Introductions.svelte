<script>
  import Button from "./ButtonComponent.svelte";
</script>

<style>
  .introduction-container {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 700px;
    padding: 10px;
  }
  .introduction-text {
    text-align: left;
  }

  .title {
    font-size: 60px;
    color: #ff3e00;
    font-weight: 700;
    letter-spacing: -1px;
  }

  .img-content {
    margin-left: 100px;
  }
</style>

<div class="introduction-container">
  <div class="introduction-text">
    <div class="title">Form idea to Realization</div>
    <p>
      Visit the
      <a href="https://svelte.dev/tutorial">Svelte tutorial</a>
      to learn how to build Svelte apps.
    </p>
    <Button title="Lebih lanjut" buttonWidth="220" />
  </div>
  <div class="img-content">
    <img src="img/day_off.svg" alt="img introduction" style="width:600px" />
  </div>
</div>
