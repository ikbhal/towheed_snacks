<script>
import SnackNoRequestCheck from "./SnackNoRequestCheck.svelte";
import SnackNoRequestCheckList from "./SnackNoRequestCheckList.svelte";
import Wallete from "./Wallete.svelte";

</script>

<main>
	<h1>Snacks Towheed Accountability</h1>
	<Wallete/>
<!-- <SnackNoRequestCheck/> -->
	<SnackNoRequestCheckList/>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
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