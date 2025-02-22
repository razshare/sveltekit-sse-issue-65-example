<script>
	import { source } from 'sveltekit-sse';

	const connection = source('/events');
	const stats = connection.select('message').json();
</script>

<main>
	<h2>Admin dashboard page</h2>

	<pre>{JSON.stringify($stats)}</pre>
</main>
