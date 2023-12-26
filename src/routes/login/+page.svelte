<script lang="ts">
	import { Card, Button, Label, Input, Checkbox } from 'flowbite-svelte';
</script>

<style>
    h1 {
        text-align: center;
    }
    form {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    form > * {
        margin: 10px;
    }
    body {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        margin: auto;
    }
</style>

<main>
	<div class="flex items-center justify-center min-h-screen mr-4 ml-4">
		<Card class="w-full max-w-md">
			<form class="flex flex-col space-y-6" action="?/login" method="POST">
			<h3 class="text-xl font-medium text-gray-900 dark:text-white">Login to your account</h3>
			<Label class="space-y-2">
				<span>Email</span>
				<Input type="email" name="email" placeholder="johndoe@email.com" required />
			</Label>
			<Label class="space-y-2">
				<span>Password</span>
				<Input type="password" name="password" placeholder="••••••••" required />
			</Label>
			<!--
			<div class="flex items-start">
				<Checkbox>Remember me</Checkbox>
				<a href="/" class="ms-auto text-sm text-primary-700 hover:underline dark:text-primary-500"> Lost password? </a>
			</div>
			-->
			<Button type="submit" class="w-full">Login</Button>
			<div class="text-sm text-center font-medium text-gray-500 dark:text-gray-300">
				Don't have an account? <a href="/register" class="text-primary-700 hover:underline dark:text-primary-500">Register</a>
			</div>
			</form>
		</Card>
	</div>

</main>
