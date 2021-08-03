# Vuetify File Browser

Open source file manager component for Vue.js. Requires Vuetify v2.0 or higher.

[💣 Demo]

[🚀 Backend]

![Screenshot]

## Features

**Storages:**
- [x] Local Filesystem;
- [x] Amazon S3;
- [ ] Dropbox;
- [ ] Google Drive;

**Functions:**
- [x] Multiple file uploading
- [x] Create folder;
- [x] Delete file/folder;
- [x] Filtering;

## Usage

```
npm i vuetify-file-browser
```

```html
<template>
    <file-browser :axiosConfig="{baseURL: 'http://localhost:8081'}" />
</template>

<script>
import FileBrowser from "vuetify-file-browser";

export default {
    components: {
        FileBrowser
    }
};
</script>
```

## Props

```js
// comma-separated list of active storage codes
storages: {
    type: String,
    default: () => availableStorages.map(item => item.code).join(",")
},
// code of default storage
storage: { type: String, default: "local" },
// show tree view
tree: { type: Boolean, default: true },
// file icons set
icons: { type: Object, default: () => fileIcons },
// custom backend endpoints
endpoints: { type: Object, default: () => endpoints },
// custom axios instance
axios: { type: Function },
// custom configuration for internal axios instance
axiosConfig: { type: Object, default: () => {} },
// max files count to upload at once. Unlimited by default
maxUploadFilesCount: { type: Number, default: 0 },
// max file size to upload. Unlimited by default
maxUploadFileSize: { type: Number, default: 0 }
```