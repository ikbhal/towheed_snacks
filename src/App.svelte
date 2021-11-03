<script>
import {Router, Route, Link} from 'svelte-navigator';
import SnackNoRequestCheck from "./SnackNoRequestCheck.svelte";
import SnackNoRequestCheckList from "./SnackNoRequestCheckList.svelte";
import Wallete from "./Wallete.svelte";

</script>
<Router>

	<head>
		<h1>Snacks Towheed Accountability</h1>

		<nav>
			<Link to="/">Home</Link>
			<Link to="/wallet">Wallet</Link>
			<Link to="/checklist">Check list</Link>
		</nav>
	</head>
	<main>
		<Route path="/wallet">
			<Wallete/>
		</Route>
		<Route path="/checklist">
			<SnackNoRequestCheckList/>
		</Route>
	</main>

</Router>

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