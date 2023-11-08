<!-- MyForm.svelte -->
<script>
    let formData = {
      inputName: "John Doe",
      inputEmail: "john.doe@example.com",
      inputUsername: "johndoe",
      inputAlamat: "123 Main Street, Cityville",
      inputJabatan: "Guru",
    };
  
    function handleSubmit() {
      console.log("Form data:", formData);
    }
  </script>
  
  <style>
    .btn {
        color: white;
    }
  </style>
  
  <form on:submit|preventDefault={handleSubmit}>
    <div class="form-group row mt-4">
      <label for="inputName" class="col-sm-2 col-form-label">Nama</label>
      <div class="col-sm-10">
        <input type="text" class="form-control" id="inputName" bind:value={formData.inputName}>
      </div>
    </div>
    <div class="form-group row mt-3">
      <label for="inputEmail" class="col-sm-2 col-form-label">Email</label>
      <div class="col-sm-10">
        <input type="email" class="form-control" id="inputEmail" bind:value={formData.inputEmail}>
      </div>
    </div>
    <div class="form-group row mt-3">
      <label for="inputUsername" class="col-sm-2 col-form-label">Nama pengguna</label>
      <div class="col-sm-10">
        <input type="text" class="form-control" id="inputUsername" bind:value={formData.inputUsername}>
      </div>
    </div>
    <div class="form-group row mt-3">
      <label for="inputAlamat" class="col-sm-2 col-form-label">Alamat</label>
      <div class="col-sm-10">
        <input type="text" class="form-control" id="inputAlamat" bind:value={formData.inputAlamat}>
      </div>
    </div>
    <div class="mb-3 row mt-4">
      <label for="inputJabatan" class="col-sm-2 col-form-label">Jabatan</label>
      <div class="col-sm-10">
        <input type="text" class="form-control" id="inputJabatan" bind:value={formData.inputJabatan}>
      </div>
    </div>
    <button type="submit" class="btn btn-success rounded-pill">Edit</button>
    <button type="submit" class="btn rounded-pill text-danger">Logout</button>
    
  </form>
  