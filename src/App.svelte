<script>
	import { ZenButton, ZenInput } from '../';
	function handleInput(e) {
		name = e.target.value
    }
    let name = '';
</script>
<style>

</style>

<ZenButton width="100px" hollow>Primary</ZenButton>
<ZenButton width="100px" type="success" rounded>Secondary</ZenButton>
<ZenButton width="100px" disabled rounded>Disabled</ZenButton>
<ZenInput bind:value={name} placeholder="Placeholder" width="200px" disabled></ZenInput>
<span>{name}</span>
