<script>
    import { Button, Label, Input } from 'flowbite-svelte';
</script>

<main>
    <body>
        <h1>Login</h1>
        <form action="?/login" method="POST">
            <Label for="email"> Email </Label>
            <Input type="text" name="email" required placeholder="name@flowbite.com" />

            <Label for="password"> Password </Label>
            <Input type="password" name="password" required placeholder="R$N2KQ8eU83%X*UqZBn*" />
            
            <Button type="submit">Login</Button>
        </form>
    </body>
</main>
