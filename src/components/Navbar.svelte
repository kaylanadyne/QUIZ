<script>
    import '../app.scss';
    export let showBeranda = true; 
    export let showRiwayat = true;
</script>

<nav class="navbar navbar-expand-lg navbar-light bg-light border-bottom">
    <div class="container">
        <img src="../images/logo.png" width="100" alt="">
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation"><span class="navbar-toggler-icon"></span></button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <div class="pages ms-3">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    {#if showBeranda}
                        <li class="nav-item">
                        <a class="nav-link active" href="/home">Beranda</a>
                        </li>
                    {/if}
                    {#if showRiwayat}
                        <li class="nav-item">
                            <a class="nav-link" href="/history">Riwayat</a>
                        </li>
                    {/if}
                </ul>
            </div>
            <ul class="navbar-nav ms-auto mt-2 mt-lg-0">
                <a class="nav-link" href="/profile">
                    <img src="../images/profile.jpg" class="rounded-circle" width="40" height="40" alt="">
                </a>    
            </ul>
        </div>
    </div>
</nav>