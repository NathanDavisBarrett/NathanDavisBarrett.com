<template>
  <div class="Header">
      <div class="namePalate">
          <span class="codeName" id="namePython" title="Python">
              <h1 class="extraText">class&#160;</h1>
              <h1 class="actualName">NathanDavisBarrett</h1>
              <h1 class="extraText">(</h1>
              <span class="attrList" v-for="(attr, index) in codeNameAttrs" :key="attr">
                  <h1 class="extraText" v-if="index != 0">,&#160;</h1>
                  <h1 class="extraText">{{attr}}</h1>
              </span>
              <h1 class="extraText">): &#9660;</h1>
          </span>
          <span class="codeName" id="nameCpp" title="C++">
              <h1 class="extraText">class&#160;</h1>
              <h1 class="actualName">NathanDavisBarrett</h1>
              <h1 class="extraText">():&#160;</h1>
              <span class="attrList" v-for="(attr, index) in codeNameAttrs" :key="attr">
                  <h1 class="extraText" v-if="index != 0">,&#160;</h1>
                  <h1 class="extraText">public {{attr}}</h1>
              </span>
              <h1 class="extraText">&#160;&#123; &hellip; &#125;</h1>
          </span>
          <span class="codeName" id="nameJava" title="Java">
              <h1 class="extraText">class&#160;</h1>
              <h1 class="actualName">NathanDavisBarrett</h1>
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
              <h1 class="actualName">&lt;NathanDavisBarrett&#160;&#47;&gt;&#160;</h1>
              <span class="attrList" v-for="attr in codeNameAttrs" :key="attr">
                  <h1 class="extraText">&lt;&#47;{{attr}}&gt;&#160;</h1>
              </span>
          </span>
          <span class="codeName" id="nameSQL" title="SQL">
              <h1 class="extraText">SELECT&#160;</h1>
              <h1 class="actualName">NathanDavisBarrett</h1>
              <h1 class="extraText">&#160;FROM</h1>
              <span class="attrList" v-for="(attr, index) in codeNameAttrs" :key="attr">
                  <h1 class="extraText" v-if="index != 0">&#160;JOIN</h1>
                  <h1 class="extraText">&#160;{{attr}}</h1>
              </span>
          </span>
          <span class="codeName" id="nameVBA" title="VBA">
              <h1 class="extraText">Public&#160;</h1>
              <h1 class="actualName">NathanDavisBarrett</h1>
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
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Header',
  data() {
      return {
          codeNameAttrs: ["Engineer", "Developer", "Learner"],
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

@media only screen and (min-width: 2050px) {
    .Header {
            align-items: center;
    }
}
@media only screen and (max-width: 2051px) {
    .Header {
        align-items: flex-start;
    }
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
    font-size: large;
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
    height: 165px;
}

.logoContainer img {
    width: 370px;
    position: absolute;
    bottom: 0;
}

</style>
