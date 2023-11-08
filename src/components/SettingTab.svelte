<!-- MyProfileForm.svelte -->
<script>
    let formData = {
      inputTelp: "123456789",
      inputGelar: "spd",
      inputTempat: "smk",
      inputStatus: "aktif",
      inputKeahlian: "mancing",
      inputHobi: "mancing",
    };
  
    function handleSubmit() {
      console.log("Form data:", formData);
    }
  </script>
  
  <style>
  </style>

  
  <form on:submit|preventDefault={handleSubmit}>
    <div class="form-group row mt-3">
      <label for="inputTelp" class="col-sm-2 col-form-label">Nomor hp</label>
      <div class="col-sm-10">
        <input type="tel" class="form-control" id="inputTelp" bind:value={formData.inputTelp}>
      </div>
    </div>
    <div class="mb-3 row mt-2">
      <label for="inputGelar" class="col-sm-2 col-form-label">Gelar</label>
      <div class="col-sm-10">
        <input type="text" class="form-control" id="inputGelar" bind:value={formData.inputGelar}>
      </div>
    </div>
    <div class="mb-3 row">
      <label for="inputTempat" class="col-sm-2 col-form-label">Tempat Tugas</label>
      <div class="col-sm-10">
        <input type="text" class="form-control" id="inputTempat" bind:value={formData.inputTempat}>
      </div>
    </div>
    <div class="mb-3 row">
      <label for="inputStatus" class="col-sm-2 col-form-label">Status</label>
      <div class="col-sm-10">
        <input type="text" class="form-control" id="inputStatus" bind:value={formData.inputStatus}>
      </div>
    </div>
    <div class="mb-3 row">
      <label for="inputKeahlian" class="col-sm-2 col-form-label">Keahlian</label>
      <div class="col-sm-10">
        <input type="text" class="form-control" id="inputKeahlian" bind:value={formData.inputKeahlian}>
      </div>
    </div>
    <div class="mb-3 row">
      <label for="inputHobi" class="col-sm-2 col-form-label">Hobi</label>
      <div class="col-sm-10">
        <input type="text" class="form-control" id="inputHobi" bind:value={formData.inputHobi}>
      </div>
    </div>

  </form>
  