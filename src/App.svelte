<script>
  import Fruits from './Fruits.svelte';
  let fruits = ['Apple', 'Banana', 'Cherry', 'Orange', 'Mange'];
</script>

<main>
  <Fruits {fruits} />
  <Fruits fruits={[...fruits].reverse()} />
  <Fruits {fruits} reverse />
  <Fruits {fruits} slice="-2" />
  <Fruits {fruits} slice="0, 3" />
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }
  .box {
    width: 300px;
    height: 150px;
    background-color: orange;
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
