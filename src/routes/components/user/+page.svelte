<script lang="ts">
	import Code from "$lib/code/Code.svelte";
	import Details from "$lib/details/Details.svelte";
	import FieldSet from "$lib/fieldset/FieldSet.svelte";
	import Snippet from "$lib/snippet/Snippet.svelte";
	import Spacer from "$lib/spacer/Spacer.svelte";
	import Text from "$lib/text/Text.svelte";
	import User from "$lib/user/User.svelte";
</script>

<Text type="h3">User</Text>
<Spacer h={10} />
<Text>A layout component to display a user.</Text>
<Spacer h={20} />
<Snippet width="450px" type="lite" text={`import { User } from 'geist-ui-svelte';`} />
<Spacer h={30} />
<Text type="h4">Basic</Text>
<Spacer h={5} />
<Text>When there is no image supplied it will use your initials for your `Avatar`.</Text>
<Spacer h={10} />
<FieldSet>
	<div class="flex gap-2 justify-start">
		<User name="Aidan" />
		<User name="Aidan Bleser" />
		<User name="Aidan R Bleser" />
		<User name="Eva Rivera" />
	</div>
	<div slot="footer">
		<Details label="Code">
			<Code
				lang="svelte"
				code={`<User name="Aidan" />
<User name="Aidan Bleser" />
<User name="Aidan R Bleser" />
<User name="Eva Rivera" />`}
			/>
		</Details>
	</div>
</FieldSet>
<Spacer h={30} />
<Text type="h4">With Avatar</Text>
<Spacer h={10} />
<FieldSet>
	<div class="flex flex-col justify-start">
		<User name="Aidan" img="https://avatars.githubusercontent.com/u/117548273?v=4" />
	</div>
	<div slot="footer">
		<Details label="Code">
			<Code
				lang="svelte"
				code={`<User 
	name="Aidan"
	img="https://avatars.githubusercontent.com/u/117548273?v=4"/>`}
			/>
		</Details>
	</div>
</FieldSet>
<Spacer h={30} />
<Text type="h4">With Name</Text>
<Spacer h={5} />
<Text>Add <code>`detail`</code> attribute to expose the name.</Text>
<Spacer h={10} />
<FieldSet>
	<div class="flex flex-col justify-start">
		<User name="Aidan" img="https://avatars.githubusercontent.com/u/117548273?v=4" detail />
	</div>
	<div slot="footer">
		<Details label="Code">
			<Code
				lang="svelte"
				code={`<User 
	name="Aidan" 
	img="https://avatars.githubusercontent.com/u/117548273?v=4" 
	detail/>`}
			/>
		</Details>
	</div>
</FieldSet>
<Spacer h={30} />
<Text type="h4">With Description</Text>
<Spacer h={5} />
<Text>
	Add <code>`details`</code> attribute to add extra description below the name. This does require
	the <code>`detail`</code> attribute.
</Text>
<Spacer h={10} />
<FieldSet>
	<div class="flex flex-col justify-start">
		<User
			name="Aidan"
			img="https://avatars.githubusercontent.com/u/117548273?v=4"
			detail
			details="Trash Dev"
		/>
	</div>
	<div slot="footer">
		<Details label="Code">
			<Code
				lang="svelte"
				code={`<User
	name="Aidan"
	img="https://avatars.githubusercontent.com/u/117548273?v=4"
	detail
	details="Trash Dev" />`}
			/>
		</Details>
	</div>
</FieldSet>
