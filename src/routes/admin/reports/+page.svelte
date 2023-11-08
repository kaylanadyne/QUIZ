<script>
    import AdminNavbar from "/src/components/AdminNavbar.svelte";

    function redirectToDetailPage(subject) {
        // Gantilah URL_TARGET dengan URL halaman detail yang sesuai
        const URL_TARGET = `/detail/${subject}`;
        window.location.href = '/admin/reports/detail';

    }
</script>

<AdminNavbar />

<div class="container">
    <div id="content" class="p-4 p-md-5 pt-5">
        <h2 class="mb-4">Laporan</h2>
        <div class="table-responsive text-center">
            <table class="table">
                <thead>
                    <tr>
                        <th scope="col">Nama kuis</th>
                        <th scope="col">Jumlah peserta</th>
                    </tr>
                </thead>
                <tbody>
                    <tr class="participant" data-sveltekit-preload-data="tap" href="/admin/reports/detail">
                        <td>Matematika</td>
                        <td>100</td>
                    </tr>
                    <tr class="participant" onclick={() => redirectToDetailPage('Sejarah')}>
                        <td>Sejarah</td>
                        <td>2</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
</div>