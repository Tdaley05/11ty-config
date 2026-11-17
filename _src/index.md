---
title: Home
layout: base.njk
---
# Welcome to my site!
11ty site - plan to update a lot over Fall Break!

Click on "guide" below to take a look at my tech issue resource guide on physical media and digital ownership!



(Also feel free to use the counter here while I have it up just for fun!)
<is-land on:visible>

  <div id="counter" v-scope="{ count: 0 }">
    <p>Count: <span v-text="count"></span></p>
    <button @click="count++">Add one</button>
  </div>

  <template data-island>
    <script type="module">
      import { createApp } from './js/petite-vue.js'
      createApp().mount('#counter')
    </script>
  </template>

</is-land>