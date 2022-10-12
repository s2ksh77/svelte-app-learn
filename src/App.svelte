<script>
  export let name;
  export let age = 85;
  const assign = () => {
    name = 'Heorpy';
    age = 36;
  };
</script>

<main>
  <h1>Hello {name}!</h1>
  <h2 class={age < 85 ? 'active' : ''}>{age}</h2>
  <p>
    Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build
    Svelte apps.
  </p>
  <img src="" alt={name} />
  <input type="text" bind:value={name} />
  <button on:click={assign}> Assign </button>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  .active {
    color: blue;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
