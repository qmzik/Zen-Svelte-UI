<script>
    export let type = 'primary';
    export let rounded = false;
    export let disabled = false;
    export let width = '100%';
    export let hollow = false;
</script>

<style>
.btn {
    cursor: pointer;
    padding: 10px 15px;
    width: 100%;
    text-align: center;
    border-radius: 20px;
    user-select: none;
    border-radius: 5px;
    transition: .3s;
}

.primary:hover, .success:hover {
    opacity: .9;
}

.primary {
    background-color: #6190e8;
    color: white;
}

.success {
    background-color: #13ce66;
    color: white;
}

.primary_hollow:hover, .success_hollow:hover {
    background-color: rgba(179, 172, 172, .1)
}

.primary_hollow {
    color: #6190e8;
    border: 1px #6190e8 solid;
}

.success_hollow {
    color: #13ce66;
    border: 1px #13ce66 solid;
}

.disabled {
    opacity: .5 !important;
    cursor: not-allowed;
}

.rounded {
    border-radius: 30px;
}
</style>

<div on:click
     class="btn {hollow ? `${type}_hollow` : type}"
     class:disabled={disabled}
     class:rounded={rounded}
     style='width: {width}'
>
    <slot></slot>
</div>
