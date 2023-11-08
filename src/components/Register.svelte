<script>
	import '../app.scss';
	import { navigate } from 'svelte-routing';

	let showAdditionalForm = false;
	let showClassForm = false;
	let showSuccessAlert = false;

	let userData = {
		name: '',
		email: '',
		password: '',
		gender: '',
		education: '',
		department: '',
		class: ''
	};

	function showForm() {
		const selectPref1 = document.getElementById('inlineFormSelectPref1');
		const selectedValue = selectPref1.value;

		showClassForm =
			selectedValue === 'sd' ||
			selectedValue === 'smp' ||
			selectedValue === 'sma' ||
			selectedValue === 'smk';
		showAdditionalForm =
			selectedValue === 'diploma' ||
			selectedValue === 'sarjana' ||
			selectedValue === 'magister' ||
			selectedValue === 'doktor';
	}

	function register() {
		// Simpan data pengguna ke server atau penyimpanan data
		// Di sini Anda dapat menggunakan fetch atau koneksi API lainnya

		// Misalnya, kita akan menggunakan console.log untuk menunjukkan data yang disimpan
		console.log('Data Pendaftaran:', userData);

		// Setelah registrasi berhasil, tampilkan alert
		showSuccessAlert = true;

		// Setelah 5 detik, atur showSuccessAlert kembali ke false
		setTimeout(() => {
			showSuccessAlert = false;
		}, 5000);

		// Navigasi ke halaman login setelah registrasi berhasil
		navigate('/login');
	}
</script>

<div class="container mt-5">
	<div class="row justify-content-center">
		<div class="col-md-6">
			<div class="title">
				<img src="images/kuning.png" alt=""	width="45" style="margin-left: 50vh; margin-top: 8vh;"/>
				<h2 class="text-center mb-4"><strong>Register</strong></h2>
				{#if showSuccessAlert}
					<div class="alert alert-success mt-3" role="alert">
						Registrasi berhasil! Silakan login.
					</div>
				{/if}
			</div>
			<form class="row g-3">
				<div class="col-md-6">
					<label for="name" class="form-label" />
					<input type="text" class="form-control" id="name" placeholder="Nama lengkap" />
				</div>
				<div class="col-md-6">
					<label for="exampleInputEmail1" class="form-label" />
					<input type="email"	class="form-control"	id="exampleInputEmail1"	placeholder="Alamat email"
					/>
				</div>
				<div class="col-md-6 mb-4">
					<label for="username" class="form-label" />
					<input type="text" class="form-control" id="username" placeholder="Nama pengguna" />
				</div>
				<div class="col-md-6">
					<label for="floatingPassword" />
					<input type="password" class="form-control" id="floatingPassword" placeholder="Password"
					/>
				</div>
				<div class="col-md-6 mb-4">
					<label class="visually-hidden" for="inlineFormSelectPref">Preference</label>
					<select class="form-select" id="inlineFormSelectPref">
						<option selected hidden disabled>Jenis kelamin</option>
						<option value="p">Perempuan</option>
						<option value="l">Laki - laki</option>
					</select>
				</div>

				<div class="col-md-6">
					<label class="visually-hidden" for="inlineFormSelectPref1">Preference</label>
					<select class="form-select" id="inlineFormSelectPref1" on:change={showForm}>
						<option selected hidden disabled>Pendidikan terakhir</option>
						<option value="sd">SD/sederajat</option>
						<option value="smp">SMP/sederajat</option>
						<option value="sma">SMA/sederajat</option>
						<option value="smk">SMK/sederajat</option>
						<option value="diploma">Diploma</option>
						<option value="sarjana">Sarjana</option>
						<option value="magister">Magister</option>
						<option value="doktor">Doktor</option>
					</select>
				</div>
				<!-- hidden -->
				<div class="col-md-6" id="additionalForm" style={showAdditionalForm ? 'display: block;' : 'display: none;'}>
					<label class="visually-hidden" for="inlineFormSelectPref2">Preference</label>
					<select class="form-select" id="inlineFormSelectPref2">
						<option selected hidden disabled>Jurusan</option>
						<option value="seni">Seni & Desain</option>
						<option value="komputer">Komputer & Informatika</option>
						<option value="kedokteran">Kedokteran</option>
						<option value="bisnis">Bisnis</option>
						<option value="pariwisata">Pariwisata</option>
					</select>
				</div>

				<div class="col-md-6" id="additionalForm1" style={showClassForm ? 'display: block;' : 'display: none;'}>
					<label class="visually-hidden" for="inlineFormSelectPref3">Preference</label>
					<select class="form-select" id="inlineFormSelectPref3">
						<option selected>Kelas</option>
						<option value="1">1</option>
						<option value="2">2</option>
						<option value="3">3</option>
						<option value="4">4</option>
						<option value="5">5</option>
						<option value="6">6</option>
						<option value="7">7</option>
						<option value="8">8</option>
						<option value="9">9</option>
						<option value="10">10</option>
						<option value="11">11</option>
						<option value="12">12</option>
					</select>
				</div>
				<!-- end hidden -->

				<div class="col-12 text-center mt-5">
					<a href="/login" class="btn shadow" style="background-color: #6096B4; color: #fff; border-radius: 5px;">Daftar</a>
				</div>
			</form>
		</div>
	</div>
	<div class="text-center mt-3">
		<p style="font-size: 15px;">Sudah punya akun? <strong><a href="/login" style="text-decoration: none; color: black;">Masuk</a></strong>
		</p>
	</div>
	<div class="row">
		<div class="col-3 d-none d-sm-block">
			<img src="images/left.jpg" width="300" alt="" class="position-absolute bottom-0 start-0 mb-5 ms-5"/>
		</div>
		<div class="col-3 d-none d-sm-block">
			<img src="images/right.jpg" width="220" alt="" class="position-absolute bottom-0 end-0 mb-5 me-5"/>
		</div>
	</div>
</div>

<style>
	img {
		z-index: -1;
	}
</style>