<script>
  let value = 0;

  const count = () => {
    value += 1;
  };
</script>

<button on:click={count}>oyeee {value}</button>
