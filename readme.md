# sv-dropzone

sv-dropzone is a simple & ssr ready wrapper around [dropzoneJS] for [svelte] and [sapper].
![cover](https://raw.githubusercontent.com/arnaudDerbey/sv-dropzone/master/cover.png)

## Installation

```bash
$ npm i sv-dropzone
```

## Usage

```javascript

<script>
  import Dropzone from "sv-dropzone";
  const addedfile = file => console.log(file);
  const drop = event => console.log(event.target);
  const init = () => console.log("dropzone init ! 😍");
</script>

<Dropzone
  dropzoneClass="dropZoneClass"
  hooveringClass="hooveringClass"
  id="id"
  dropzoneEvents={{ addedfile, drop }}
  options={{ clickable: true, acceptedFiles: 'text/javascript', maxFilesize: 256, init }}>
  <p>hello</p>
</Dropzone>

```

## API

| prop           | default                                                                                | type/structure                        |
| -------------- | -------------------------------------------------------------------------------------- | ------------------------------------- |
| dropzoneEvents | {}                                                                                     | object:{{ [eventName]: func}}         |
| options        | { previewTemplate: "`<div/>`", dictDefaultMessage: "" }                                | object:{{ [optionName]: optionValue}} |
| dropzoneClass  | "dropzone"                                                                             | string                                |
| hooveringClass | "dropzone-hoovering"                                                                   | string                                |
| id             | "dropId"                                                                               | string                                |
| autoDiscover   | false                                                                                  | bool                                  |
| slot           | `<p class="dropzoneDefaultSentence"> drop your file(s) here or click to add file </p>` | element                               |

- All dropzone events can be found [here](https://www.dropzonejs.com/#events-list)
- All dropzone options can be found [here](https://www.dropzonejs.com/#configuration-options)

[dropzonejs]: https://www.dropzonejs.com/
[svelte]: https://svelte.dev/
[sapper]: https://svelte.dev/
[eventname]: https://www.dropzonejs.com/#events
[optionname]: https://www.dropzonejs.com/#configuration-options
[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"
