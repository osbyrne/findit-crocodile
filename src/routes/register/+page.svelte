<script lang="ts">
	import { Card, Button, Label, Input, Checkbox } from 'flowbite-svelte';
</script>

<main>
	<div class="flex items-center justify-center min-h-screen mr-4 ml-4">
		<Card class="w-full max-w-md">
			<form class="flex flex-col space-y-6" action="?/register" method="POST">
			<h3 class="text-xl font-medium text-gray-900 dark:text-white">Create an account</h3>
			<Label class="space-y-2">
				<span>Email</span>
				<Input type="email" name="email" placeholder="johndoe@email.com" required />
			</Label>
			<Label class="space-y-2">
				<span>Password</span>
				<Input type="password" name="password" placeholder="••••••••" required />
			</Label>
			<Button type="submit" class="w-full">Register</Button>
			<div class="text-sm text-center font-medium text-gray-500 dark:text-gray-300">
				Already have an account? <a href="/login" class="text-primary-700 hover:underline dark:text-primary-500">Login</a>
			</div>
			</form>
		</Card>
	</div>
</main>
