<script lang="ts">
	import Code from "$lib/code/Code.svelte";
	import Details from "$lib/details/Details.svelte";
	import FieldSet from "$lib/fieldset/FieldSet.svelte";
	import Snippet from "$lib/snippet/Snippet.svelte";
	import Spacer from "$lib/spacer/Spacer.svelte";
	import Text from "$lib/text/Text.svelte";
	import Badge from "$lib/badge/Badge.svelte";
</script>

<Text type="h3">Badge</Text>
<Spacer h={10} />
<Text>A simple component for status indicators or notification markers.</Text>
<Spacer h={20} />
<Snippet width="425px" type="lite" text={`import { Badge } from 'geist-ui-svelte';`} />
<Spacer h={30} />
<Text type="h4">Sizes</Text>
<Spacer h={10} />
<FieldSet>
	<div class="flex gap-2 place-items-end justify-start">
		<Badge size="xs">xs</Badge>
		<Badge size="sm">sm</Badge>
		<Badge size="md">md</Badge>
		<Badge size="lg">lg</Badge>
		<Badge size="xl">xl</Badge>
	</div>
	<div slot="footer">
		<Details label="Code">
			<Code
				lang="svelte"
				code={`<Badge size="xs">xs</Badge>
<Badge size="sm">sm</Badge>
<Badge size="md">md</Badge>
<Badge size="lg">lg</Badge>
<Badge size="xl">xl</Badge>`}
			/>
		</Details>
	</div>
</FieldSet>
<Spacer h={30} />
<Text type="h4">Colors</Text>
<Spacer h={10} />
<FieldSet>
	<div class="flex flex-col gap-2 justify-start">
		<Badge size="xs">Default</Badge>
		<Badge size="xs" type="success">Success</Badge>
		<Badge size="xs" type="warning">Warning</Badge>
		<Badge size="xs" type="error">Error</Badge>
		<Badge size="xs" type="secondary">Secondary</Badge>
	</div>
	<div slot="footer">
		<Details label="Code">
			<Code
				lang="svelte"
				code={`<Badge size="xs">Default</Badge>
<Badge size="xs" type="success">Success</Badge>
<Badge size="xs" type="warning">Warning</Badge>
<Badge size="xs" type="error">Error</Badge>
<Badge size="xs" type="secondary">Secondary</Badge>`}
			/>
		</Details>
	</div>
</FieldSet>
