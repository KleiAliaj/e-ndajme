<script lang="ts">
	import Button, { Label } from '@smui/button';

	import Dialog, { Header, Title, Content, Actions } from '@smui/dialog';

	export let openDialog = false;
</script>

<Dialog
	bind:open={openDialog}
	aria-labelledby="default-focus-title"
	aria-describedby="default-focus-content"
>
	<Header>
		<Title id="fullscreen-title">🌐 Probleme me sinkronizimin?</Title>
	</Header>
	<Content id="default-focus-content" class="mdc-typography--body1" style="white-space: pre-line;">
		
i gjithë informacioni në e-ndajme shpërndahet p2p, si një torrent.

kur një grupi kërkon shumë kohë për t'u ngarkuar (ose nuk do të ngarkohet), ose kur mungojnë disa shpenzime, hapni grupin në një pajisje tjetër në të njëjtën kohë për të rifreskuar informacionin.
	</Content>
	<Actions>
		<Button>
			<Label>ne rregull</Label>
		</Button>
	</Actions>
</Dialog>
