<template>
  <span :class="spanClasses">
    <i :class="iconClasses"></i>
  </span>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component'
@Options({
  props: {
    color: {
      type: String,
      default: 'has-text-white'
    },
    icon: String,
    size: String
  }
})
export default class MDIcon extends Vue {
  /**
   * Color of the icon, using Bulma
   * @see {@link https://bulma.io/documentation/helpers/color-helpers/}
   */
  public readonly color!: string
  /**
   * Name of the icon
   * @see {@link https://materialdesignicons.com/}
   */
  public readonly icon!: string
  /**
   * Size of the icon, this must be passed as a number.
   * @see {@link https://bulma.io/documentation/elements/icon/#material-design-icons}
   */
  public readonly size!: string

  get spanClasses (): string[] {
    return ['icon', this.color]
  }

  get iconClasses (): string[] {
    return ['mdi', this.icon, this.size]
  }
}
</script>
