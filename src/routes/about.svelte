<script lang="ts">
	import SplitioIcon from '$lib/SplitioIcon.svelte';
	import Button, { Label, Icon } from '@smui/button';
	import Paper, { Title, Content } from '@smui/paper';
</script>

<svelte:head>
	<title>e-ndajme | about</title>
</svelte:head>

<div class="homepage-container">
	<div>
		<SplitioIcon />
	</div>
	<div class="group-text-container">
		<Paper class="paper-demo" elevation={5}>
			<Title>ℹ️ pakez info</Title>
			<Content style="white-space: pre-line;">
				ndani me lehtësi faturat tuaja! E-ndajme, është një aplikacion web, i krijuar për të gjurmuar shpejt borxhet dhe pagesat, pa asnjë llogari përdoruesi.

të gjitha informacionet shpërndahen në një mënyrë p2p (si një torrent), prandaj sigurohuni që të lidheni me miqtë tuaj në të njëjtën kohë nëse diçka nuk shkon.

ndërtuar nga kriptoboidi me SvelteKit dhe GunDB.
				<!-- <Button
					on:click={() => {}}
					variant="raised"
					href="https://github.com/cryptoboid/splitio"
					target="_blank"
					rel="noopener noreferrer"
					style="display: flex; margin-top: 1rem"
				>
					<Label>GitHub</Label>
					<Icon class="material-icons">open_in_new</Icon>
				</Button> -->
			</Content>
		</Paper>
	</div>
</div>

<style>
	.homepage-container {
		min-height: 100vh;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	.group-text-container {
		margin-top: 1.5rem;
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
	}

	* :global(.info-btn) {
		position: absolute;
		top: 1rem;
		right: 1rem;
	}

	* :global(.paper-demo) {
		margin: 0 1rem;
		max-width: 600px;
	}
</style>
