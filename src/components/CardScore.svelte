<script>
    export let username = "Nama pengguna";
    export let subject = "Matematika";
    export let elapsedTime = "00.15.23 dari 02.00.00";
    export let date = "november 11, 2023";
    export let correctCount = 0;
    export let incorrectCount = 0;
  </script>
  
  <section class="p-5 p-md-5 text-center text-lg-start shadow-1-strong rounded" style="background-color: #6096B4; height: 706px;">
    <div class="container">
      <nav aria-label="breadcrumb">
        <ol class="breadcrumb">
          <li class="breadcrumb-item"><a href="/home">Home</a></li>
          <li class="breadcrumb-item active" aria-current="page">Profil</li>
        </ol>
      </nav>
      <div class="row d-flex justify-content-center align-items-center">
        <div class="col-md-6">
          <div class="card text-center">
            <div class="card-body m-3 align-items-center">
              <div class="row">
                <div class="col-lg-4 d-flex justify-content-center align-items-centr mb-4 mb-lg-0">
                  <img src="https://mdbcdn.b-cdn.net/img/Photos/Avatars/img%20%2810%29.webp"
                    class="rounded-circle img-fluid shadow-1" alt="woman avatar" width="100" height="100" />
                </div>
                <div class="col-lg-8">
                  <p class="fw-bold lead mb-2"><strong>{username}</strong></p>
                  <p class="fw-bold text-muted mb-0">{subject}</p>
                </div>
              </div>
              <div class="row mt-5 time">
                <div class="col-5">
                  <h5>{elapsedTime}</h5>
                </div>
                <div class="col-2"></div>
                <div class="col-5">
                  <h5>{date}</h5>
                </div>
              </div>
              <div class="row mt-3 score">
                <div class="col-md-6 mb-4">
                  <div class="card text-center" style="height: 55px; background-color: #60B478;">
                    <div class="card-body">
                      <h5 class="card-title text-white">Benar: {correctCount}</h5>
                    </div>
                  </div>
                </div>
                <div class="col-md-6 mb-4">
                  <div class="card text-center" style="height: 55px; background-color: #E53F3F;">
                    <div class="card-body">
                      <h5 class="card-title text-white">Salah: {incorrectCount}</h5>
                    </div>
                  </div>
                </div>
              </div>
              <button type="button" class="btn" style="background-color: #6096B4; color: #fff;">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                  class="bi bi-arrow-clockwise" viewBox="0 0 16 16">
                  <path fill-rule="evenodd" d="M8 3a5 5 0 1 0 4.546 2.914.5.5 0 0 1 .908-.417A6 6 0 1 1 8 2v1z" />
                  <path d="M8 4.466V.534a.25.25 0 0 1 .41-.192l2.36 1.966c.12.1.12.284 0 .384L8.41 4.658A.25.25 0 0 1 8 4.466z" />
                </svg>
                Ulangi kuis
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  
<style>
    nav {
        color: white;
    }
</style>