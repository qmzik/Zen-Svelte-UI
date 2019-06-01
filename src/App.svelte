<script>
	import AppButton from './ZenButton.svelte';
	function handler() {
		console.log(1);
	}
</script>
<style>
	.item {
		margin-bottom: 10px;
	}
</style>

<AppButton width="100px" hollow>Primary</AppButton>
<AppButton width="100px" type="success" rounded>Secondary</AppButton>
<AppButton width="100px" disabled rounded>Disabled</AppButton>
