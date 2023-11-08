<script>
    import '../app.scss';
    export let showPublished = true;
    export let showDraft = true;
    export let showProfile = true;
    export let showReports =true;
    import Modal from '/src/components/Modal.svelte';
    let showModal = false;
    function handleKeyDown(event) {
        if (event.key === "Enter") {
            showModal = true;
        }
    }
</script>

<nav class="navbar navbar-expand-lg navbar-light bg-light border-bottom">
  <div class="container">
      <img src="../images/logo.png" width="100" alt="">
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation"><span class="navbar-toggler-icon"></span></button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <div class="pages ms-3">
              <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                  {#if showPublished}
                      <li class="nav-item">
                        <a class="nav-link active" href="/admin">Diterbitkan</a>
                      </li>
                  {/if}
                  {#if showDraft}
                      <li class="nav-item">
                          <a class="nav-link active" href="/admin/draft">Draft</a>
                      </li>
                  {/if}
                  {#if showReports}
                      <li class="nav-item">
                          <a class="nav-link active" href="/admin/reports">Laporan</a>
                      </li>
                  {/if}
              </ul>
          </div>
          {#if showProfile}
          <ul class="navbar-nav ms-auto mt-2 mt-lg-0">
            <img src="../images/profile.jpg" class="rounded-circle" width="40" height="40" alt="">
            <button class="btn rounded-pill text-danger" tabindex="0" on:click={() => (showModal = true)} on:keydown={handleKeyDown}><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-box-arrow-right" viewBox="0 0 16 16">
                <path fill-rule="evenodd" d="M10 12.5a.5.5 0 0 1-.5.5h-8a.5.5 0 0 1-.5-.5v-9a.5.5 0 0 1 .5-.5h8a.5.5 0 0 1 .5.5v2a.5.5 0 0 0 1 0v-2A1.5 1.5 0 0 0 9.5 2h-8A1.5 1.5 0 0 0 0 3.5v9A1.5 1.5 0 0 0 1.5 14h8a1.5 1.5 0 0 0 1.5-1.5v-2a.5.5 0 0 0-1 0v2z"/>
                <path fill-rule="evenodd" d="M15.854 8.354a.5.5 0 0 0 0-.708l-3-3a.5.5 0 0 0-.708.708L14.293 7.5H5.5a.5.5 0 0 0 0 1h8.793l-2.147 2.146a.5.5 0 0 0 .708.708l3-3z"/>
            </svg></button>
          </ul>
          {/if}
      </div>
  </div>
</nav>

<Modal bind:showModal>
	<h3 slot="header">Keluar</h3>
    <h6>Yakin akan keluar?</h6>
    <a slot="button" href="/" class="btn btn-danger text-white">Keluar</a>
</Modal>