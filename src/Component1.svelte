<div>
	<ol>
		<li><button>
			<a
            href="https://www.heroku.com/deploy/?template=https://github.com/amark/gun"
            target="_blank"
            rel="noopener noreferrer"
          >Deploy Tracker</a>	
		</button></li><br>
		<li>Sign up (answer the questions with "i dont know" if you don't know) and confirm the registration email. <br><br>
			Also choose a servername and your own region(you strengthen the connection in your own region, other donators in their region)</li>
			<br><li><button on:click={() => (toggleModal(Component3))}>
			Drop Support URL
		</button>	 
		</li>
	
	</ol>
</div>

{#if showModal}
	<Modal on:click={toggleModal} {modalContent} />
{/if}

<script>
	import Modal from './Modal.svelte'
	import Component3 from './Component3.svelte'

	// initialise modal state and content
	let showModal = false;
	let modalContent;
	
	// pass in component as parameter and toggle modal state
	function toggleModal(component) {
		modalContent = component;
		showModal = !showModal;
	}
</script>