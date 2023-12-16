<script lang="ts">
	import { enhance, type SubmitFunction } from '$app/forms';
	import { supabaseClient } from '$lib/supabase';
	import type { PageData } from './$types';
	import HeaderLanding from '../components/HeaderLanding.svelte';

	export let data: PageData;

	const submitLogout: SubmitFunction = async ({ cancel }) => {
		const { error } = await supabaseClient.auth.signOut();
		if (error) {
			console.log(error);
		}
		cancel();
	};
</script>

<main>
	<HeaderLanding session={data.session}/>
	{#if data.session}
		<p>Welcome, {data.session.user.email}</p>
		<form action="/logout" method="POST" use:enhance={submitLogout}>
			<button type="submit">Logout</button>
		</form>
	{:else}
		<p>Let's learn how to register and login users!</p>
		<div>
			<a href="/login">Login</a>
			<a href="/register">Register</a>
		</div>
	{/if}
</main>