<script>
    export let items = [];
    export let activeTabValue = 1;
  
    const handleClick = tabValue => () => (activeTabValue = tabValue);

    const handleKeyDown = (event, tabValue) => {
    if (event.key === 'Enter') {
      activeTabValue = tabValue;
    }
  };
  </script>
  
  
<div class="container">
    <div class="row mt-5">
        <nav aria-label="breadcrumb">
            <ol class="breadcrumb">
                <li class="breadcrumb-item"><a href="/home">Home</a></li>
                <li class="breadcrumb-item active" aria-current="page">Profil</li>
            </ol>
        </nav>
        <div class="col-md-4 mt-5">
            <div class="profile-photo d-flex justify-content-center">
                <img src="images/profile.jpg" width="250" class="rounded-circle" alt="">
            </div>
            <div class="profile-info">
                <h5 class="name mt-3 text-center">Nama</h5>
                <p class="email text-center text-muted">nama@gmail.com</p>
            </div>
        </div>
        <div class="col-md-8">
            <ul role="tablist">
                {#each items as item}
                  <li role="presentation" class={activeTabValue === item.value ? 'active' : ''}>
                    <span
                      role="tab"
                      aria-selected={activeTabValue === item.value}
                      on:click={handleClick(item.value)}
                      on:keydown={e => handleKeyDown(e, item.value)}
                      tabindex="0"> {item.label}
                    </span>
                  </li>
                {/each}
              </ul>
              
              {#each items as item}
                {#if activeTabValue == item.value}
                  <div class="box">
                    <svelte:component this={item.component}/>
                  </div>
                {/if}
              {/each}
        </div>
    </div>
</div>

  
  <style>
    .box {
      margin-bottom: 10px;
      padding: 40px;
      border: 1px solid #dee2e6;
      border-radius: 0 0 .5rem .5rem;
      border-top: 0;
    }
    ul {
      display: flex;
      flex-wrap: wrap;
      padding-left: 0;
      margin-bottom: 0;
      list-style: none;
      border-bottom: 1px solid #dee2e6;
    }
      li {
          margin-bottom: -1px;
      }
  
    span {
      border: 1px solid transparent;
      border-top-left-radius: 0.25rem;
      border-top-right-radius: 0.25rem;
      display: block;
      padding: 0.5rem 1rem;
      cursor: pointer;
    }
  
    span:hover {
      border-color: #e9ecef #e9ecef #dee2e6;
    }
  
    li.active > span {
      color: #495057;
      background-color: #fff;
      border-color: #dee2e6 #dee2e6 #fff;
    }
  </style>