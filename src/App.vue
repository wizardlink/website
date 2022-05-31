<template>
  <section id="face" class="hero is-fullheight">
    <div class="hero-head">
      <div id="stars"></div>
    </div>

    <div class="hero-body is-align-self-center">
      <div class="block is-flex is-flex-direction-column is-align-items-center">
        <figure class="image is-128x128">
          <!-- MD5 hash of my e-mail is used here to pull the right gravatar. -->
          <img class="is-rounded" src="https://www.gravatar.com/avatar/e2e6de9b912a77f0f7137272cf462745?s=2048">
        </figure>

        <h2 class="has-text-white is-size-3">
          wizardlink
        </h2>

        <nav class="level is-mobile">
          <a class="level-item mx-1" href="https://github.com/wizardlink" target="_blank">
            <icon icon="mdi-github" size="mdi-24px" />
          </a>

          <a class="level-item mx-1" href="https://linkedin.com/in/wizardlink" target="_blank">
            <icon icon="mdi-linkedin" size="mdi-24px" />
          </a>

          <a class="level-item mx-1" href="https://twitter.com/thewizardlink" target="_blank">
            <icon icon="mdi-twitter" size="mdi-24px" />
          </a>

          <a class="level-item mx-1" href="https://twitch.tv/thewizardlink" target="_blank">
            <icon icon="mdi-twitch" size="mdi-24px" />
          </a>

          <a class="level-item mx-1" href="https://youtube.com/whitelinkker" target="_blank">
            <icon icon="mdi-youtube" size="mdi-24px" />
          </a>

          <a class="level-item mx-1" href="https://steamcommunity.com/id/thewizardlink" target="_blank">
            <icon icon="mdi-steam" size="mdi-24px" />
          </a>
        </nav>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component'
import Icon from './components/MDIcon.vue'
@Options({
  components: { Icon }
})
export default class App extends Vue {}
</script>

<style lang="scss" scoped>
  @function multiple-box-shadow ($n) {
    $value: '#{random(2000)}px #{random(2000)}px #FFF';
    @for $i from 2 through $n {
      $value: '#{$value}, #{random(2000)}px #{random(2000)}px #FFF';
    }
    @return unquote($value);
  }
  $dots: multiple-box-shadow(831);
  #stars {
    width: 2px;
    height: 2px;
    background: transparent;
    box-shadow: $dots;
  }
</style>
