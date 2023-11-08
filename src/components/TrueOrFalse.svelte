<script>
  let selectedOption = null;

  function handleOptionChange(event) {
    selectedOption = event.target.value;
  }
</script>

<style>
  /* Gaya CSS tambahan di sini jika diperlukan */
</style>

<div class="container">
  <form class="mt-2 mb-2">
    <label>
      <input type="radio" bind:group={selectedOption} value="option1">
      Benar
    </label>
  </form>
  <form class="mt-2 mb-2">
    <label>
      <input type="radio" bind:group={selectedOption} value="option2">
      Salah
    </label>
  </form>
</div>


