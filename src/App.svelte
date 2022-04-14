<script>
	import Modal from './Modal.svelte'
	import Component1 from './Component1.svelte'
	import Component2 from './Component2.svelte'
	import Component3 from './Component3.svelte'

	// initialise modal state and content
	let showModal = false;
	let modalContent;
	
	// pass in component as parameter and toggle modal state
	function toggleModal(component) {
		modalContent = component;
		showModal = !showModal;
	}
		// Enter your apps name
		let appname = "(Your App's Name)";
	// Enter your button texts
	let button1 = "Donate Decentralize";
	let button2 = "Selfhost Decentralize";
	let button3 = "Drop Support URL"
</script>



<div class="container">
<strong class="font">Do you love {appname}? Donate a P2P tracker to make sure {appname} keeps running! For free or for 7$ monthly! Your donation goes 100% were it belongs to... </strong>
<button on:click={() => (toggleModal(Component1))}>
	{button1}
</button>
<button on:click={() => (toggleModal(Component2))}>
	{button2}
</button>
<button on:click={() => (toggleModal(Component3))}>
	{button3}
</button>
</div>

{#if showModal}
	<Modal on:click={toggleModal} {modalContent} />
{/if}

<style>
	/* The content inside the modal can be styled as usual	 */
	.font {
          padding: 0;
          margin: 0;
          font-family: "Libre Franklin", -apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Oxygen,
            Ubuntu, Cantarell, Fira Sans, Droid Sans, Helvetica Neue, sans-serif;
        }
        * {
          -webkit-font-smoothing: antialiased;
          -moz-osx-font-smoothing: grayscale;
          box-sizing: border-box;
        }
		.container {text-align: right ; background-color: lightgrey;}
</style>