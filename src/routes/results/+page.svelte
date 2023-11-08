<script>
    import Navbar from "/src/components/Navbar.svelte";
    let showBeranda = false;
    let showRiwayat = false;
    import CardScore from '/src/components/CardScore.svelte';
</script>

<Navbar {showRiwayat} {showBeranda} />
<CardScore
    username="John Doe"
    subject="Physics"
    elapsedTime="00.10.45 dari 01.30.00"
    date="December 5, 2023"
    correctCount={15}
    incorrectCount={3}
/>