<script lang="typescript">
	import PopupComboBox from './PopupComboBox.svelte';
</script>

<h1>Welcome to SvelteKit</h1>

<form method="post">
	<PopupComboBox name="AlbumId" valueDisplay="Album XYZ" heading="Select An Ablum" valueId={1} />
	<button type="submit">Submit</button>
</form>

<button class="bg-gray-100 px-3 py-1 rounded-lg">Close</button>
