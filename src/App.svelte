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

<AppButton width="100px">Primary</AppButton>
<AppButton width="100px" type="secondary">Secondary</AppButton>
<AppButton width="100px" disabled>Disabled</AppButton>
