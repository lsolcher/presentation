<template lang='pug'>
#VueSlideshow
  .eg-slideshow
    slide
      h1 VueJS
      .center.frontpage
        img(src='./assets/logo.png')
      h4
      .center.frontpage
       The Progressive JavaScript Framework

    slide(enter='fadeIn' leave='fadeOut')
      h2 Roadmap
      h3 What
      h3 Why
      h3 How
      //h3 Examples

    slide(enter='fadeIn' leave='fadeOut')
      h3 What
      p.
       JavaScript framework
      //with focus on user interfaces
      p.
       Progressive
      //- Can be plugged in parts of the application
      p.
       Reusable
      // //- Splits up a web page in reusable components
      p.
       Reactive
      p.
       Supports single page applications

    slide(enter='fadeIn' leave='fadeOut')
      h3 Why
      p.
        Very lean and small
      p.
        Easy to use
      p.
        Easy to integrate
      p.
        Many extensions
      p.
        Good documentation


    slide(enter='fadeIn' leave='fadeOut')
      h3 Vue vs React vs Angular
      .center.frontpage
       img(src='./assets/compare.jpg')

    slide(:steps=3 enter='fadeIn' leave='fadeOut')
      h3 Why not?
      p(v-if='step >=2').
        Still widely unknown
      .center.frontpage
        img(v-if='step >=3' src='./assets/compare2.jpg')
      p(v-if='step >=3')
        <a href="https://medium.com/@TechMagic/reactjs-vs-angular5-vs-vue-js-what-to-choose-in-2018-b91e028fa91d">Recent comparison between Vue, React and Angular</a>
      p(v-if='step >=4')
        <a href="https://vuejs.org/v2/guide/comparison.html">Vue's internal comparison with React and Angular</a>

    slide(enter='fadeIn' leave='fadeOut')
      h3 How
      p.
       <a href="https://jsfiddle.net/t6feb4bj/">Hello World!</a>
      p.
       <a href="https://jsfiddle.net/ckt6bs13/1/">Bindings</a>
      p.
       <a href="https://jsfiddle.net/q4nva61z/">Forms</a>
      p.
       <a href="https://jsfiddle.net/argq6n43/7/">Components</a>


    slide(enter='fadeIn' leave='fadeOut')
      h3 Extensions
      p.
        HTTP-Requests: vue-resource
      p.
        Routing: vue-router
      p.
        State management: Vuex
      p.
        <a href="https://github.com/vuejs/awesome-vue#components--libraries">...and many more</a>

    slide(enter='fadeIn' leave='fadeOut')
      h3 Things made with Vue
      p.
       This presentation
      p.
        <a href="http://letsgetlost.travelgram.co/en/">Websites</a>
      p.
        <a href="https://madewithvuejs.com/photon-cms">Frameworks</a>
      p.
        <a href="https://rottensoup.herokuapp.com/?ref=madewithvuejs.com">Games</a>
      p.
        <a href="https://madewithvuejs.com/">Many more</a>

    slide(enter='fadeIn' leave='fadeOut')
      h3 Resources
      p.
        <a href="https://www.udemy.com/vuejs-2-the-complete-guide/learn/v4/">Vue online course</a>
      p.
        <a href="https://docs.google.com/document/d/14tYfJXQH9-ZwTqoJq2gTbGuUzHwzY-EP1mrVI8nGK6A/edit?usp=sharing">learning journal</a>


    slide(enter='fadeIn' leave='fadeOut')
      h3 Thank you!
</template>

<script>
import eagle from 'eagle.js'
export default {
  mixins: [ eagle.slideshow ],
  infos: {
    // These infos appear on the home page, below the slideshow's thumbnail
    title: 'vue-slideshow JS',
    description: 'A boilerplate to get you started',
    path: 'vue-slideshow'
  },
  created () {
    let trends = document.createElement('script')
    trends.setAttribute('src', 'https://ssl.gstatic.com/trends_nrtr/1480_RC02/embed_loader.js')

    document.head.appendChild(trends)
  }
}
</script>

<style lang='scss'>
@import url(https://fonts.googleapis.com/css?family=Raleway);
#VueSlideshow{
  .frontpage {
    img {
      height: 10em;
    }
    img.control-schema {
      width: 8em;
      height: 3em;
    }
  }

  .quarter {
    text-align: center;
    p {
      margin-top: 0;
      text-align: center;
    }
    h4 {
      margin-top: 0;
      margin-bottom: 0
    }
  }

  .eg-slideshow{
    font-family: 'Raleway';
    background-color: #eef;
    .eg-slide{
      .eg-slide-content{
        width: 25em;
        max-width: 80%;
        margin: 0 auto;
      }
    }
  }
  .eg-slide-content{
    width: 25em;
    max-width: 80%;
    margin: 0 auto;
  }
}
</style>
