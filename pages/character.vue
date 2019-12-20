<template>
    <div class="main">
        <div class="cbox">
            <h1>Character Generator</h1>
            <p class="subtext">This generator will come up with a random image, name, age and location that you can use as a start for character creation.</p>
            <br>
            <img :src="character.photo"/>
            <h3>Name</h3>
            <p>{{character.name}} {{character.surname}}</p>
            <h3>Age</h3>
            <p>{{character.age}}</p>
            <h3>Country</h3>
            <p>{{character.region}}</p>
            <br>
            <p class="refresh">Don't like what you've got? Refresh the page and try someone new!</p>
            <!-- <nuxt-link to="/character" class="refresh">Try Again</nuxt-link> -->
            </div>
    </div>
</template>


<script>
import axios from "axios";
export default {
    data() {
        return {
            character: []
        }
    },
    async created() {
        try {
            const res = await axios.get('https://uinames.com/api/?ext');
            this.character = res.data;
        } catch(err) {
            console.log(err)
        }
    },
    head() {
        return {
            title: "Character Generator",
            meta: [ 
            {
                hid: "description",
                name: "description",
                content: "Character Generator"
            },
            {
                hid: "keywords",
                name: "keywords",
                content: "character, generator, character generator, writing tool, writing, roleplaying"
            }
            ]
        }
    }
}
</script>

<style>

.main {
    display: flex;
    justify-content: center;
}

.cbox {
    background: #005C69;
    color: white;
    width: 50%;
    margin-top: 2rem;
    padding: 1rem;
    text-align: center;
}

h1 {
    color: #A9ACA9;
}

.subtext {
    font-size: 1.2rem;
}

.refresh {
    text-decoration: none;
    font-weight: bold;
    background-color: #A32222;
    color: white;
    padding: 0.8em;
    border: white solid 1px;
}

</style>