<script lang="ts">
  import type { HTMLAttributes } from "svelte/elements";
  import { cn } from "$lib/utils.js";

  type $$Props = HTMLAttributes<HTMLTableRowElement> & {
    "data-state"?: unknown;
  };

  let className: $$Props["class"] = undefined;
  export { className as class };
</script>

<tr
  class="{cn(
    'border-b transition-colors hover:bg-muted/50 data-[state=selected]:bg-muted',
    className,
  )}"
  {...$$restProps}
  on:click
  on:keydown>
  <slot />
</tr>
