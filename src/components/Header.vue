<template>
  <div class="Header">
      <div class="profilePalate">
          <a href="https://github.com/NathanDavisBarrett" title="GitHub">
              <img src="GitHub-Mark-Light-120px-plus.png">
          </a>
          <a href="https://www.linkedin.com/in/nathandavisbarrett/" title="LinkedIn">
              <img src="In-Blue-Logo.png.original.png">
          </a>
          <a href="https://scholar.google.com/citations?user=4KekiOAAAAAJ&hl=en" title="Google Scholar">
              <img src="google-scholar.png">
          </a>
      </div>
      <div class="namePalate">
          <span class="codeName" id="namePython" title="Python">
              <h1 class="extraText">class&#160;</h1>
              <h1 class="actualName">{{myName}}</h1>
              <h1 class="extraText">(</h1>
              <span class="attrList" v-for="(attr, index) in codeNameAttrs" :key="attr">
                  <h1 class="extraText" v-if="index != 0">,&#160;</h1>
                  <h1 class="extraText">{{attr}}</h1>
              </span>
              <h1 class="extraText">): &#9660;</h1>
          </span>
          <span class="codeName" id="nameCpp" title="C++">
              <h1 class="extraText">class&#160;</h1>
              <h1 class="actualName">{{myName}}</h1>
              <h1 class="extraText">():&#160;</h1>
              <span class="attrList" v-for="(attr, index) in codeNameAttrs" :key="attr">
                  <h1 class="extraText" v-if="index != 0">,&#160;</h1>
                  <h1 class="extraText">public {{attr}}</h1>
              </span>
              <h1 class="extraText">&#160;&#123; &hellip; &#125;</h1>
          </span>
          <span class="codeName" id="nameJava" title="Java">
              <h1 class="extraText">class&#160;</h1>
              <h1 class="actualName">{{myName}}</h1>
              <h1 class="extraText">&#160;implements&#160;</h1>
              <span class="attrList" v-for="(attr, index) in codeNameAttrs" :key="attr">
                  <h1 class="extraText" v-if="index != 0">,&#160;</h1>
                  <h1 class="extraText">{{attr}}</h1>
              </span>
              <h1 class="extraText">&#160;&#123; &hellip; &#125;</h1>
          </span>
          <span class="codeName" id="nameHTML" title="HTML, CSS, JavaScript, Vue.js">
              <span class="attrList" v-for="attr in codeNameAttrs" :key="attr">
                  <h1 class="extraText">&lt;{{attr}}&gt;&#160;</h1>
              </span>
              <h1 class="actualName">&lt;{{myName}}&#160;&#47;&gt;&#160;</h1>
              <span class="attrList" v-for="attr in codeNameAttrs" :key="attr">
                  <h1 class="extraText">&lt;&#47;{{attr}}&gt;&#160;</h1>
              </span>
          </span>
          <span class="codeName" id="nameSQL" title="SQL">
              <h1 class="extraText">SELECT&#160;</h1>
              <h1 class="actualName">{{myName}}</h1>
              <h1 class="extraText">&#160;FROM</h1>
              <span class="attrList" v-for="(attr, index) in codeNameAttrs" :key="attr">
                  <h1 class="extraText" v-if="index != 0">&#160;JOIN</h1>
                  <h1 class="extraText">&#160;{{attr}}</h1>
              </span>
          </span>
          <span class="codeName" id="nameVBA" title="VBA">
              <h1 class="extraText">Public&#160;</h1>
              <h1 class="actualName">{{myName}}</h1>
              <h1 class="extraText">&#160;As&#160;</h1>
              <span class="attrList" v-for="(attr, index) in codeNameAttrs" :key="attr">
                  <h1 class="extraText" v-if="index != 0">_</h1>
                  <h1 class="extraText">{{attr}}</h1>
              </span>
              <h1 class="extraText">&#160;&hellip;</h1>
          </span>

      </div>
      <div class="logoContainer">
          <img src="NLogo_New_Transparent.png">
      </div>

      <div class="mainName">
          <h1>Nathan Davis Barrett<span class="blink">_</span></h1>
          <div class="attrFullList">
              <span v-for="(attr, index) in codeNameAttrs" :key="attr">
                  <h2 v-if="index != 0">,&#160;</h2>
                  <h2>{{attr}}</h2>
              </span>
              <span>
                  <h2>,&#160;...</h2>
              </span>
          </div>
      </div>

      <div class="routerLinksContainer">
          <div class="routerLinks">
              <HeaderLink v-bind:linkLocation="'about'" v-bind:displayText="'About'" v-bind:selection="selection" v-on:click="setSelection('about')"/>
              <HeaderLink v-bind:linkLocation="'cv'" v-bind:displayText="'CV'" v-bind:selection="selection" v-on:click="setSelection('cv')"/>
              <HeaderLink v-bind:linkLocation="'research_projects'" v-bind:displayText="'Research Projects'" v-bind:selection="selection" v-on:click="setSelection('research_projects')"/>
              <HeaderLink v-bind:linkLocation="'personal_projects'" v-bind:displayText="'Personal Projects'" v-bind:selection="selection" v-on:click="setSelection('personal_projects')"/>
          </div>
      </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HeaderLink from '@/components/HeaderLink.vue'

