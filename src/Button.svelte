<script>
  function handleClick() {
    console.log('yo!');
  }
</script>

<button on:click={handleClick} type="button">
	<slot>
		No label
	</slot>
</button>

<style>
	button {
    --color: #333;
    position: relative;
		display: inline-block;
		width: 100%;
    padding: .5em;
    border: 3px solid;
    font-size: 1.25em;
    font-weight: bold;
    color: var(--color);
	}
  button::before {
    content: '';
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    z-index: -1;
    background-color: #999;
    opacity: 0;
    transition: opacity .1s;
  }
  button:hover::before,
  button:focus::before {
    opacity: 1;
  }
  button + button {
    margin-top: .5em;
  }
</style>
