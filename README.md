# vue-fineuploader

[![Build Status](https://travis-ci.org/Elhebert/vue-fineuploader.svg?branch=master)](https://travis-ci.org/Elhebert/vue-fineuploader)
[![Dependency Status](https://david-dm.org/Elhebert/vue-fineuploader.svg)](https://david-dm.org/Elhebert/vue-fineuploader)
[![devDependency Status](https://david-dm.org/Elhebert/vue-fineuploader/dev-status.svg)](https://david-dm.org/Elhebert/vue-fineuploader?type=dev)

A VueJS 2 Component for Fine Uploader with a drag'n'drop area.

## Usage

### Installation

Get the `FineUploader` component:

- with npm:
```
npm install --save vue-fineuploader
```
- clone this repository and copy the `FineUploader.vue` into your project:
```
git clone https://github.com/Elhebert/vue-fineuploader.git
```


### Options

- `options`: Object containing the different configuration options

    See the official Fine Uploader documentation [for detailed information about the different options](http://docs.fineuploader.com/branch/master/api/options.html)

- `callbacks`: Object containing the different callbacks to execute when events are triggers.

    See the official Fine Uploader documentation [for detailed information about the different events](http://docs.fineuploader.com/branch/master/api/events.html)

- `dropzone`: Object container the different dropzone options

	The possible options are:
    
    `element`: id or class of the container element that should be treated as drop zone.  
    `dropActive`: Specify a CSS class to apply to drop zone(s) when a file has entered it.

### Example

```js
<template>
    <div>
        <FineUplaoder :options="options" :callbacks="callbacks" :dropzone="dropzone">
            <div class="drop-area">
                Drop your files here<br>
                or<br>
                <div class="browse"></div>
            </div>
        </FineUplaoder>
    </div>
</template>

<style></style>

<script language="text/babel">
import FineUplaoder from './path/to/FineUploader.vue';

export default {
    data() {
        return {
            options: {
                button: '.browse',
                request: {
                    endpoint: '/path/to/your/endpoint'
                }
            },
            callbacks: {},
            dropzone: {
                element: '.droparea',
                dropActive: '.active'
            },
        };
    },

    components: { FineUploader },
};
</script>
```

This script is published under the [MIT license](./LICENSE)