export default {
  name: 'Header',
  components: {
      HeaderLink,
  },
  data() {
      return {
          myName: "NathanDavisBarrett",
          codeNameAttrs: ["Engineer", "Developer", "Researcher"],
          selection: "",
      }
  },
  methods: {
      setSelection(newSelection) {
          this.selection = newSelection;
      }
  }
}
</script>

<style>
.Header {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
}

@media only screen and (min-width: 2051px) {
    .Header {
            align-items: center;
    }
}
@media only screen and (max-width: 2050px) {
    .Header {
        align-items: flex-start;
    }
}

.profilePalate {
    width: 100%;
    height: 5vh;
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    align-items: center;
}

.profilePalate a {
    height: 100%;
    padding-left: 10px;
}

.profilePalate img {
    height: 100%;
}

.namePalate {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    -webkit-mask-image: -webkit-gradient(linear, left top, left bottom, from(rgba(0,0,0,1)), to(rgba(0,0,0,0)));
}

.namePalate h1 {
    margin-top: 10px;
    margin-bottom: 10px;
    margin-left: 0;
    margin-right: 0;
}

.codeName {
    display: flex;
    flex-direction: row;
}

@media only screen and (max-width: 800px) {
    .codeName {
        font-size: xx-small;
    }
    .logoContainer {
        height: 115px;
    }
    .logoContainer img {
        width: 250px;
    }
}
@media only screen and (min-width: 801px) {
    .codeName {
        font-size: large;
    }
    .logoContainer {
        height: 165px;
    }
    .logoContainer img {
        width: 370px;
    }
}

.attrList {
    display: flex;
    flex-direction: row;
}

.actualName {
    font-weight: 800;
}

.extraText {
    font-weight: 300;
}

.logoContainer {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;

    text-align: center;

    position: relative;
    width: 100%;
}

.logoContainer img {
    position: absolute;
    bottom: 0;
}

.mainName {
    display: flex;
    flex-direction: column;
    width: 100%;
    justify-content: center;
    align-items: center;
}

.mainName h1 {
    font-size: 7vw;
}

.blink {
    animation: blinker 2s cubic-bezier(0,1.19,0,0.89) infinite;
}

@keyframes blinker {
    0% {
        opacity: 1;
    }
    50% {
        opacity: 0;
    }
    100% {
        opacity: 1;
    }
}

.attrFullList {
    display: flex;
    width: 80%;
    flex-direction: row;
    justify-content: center;
}

.attrFullList span {
    display: flex;
    flex-direction: row;
}

.attrFullList h2 {
    margin: 0px;
}

.routerLinksContainer {
    display: flex;
    width: 100%;
    justify-content: center;
    margin-top: 50px;
    margin-bottom: 50px;
}

.routerLinks {
    display: flex;
    width: 80%;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
}

</style>
