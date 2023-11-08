<script>
    let selectedOptions = [];

    function handleOptionChange(event) {
    const optionValue = event.target.value;

    if (selectedOptions.includes(optionValue)) {
        // Hapus jika sudah dipilih
        selectedOptions = selectedOptions.filter(option => option !== optionValue);
    } else {
        // Tambahkan jika belum dipilih
        selectedOptions = [...selectedOptions, optionValue];
    }
    }
  </script>
  
  <style>
    /* Gaya CSS tambahan di sini jika diperlukan */
  </style>
  
  <div class="container">
    <form class="mt-2 mb-2">
        <label>
            <input type="checkbox" bind:group={selectedOptions} value="option1">
            Opsi 1
          </label>
    </form>
    <form class="mt-2 mb-2">
        <label>
            <input type="checkbox" bind:group={selectedOptions} value="option2">
            Opsi 2
          </label>
    </form>
    <form class="mt-2 mb-2">
        <label>
            <input type="checkbox" bind:group={selectedOptions} value="option3">
            Opsi 3
          </label>
    </form>
    <form class="mt-2 mb-2">
        <label>
            <input type="checkbox" bind:group={selectedOptions} value="option4">
            Opsi 4
          </label>
    </form>
  </div>
  
  
  