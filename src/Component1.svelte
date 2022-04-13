<script>
	import Modal from './Modal.svelte'
	import App from './App.svelte'
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
</script>

<div>
	<ol>
		<li><button>
			<a
            href="https://heroku.com/deploy?template=https://github.com/draeder/p2p-tracker/tree/master"
            target="_blank"
            rel="noopener noreferrer"
          >Deploy Tracker</a>	
		</button></li>
		<li>Sign up and confirm the registration email (answer the questions with "i dont know" if you like)
			and choose a servername and your own region(you strengthen the connection in your own region, other donators in their region)</li>
		<li><button on:click={() => (toggleModal(Component3))}>
			Drop Support URL
		</button>	 
		</li>
	
	</ol>
</div>

