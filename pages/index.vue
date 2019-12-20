<template>
  <div class="container">
    <div class="innercon">
      <h1 class="title">Welcome to the Character Shop</h1>
      <h2 class="minititle">Your One Stop Shop For Writing Ideas</h2>
    </div>
    <div class="boxcontainer">
      <div class="test">
        <p>Here at The Character Shop we offer a couple of generators to help out writers who are a little low on ideas. We provide character and prompt generators that you can use to your heart's content.</p>
      </div> 
    </div>
    <div class="linkcontainer">
        <div class="box">
          <nuxt-link to="character" class="link">
            <p class="star">★</p>
            <p>Character Generator</p></nuxt-link>
        </div>
        <div class="box">
          <nuxt-link to="prompt" class="link"> 
            <p class="star">★</p>
            <p>Prompt<br>Generator</p></nuxt-link>
        </div>
      </div>
  </div>
</template>

<script>

export default {
  head() {
    return {
      title: "The Character Shop",
      meta: [ 
      {
        hid: "description",
        name: "description",
        content: "Character and Prompt Generator"
      },
      {
        hid: "keywords",
        name: "keywords",
        content: "generator, writing tool, writing, roleplaying, character, prompt"
      }
      ]
    }
  }
}
</script>

<style>

body {
  text-align: center;
}

.container {
  display: flex;
  flex-direction: column;
}

.linkcontainer {
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.title {
  margin: 2rem 0 0 -1.5rem;
  color: #A32222;
}

.minititle {
  color: #005C69;
}

.forcolumns {
  display: flex;
  flex-direction: column;
}

.boxcontainer {
  display: flex;
  justify-content: center;
}

.test {
    background: #A9ACA9;
    color: white;
    width: 50%;
    margin-top: 2rem;
    padding: 1rem;
    font-size: 1.2rem;
    text-align: center;
}

.box {
  width: 22%;
  background: #005C69;
  font-size: 3rem;
  margin: 2rem 3rem;
  padding: 2rem 0;
}

.star {
  font-size: 6rem;
}

.link {
  color: white;
  text-decoration: none;
}

</style>
