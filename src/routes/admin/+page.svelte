<script>

    import AdminNavbar from "/src/components/AdminNavbar.svelte";
</script>
  

<AdminNavbar />

<div class="container mt-4">
    <h3 class="mb-3">Diterbitkan</h3>
    <a href="admin/add-quiz" class="btn btn-success text-white"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-plus-lg" viewBox="0 0 16 16">
        <path fill-rule="evenodd" d="M8 2a.5.5 0 0 1 .5.5v5h5a.5.5 0 0 1 0 1h-5v5a.5.5 0 0 1-1 0v-5h-5a.5.5 0 0 1 0-1h5v-5A.5.5 0 0 1 8 2Z"/>
    </svg>&nbsp;Tambah soal</a>

    <div class="card mt-3 mb-3 w-50">
        <div class="row no-gutters">
            <div class="col-8">
                <div class="card-body">
                    <h6 class="card-title">KUIS</h6>
                    <h5 class="card-title">Matematika</h5>
                    <p>7 Pertanyaan</p>
                    <div class="info-admin">
                        <div class="row">
                            <div class="col-1">
                                <img src="../images/profile.jpg" width="20" class="rounded-circle"
                                    alt="">
                            </div>
                            <div class="col-7">
                                <p class="card-text"><small class="text-muted">oleh admin</small></p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>