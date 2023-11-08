<script>
    import Navbar from "/src/components/Navbar.svelte";
    let showBeranda = false;
    let showRiwayat = false;

    import Quizzing from "/src/components/Quizzing.svelte";
    import MultiAnswer from "/src/components/MultiAnswer.svelte";
    import Buttons from "/src/components/Buttons.svelte";
</script>

<Navbar {showRiwayat} {showBeranda} />
<Quizzing />
<MultiAnswer />
<Buttons />