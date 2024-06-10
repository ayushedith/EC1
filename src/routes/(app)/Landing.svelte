<script>
    import { onMount } from "svelte";

    const greetings = ["Hello", "Hey", "Kaise ho", "Greetings", "What's up?", "Yo"];
    let greeting = "Hello";

    onMount(() => {
        greeting = greetings[Math.floor(Math.random() * greetings.length)];
    });
</script>

<article>
    <h1>
        {greeting}, my name is <b>Ayush</b>.
    </h1>
    <p>
        I'm a UI/Backend software engineer who specializes in asynchronous Python/JavaScript
        code.
    </p>
</article>

<style>
    article {
        display: flex;
        flex-direction: column;
        justify-content: end;
        margin: 20rem 2.5rem;
        min-height: calc(100vh - 40rem);
    }

    h1 {
        font-weight: normal;
    }

    p {
        margin: 0;
        font-size: var(--font-size-4);
    }

    @media (min-width: 64rem) {
        article {
            margin: 20rem 10rem;
        }
    }
</style>
