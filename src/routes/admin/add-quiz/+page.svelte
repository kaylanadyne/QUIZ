<script>
    import AdminNavbar from "/src/components/AdminNavbar.svelte";
    export let showPublished = false;
    export let showDraft = false;
    export let showReports = false;
    import AddQuiz from "/src/components/AddQuiz.svelte";
</script>

<AdminNavbar {showPublished} {showDraft} {showReports} />
<AddQuiz />