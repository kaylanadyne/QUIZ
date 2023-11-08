<script>
     import '../app.scss'

    let selected = '';
    let customAmount = '';

    function onChange(event) {
        selected = parseInt(event.target.value);
        console.log('Selected:', selected);
    }

    function onCustomInputChange(event) {
        customAmount = event.target.value;
        console.log('Custom Amount:', customAmount);
    }
</script>

<div class="container mt-5">
    <nav aria-label="breadcrumb">
        <ol class="breadcrumb">
            <li class="breadcrumb-item"><a href="/admin">Home</a></li>
            <li class="breadcrumb-item active" aria-current="page">Tambah kuis</li>
        </ol>
    </nav>
    <div class="card card-question w-75 w-md-50 p-4 mx-auto mt-4">
        <h4 class="mb-4 py-4 px-3 px-md-5">Tambah Kuis</h4>

        <div class="row px-3 px-md-5">
            <div class="col-md-6 mb-3">
                <div class="form-floating">
                    <input type="text" class="form-control" name="formId1" id="formId1" placeholder="">
                    <label for="formId1">Nama kuis</label>
                </div>
            </div>
            <div class="col-md-3 mb-3">
                <div class="form-floating">
                    <input type="number" class="form-control" name="formId2" id="formId2" placeholder="">
                    <label for="formId2">Nilai minimal</label>
                </div>
            </div>
            <div class="col-md-3 mb-3">
                <div class="form-floating">
                    <input type="text" class="form-control" name="formId3" id="formId3" placeholder="">
                    <label for="formId3">Durasi pengerjaan</label>
                </div>
            </div>
        </div>

        <h4 class="py-3 px-3 px-md-5">Pertanyaan</h4>
        <div class="container">
            <div id="question-container">
                <div class="card mx-5 mb-3">
                    <div class="card-body">
                        <div class="row">
                            <div class="col-md-8 mb-3">
                                <div class="form-floating">
                                    <textarea class="form-control" placeholder="" id="floatingTextarea"></textarea>
                                    <label for="floatingTextarea">Pertanyaan</label>
                                </div>
                            </div>
                            <div class="col-md-2 mb-3">
                                <select class="form-select" style="height: 60px;" id="jenisPertanyaan"
                                    aria-label="Default select example">
                                    <option selected hidden disabled>Jenis</option>
                                    <option value="1">Pilihan ganda</option>
                                    <option value="2">Benar atau Salah</option>
                                    <option value="3">Pilih beberapa</option>
                                </select>
                            </div>
                            <div class="col-md-2 mb-3">
                                <div class="form-floating">
                                    <input type="number" class="form-control" name="skor" id="skor"
                                        placeholder="">
                                    <label for="skor">Skor</label>
                                </div>
                            </div>
                        </div>
                        <div class="opsi-container">
                            <form class="mt-2">
                                <label>
                                    <input type="radio" name="amount" value="custom" checked={selected === 'custom'} onchange={onChange} /> 
                                    <input type="text" name="customAmount" value={selected === 'custom' ? customAmount : ''} onchange={onCustomInputChange} />
                                </label>
                            </form>
                            <form class="mt-2">
                                <label>
                                    <input type="radio" name="amount" value="custom" checked={selected === 'custom'} onchange={onChange} />
                                    <input type="text" name="customAmount" value={selected === 'custom' ? customAmount : ''} onchange={onCustomInputChange} />
                                </label>
                            </form>
                            <form class="mt-2">
                                <label>
                                    <input type="radio" name="amount" value="custom" checked={selected === 'custom'} onchange={onChange} /> 
                                    <input type="text" name="customAmount" value={selected === 'custom' ? customAmount : ''} onchange={onCustomInputChange} />
                                </label>
                            </form>
                            <form class="mt-2">
                                <label>
                                    <input type="radio" name="amount" value="custom" checked={selected === 'custom'} onchange={onChange} /> 
                                    <input type="text" name="customAmount" value={selected === 'custom' ? customAmount : ''} onchange={onCustomInputChange} />
                                </label>
                            </form>
                        </div>
                    </div>
                </div>
            </div>
            <button class="btn btn-primary mt-3 mx-5 text-white">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                    class="bi bi-plus-circle" viewBox="0 0 16 16">
                    <path d="M8 15A7 7 0 1 1 8 1a7 7 0 0 1 0 14zm0 1A8 8 0 1 0 8 0a8 8 0 0 0 0 16z" />
                    <path d="M8 4a.5.5 0 0 1 .5.5v3h3a.5.5 0 0 1 0 1h-3v3a.5.5 0 0 1-1 0v-3h-3a.5.5 0 0 1 0-1h3v-3A.5.5 0 0 1 8 4z" />
                </svg>
                &nbsp;Tambah soal
            </button>
        </div>
    </div>
</div>

<style>
    input::-webkit-inner-spin-button {
            -webkit-appearance: none;
    }
</style>