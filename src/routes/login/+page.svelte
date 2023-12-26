<script>
    import { Button, Label, Input } from 'flowbite-svelte';
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
    <body>
        <h1>Login</h1>
        <form action="?/login" method="POST">
            <label for="email"> Email </labe>
            <input type="text" name="email" required placeholder="name@flowbite.com" />

            <Label for="password"> Password </Label>
            <Input type="password" name="password" required placeholder="R$N2KQ8eU83%X*UqZBn*" />
            
            <Button type="submit">Login</Button>
        </form>
    </body>
</main>
