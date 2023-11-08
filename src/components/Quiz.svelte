<script>
  import '../app.scss';
  import Modal from './Modal.svelte';
  let showModal = false;
  export let title = 'Matematika';
  export let imagePath = '../images/quiz.png';
  export let profilPics = '../images/profile.jpg'
  export let jumlahSoal = 7 ;
  function handleKeyDown(event) {
    if (event.key === "Enter") {
      showModal = true;
    }
  }

</script>

<div class="container">
  <div class="quiz">
    <div class="row justify-content-center">  
      <div class="col-md-4 mt-5 mb-5" role="button" tabindex="0" on:click={() => (showModal = true)} on:keydown={handleKeyDown}>
        <div class="card" style="width: 25rem;">
          <img src={imagePath} class="card-img-top" alt="">
          <div class="card-body">
            <h5 class="card-title">{title}</h5>
          </div>
        </div>
      </div>
      <div class="col-md-4 mt-5 mb-5">
        <div class="card" style="width: 25rem;">
          <img src={imagePath} class="card-img-top" alt="">
          <div class="card-body">
            <h5 class="card-title">{title}</h5>
          </div>
        </div>
      </div>
      <div class="col-md-4 mt-5 mb-5">
        <div class="card" style="width: 25rem;">
          <img src={imagePath} class="card-img-top" alt="">
          <div class="card-body">
            <h5 class="card-title">{title}</h5>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<Modal bind:showModal>
	<h2 slot="header">{title}</h2>
  <img src={imagePath} alt="">
  <h6 class="mt-3 mb-3">Pengerjaan kuis {title}</h6>
  <div class="row">
    <div class="col-10">
      <img src={profilPics} alt="" class="rounded-pill" width="30">
    </div>
    <div class="col-2">
      <p class="text-muted">{jumlahSoal} Soal</p>
    </div>
  </div>
  <a slot="button" href="/multichoice" class="btn btn-success text-white">
    <svg xmlns="http://www.w3.org/2000/svg" width="25" height="25" fill="currentColor" class="bi bi-play-fill" viewBox="0 0 16 16">
        <path d="m11.596 8.697-6.363 3.692c-.54.313-1.233-.066-1.233-.697V4.308c0-.63.692-1.01 1.233-.696l6.363 3.692a.802.802 0 0 1 0 1.393z"/>
    </svg>&nbsp;Mulai
  </a>
</Modal>

<style>

</style>