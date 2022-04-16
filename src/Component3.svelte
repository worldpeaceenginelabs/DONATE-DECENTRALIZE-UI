<script>
	// Enter your apps name
	//let appname = "(Your App's Name)";
	// export var appname;
	import {getContext} from "svelte"
	let appname1 = getContext("name");


	
</script>

<div align="center">
	<input>
	<button>Drop tracker URL</button>
	<p>Thank you so much for supporting us.<br><br>
	With your tracker donation, you are supporting the whole community of {JSON.stringify(appname1)} users actively.<br>
</p>
</div>



