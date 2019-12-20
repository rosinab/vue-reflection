<template>
 <header>
    <h1><nuxt-link to="/" class="logo">The Character Shop</nuxt-link></h1>

    <nav>
        <ul>
            <li><nuxt-link to="/">Home</nuxt-link></li>
            <li><nuxt-link to="character">Character Generator</nuxt-link></li>
            <li><nuxt-link to="prompt">Prompt Generator</nuxt-link></li>
        </ul>
    </nav>
</header>
</template>

<script>
export default {

}
</script>

<style>
 header {
        background: #313638;
        display: grid;
        grid-template-columns: repeat(2,auto);
    }
    .logo, li a {
        padding: 1em;
        display: block;
        text-transform: uppercase;
        text-decoration: none;
        font-weight: bold;
        color: white;
        font-size: .9em;
    }
    nav {
        justify-self: right;
    }
    ul {
        list-style-type: none;
        margin-top: 1.5em;
        margin-right: 2em;
    }
    li {
        display: inline;
        margin: 0 0.3em;
    }
    li a {
        padding: 1em 1em;
        display: inline-block;
        background: #A32222;
    }

</style>