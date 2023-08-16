<script>
  import { getContext } from "svelte"
  import { useLazyImage as lazyImage } from 'svelte-lazy-image';

  export let imgSrc
  export let imgAltText = "Assessment Capture"

  const { styleable } = getContext("sdk")
  const component = getContext("component")
</script>

<img use:styleable={$component.styles} data-src={imgSrc} alt={imgAltText} use:lazyImage />
