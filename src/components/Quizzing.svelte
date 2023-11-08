<script>
  import '../app.scss';
  export let questionNumber = 1;
  export let totalQuestions = 7;
  export let timestamp = '09.11.00';

</script>

<div class="container">
  <div class="question-container">
    <div class="information">
      <div class="row">
        <div class="col-3">
          <h5 class="mt-4 fw-semibold text-secondary">{`SOAL ${questionNumber}/${totalQuestions} `}</h5>
        </div>
        <div class="col-9 d-flex justify-content-end">
          <h5 class="mt-4">{timestamp}</h5>
        </div>
      </div>
    </div>
    <div class="alert alert-secondary mt-3" role="alert">
      <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" class="bi bi-exclamation-circle me-2" viewBox="0 0 16 16">
        <path d="M8 15A7 7 0 1 1 8 1a7 7 0 0 1 0 14zm0 1A8 8 0 1 0 8 0a8 8 0 0 0 0 16z"/>
        <path d="M7.002 11a1 1 0 1 1 2 0 1 1 0 0 1-2 0zM7.1 4.995a.905.905 0 1 1 1.8 0l-.35 3.507a.552.552 0 0 1-1.1 0L7.1 4.995z"/>
      </svg>
      Pilih jawaban yang tepat.
    </div>
    <slot></slot>
  </div>
</div>


<style>
  /* Gaya tambahan di sini jika diperlukan */
</style>
