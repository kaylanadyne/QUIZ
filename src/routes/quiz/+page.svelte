<script>
    import Navbar from "../src/components/Navbar.svelte";    
    let showBeranda = false;
    let showRiwayat = false;

</script>

<Navbar {showBeranda} {showRiwayat} />
<div class="container mt-5 w-50">
    <div class="quiz">
        <div class="quiz-image">
            <img src="images/quiz.png" alt="" class="mx-auto w-100">
        </div>
        <div class="quiz-title">
            <h2 class="mt-3">Quiz Name</h2>
        </div>
        <div class="start-btn d-flex justify-content-end">
            <a class="btn btn-success text-white rounded-pill" href="/multichoice">Mulai kuis</a>
        </div>
    </div>
</div>
