<script lang="ts">
	/** Renders the caption as HTML */
	export let caption: string;
	export let width: string = "auto";
	export let style: string = "";
</script>

<div
	{...$$restProps}
	style="width: {width}; {style}"
	class="flex place-items-center justify-center flex-col"
>
	<slot />
	<div class="pt-4">
		<small class="text-gray-800 dark:text-gray-700">{@html caption}</small>
	</div>
</div>

<!--
@component
[Open Issue](https://github.com/ieedan/geist-ui-svelte/issues)
#### Description
A component for showing a caption below a bit of content.
##### Example:
```svelte
<Display caption="...">
	<Image ... />
</Display>
```
-->
