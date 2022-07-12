<script lang="ts">
	import Dialog, { Title, Content, Actions } from '@smui/dialog';
	import Button, { Label } from '@smui/button';
	import Textfield from '@smui/textfield';

	export let openDialog = false;
	export let addCallback: Function = () => {};

	let inputName: string = '';
</script>

<Dialog
	bind:open={openDialog}
	aria-labelledby="default-focus-title"
	aria-describedby="default-focus-content"
>
	<Title id="default-focus-title">👋 fute ktu</Title>
	<Content id="default-focus-content">
		<div>
			vendos emrin e tij:
			<Textfield bind:value={inputName} />
		</div>

		<p>⚠️ Nese e shtoni, <strong>ju nuk mundeni ta editoni ose fshini pjestarin</strong>, keshtu qe ndajeni mendjen!</p>
	</Content>
	<Actions>
		<Button>
			<Label>hiqe</Label>
		</Button>
		<Button
			variant="unelevated"
			disabled={inputName === ''}
			on:click={() => {
				addCallback(inputName);
				inputName = '';
			}}
		>
			<Label>shtoje</Label>
		</Button>
	</Actions>
</Dialog>
