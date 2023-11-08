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
      Opsi 1
    </label>
  </form>
  <form class="mt-2 mb-2">
    <label>
      <input type="radio" bind:group={selectedOption} value="option2">
      Opsi 2
    </label>
  </form>
  <form class="mt-2 mb-2">
    <label>
      <input type="radio" bind:group={selectedOption} value="option3">
      Opsi 3
    </label>
  </form>
  <form class="mt-2 mb-2">
    <label>
      <input type="radio" bind:group={selectedOption} value="option4">
      Opsi 4
    </label>
  </form>
</div>


