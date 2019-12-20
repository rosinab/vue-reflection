<template>
      <div class="main">
        <div class="cbox">
            <h1>Photo Prompt Generator</h1>
            <p class="subtext">This generator will come up with a random photo of a location from LoremFlickr. Use it as inspiration of where to start your story!</p>
            <br>
            <img :src="prompt.file"/>
            <br>
            <br>
            <p class="refresh">Don't like what you've got? Refresh the page and try something new!</p>
            <!-- <nuxt-link to="/character" class="refresh">Try Again</nuxt-link> -->
            </div>
    </div>
</template>

<script>
import axios from "axios";
export default {
      asyncData ({ params }) {
    return axios.get('https://loremflickr.com/json/600/540/outside')
      .then((res) => {
        return { prompt: res.data }
      })
  },

    head() {
        return {
            title: "Prompt Generator",
            meta: [ 
            {
                hid: "description",
                name: "description",
                content: "Prompt Generator"
            },
            {
                hid: "keywords",
                name: "keywords",
                content: "writing prompts, prompts, generator, prompts generator, writing tool, writing, roleplaying"
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