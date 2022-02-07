<script>
  export let type = "primary"
  export let flat = false
  export let inverse = false
</script>

<button class={type} class:flat class:inverse on:click>
  <slot />
</button>

<style>
  button {
    border: 0;
    cursor: pointer;
    padding: 12px 24px;
    font-weight: bold;
    box-shadow: 1px 2px 3px rgba(0, 0, 0, 0.2);
  }

  .primary {
    background: #9a3fff;
    border: 1px solid #9a3fff;
    color: white;
  }

  .secondary {
    background: #1b6dff;
    border: 1px solid #1b6dff;
    color: white;
  }

  .flat {
    box-shadow: none;
  }

  .inverse {
    background: white;
  }

  .primary.inverse {
    color: #9a3fff;
  }

  .secondary.inverse {
    background: #1b6dff;
  }
</style>
