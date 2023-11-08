<script>
    import '../app.scss';
  
    let username = '';
    let password = '';
    let showAlert = false;
  
    function login() {
      // Logika autentikasi disini (sesuaikan dengan backend atau logika autentikasi yang Anda miliki)
      // Misalnya, Anda dapat membandingkan email dan password dengan data pengguna yang ada di server.
  
      // Contoh: Username dan password statis
      const validUsername = 'nadin';
      const validPassword = 'nadin123';
  
      if (username === validUsername && password === validPassword) {
      window.location.href = '/home';
        } else {
        showAlert = true;

        setTimeout(() => {
            showAlert = false;
        }, 3000);
        }
    }
  </script>
  
  <style>
  </style>
  
  <div class="container mt-5">
    <div class="row d-flex justify-content-center">
      <div class="col-md-6">
        <img src="images/kuning.png" alt="" width="30" style="margin-left: 50vh; margin-top: 8vh;">
        <h2 class="text-center mb-4"><strong>Login</strong></h2>
        {#if showAlert}
          <div class="alert alert-danger mt-3" role="alert">
            Username atau password tidak sesuai! Coba lagi.
          </div>
        {/if}
        <form on:submit|preventDefault="{login}">
          <div class="col-md-12">
            <label for="exampleInputEmail1" class="form-label"></label>
            <input type="text" bind:value="{username}" class="form-control" id="exampleInputUsername" placeholder="Username">
          </div>
  
          <div class="col-md-12">
            <label for="floatingPassword"></label>
            <input type="password" bind:value="{password}" class="form-control" id="floatingPassword" placeholder="Password">
          </div>
  
          <div class="col-12 text-center mt-5">
            <button type="submit" class="btn shadow" style="background-color: #6096B4; color: #fff; border-radius: 5px;">Masuk</button>
          </div>
        </form>
  
        
      </div>
    </div>
    <div class="text-center mt-3">
      <p style="font-size: 15px;">Belum punya akun? <strong><a href="/register" style="text-decoration: none; color: black;">Daftar</a></strong></p>
    </div>
    <div class="row">
      <div class="col-3 d-none d-sm-block">
        <img src="images/left.jpg" width="300" alt="" class="position-absolute bottom-0 start-0 mb-5 ms-5">
      </div>
      <div class="col-3 d-none d-sm-block">
        <img src="images/right.jpg" width="220" alt="" class="position-absolute bottom-0 end-0 mb-5 me-5">
      </div>
    </div>
  </div>
  