<script lang="ts">
	import Dialog, { Title, Content, Actions } from '@smui/dialog';
	import Button, { Label } from '@smui/button';
	import Textfield from '@smui/textfield';
	import LayoutGrid, { Cell } from '@smui/layout-grid';
	import Select, { Option } from '@smui/select';
	import Icon from '@smui/select/icon';
	import { Graphic } from '@smui/list';
	import { getMemberAvatarURL } from './_modules/utils';

	export let openDialog = false;
	export let addCallback: Function = () => {};
	export let membersList: Array<Array<string | object>> = [];

	let inputName: string = '';
	let inputAmount: number = 0.0;
	let inputPaidBy: string = '';
</script>

<Dialog
	bind:open={openDialog}
	aria-labelledby="default-focus-title"
	aria-describedby="default-focus-content"
>
	<Title id="default-focus-title">🧾 shto shpenzimin</Title>
	<Content id="default-focus-content">
		<LayoutGrid>
			<Cell span={12}>
				cfare u ble?:
				<Textfield bind:value={inputName} />
			</Cell>
			<Cell span={12}>
				vendos shumen ne Lek:
				<Textfield type="number" bind:value={inputAmount} />
			</Cell>
			<Cell span={12}>
				kush pagoji?
				<Select bind:value={inputPaidBy} class="add-expense-select">
					<Icon
						slot="leadingIcon"
						style="background-image: url({getMemberAvatarURL(inputPaidBy, 24)});"
					/>
					<Option value="" />
					{#each membersList as [key, member]}
						<Option value={member.name}>
							<Graphic
								style="background-image: url({getMemberAvatarURL(member.name, 24)});"
							/>{member.name}</Option
						>
					{/each}
				</Select>
			</Cell>
		</LayoutGrid>
	</Content>
	<Actions>
		<Button>
			<Label>fshije</Label>
		</Button>
		<Button
			variant="unelevated"
			disabled={inputName === '' || inputAmount === 0.0 || inputPaidBy === ''}
			on:click={() => {
				addCallback(inputName, inputAmount, inputPaidBy);
				inputName = '';
				inputAmount = 0.0;
				inputPaidBy = '';
			}}
		>
			<Label>shtoje</Label>
		</Button>
	</Actions>
</Dialog>
