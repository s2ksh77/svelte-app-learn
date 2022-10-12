<script>
  import { storeName } from './store.js';
  import Parent from './Parent.svelte';
  let name = 'world';
  console.log(storeName); // 객체, set, subscribe, update
  console.log($storeName); // 값을 확인 하는것 auto subscription
  $storeName = name;
</script>

<main>
  <h1>Hello {name}</h1>
  <Parent />
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
