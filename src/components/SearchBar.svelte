<script>
    let searchQuery = "";
  
    function handleSearch() {
      console.log("Search query:", searchQuery);
    }
  </script>
  
  <style>
    form  {
        width: 50vh;
    }
  </style>
  
  <div class="container">
    <div class="image d-flex justify-content-center mt-5">
      <img src="images/home.png" width="300" alt="">
    </div>
    <div class="container search-container mt-3">
      <form class="search-form mx-auto" on:submit|preventDefault={handleSearch}>
        <div class="input-group">
          <input class="form-control border rounded-pill" type="search" placeholder="search" bind:value={searchQuery} id="search-input"/>
        </div>
      </form>
    </div>
  </div>
  