<img width="200" src="https://raw.githubusercontent.com/sveltejs/svelte/29052aba7d0b78316d3a52aef1d7ddd54fe6ca84/site/static/images/svelte-android-chrome-512.png">

# ZEN SVELTE UI

## Features

- Based on `Svelte`
- Lightweight
- Support modern browsers and IE 12+

# Installation
```bash
npm install zen-svelte-ui
```

# Usage
In .svelte file

## ZenButton
```html
<script>
    import { ZenButton } from 'zen-svelte-ui';
</script>

<ZenButton on:click={() => console.log('hello')} type="success" hollow>Hello world!</ZenButton>
```

| Property  | Description | Type | Accepted Values | Default |
| --------- | ----------- | ---- | --------------- | ------- |
| type  | The button style  | String | primary, success | primary |
| width  | Button width  | String | css width values | 100% |
| rounded  | Round corners  | Boolean | true, false | false |
| disabled  | Disabling style and cancel click event  | Boolean | true, false | false |
| hollow  | Hollow style  | Boolean | true, false | false |
| Slot  | Button text | String | any | '' |

## ZenInput
```html
<script>
    import { ZenInput } from 'zen-svelte-ui';
    let name = '';
</script>

<ZenInput bind:value={name} placeholder="Your name" width="200px" status="error"></ZenInput>
```

| Property  | Description | Type | Accepted Values | Default |
| --------- | ----------- | ---- | --------------- | ------- |
| type  | The input type  | String | text, password | text |
| width  | Input width  | String | css width values | 100% |
| disabled  | Disabling style and input  | Boolean | true, false | false |
| placeholder  | Input placeholder  | String | any | '' |
| status  | Status styles | String | info, success, error, warning | '' |

## ZenCheckbox
```html
<script>
    import { ZenCheckbox } from 'zen-svelte-ui';
    let checked = false;
</script>

<ZenCheckbox bind:checked={checked}>Check this out!</ZenCheckbox>
```

| Property  | Description | Type | Accepted Values | Default |
| --------- | ----------- | ---- | --------------- | ------- |
| disabled  | Disabling style and cancel check event  | Boolean | true, false | false |
| Slot  | Label text | String | any | '' |
