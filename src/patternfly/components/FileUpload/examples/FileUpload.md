---
id: Simple file upload
section: components
subsection: file-upload
cssPrefix: pf-v5-c-file-upload
---

## Examples

### Basic file upload
```hbs
{{#> file-upload file-upload--id="basic-file-upload"}}
  {{#> file-upload-file-select}}
    {{#> input-group}}
      {{#> input-group-item input-group-item--IsFill=true}}
        {{> file-upload-text-input
          file-upload-text-input--aria-label="Drag and drop a file or upload one"
          file-upload-text-input--attribute=(concat 'readonly placeholder="Drag and drop a file or upload one" aria-describedby="' file-upload--id '-browse"')
          }}
      {{/input-group-item}}
      {{#> input-group-item}}
        {{#> button button--modifier="pf-m-control" button--attribute=(concat 'id="' file-upload--id '-browse"')}}
          Upload
        {{/button}}
      {{/input-group-item}}
      {{#> input-group-item}}
        {{#> button button--modifier="pf-m-control" button--attribute="disabled"}}
          Clear
        {{/button}}
      {{/input-group-item}}
    {{/input-group}}
  {{/file-upload-file-select}}
  {{#> file-upload-file-details file-upload-file-details--aria-label="Empty text area"}}
  {{/file-upload-file-details}}
{{/file-upload}}
```

### Upload complete non editable
```hbs
{{#> file-upload file-upload--id="browsed-file-upload-complete"}}
  {{#> file-upload-file-select}}
    {{#> input-group}}
      {{#> input-group-item input-group-item--IsFill=true}}
        {{> file-upload-text-input
          file-upload-text-input--aria-label="Read only filename"
          file-upload-text-input--attribute=(concat 'readonly value="Read only filename" aria-describedby="' file-upload--id '-browse"')
          }}
      {{/input-group-item}}
      {{#> input-group-item}}
        {{#> button button--modifier="pf-m-control" button--attribute=(concat 'id="' file-upload--id '-browse"')}}
          Upload
        {{/button}}
      {{/input-group-item}}
      {{#> input-group-item}}
        {{#> button button--modifier="pf-m-control"}}
          Clear
        {{/button}}
      {{/input-group-item}}
    {{/input-group}}
  {{/file-upload-file-select}}
  {{#> file-upload-file-details file-upload-file-details--aria-label="Text area" file-upload-file-details--attribute='readonly'}}Ssh-Rsa AAh3zJFkzjjakCJialksjfB3zJFkzzAAhhMskjjakCJialksjfB3z89z3zJFkz3 +kzMAjsauoox88aaZXphBx4fczJFkzMAjsauoox88aaZXphBx4fczJFkzMAjsauoox88aaZXphBx4fc
  {{/file-upload-file-details}}
{{/file-upload}}
```

### Upload complete editable
```hbs
{{#> file-upload file-upload--id="drop-file"}}
  {{#> file-upload-file-select}}
    {{#> input-group}}
      {{#> input-group-item input-group-item--IsFill=true}}
        {{> file-upload-text-input
          file-upload-text-input--aria-label="Read only filename"
          file-upload-text-input--attribute=(concat 'readonly value="Sample.txt" aria-describedby="' file-upload--id '-browse"')
          }}
      {{/input-group-item}}
      {{#> input-group-item}}
        {{#> button button--modifier="pf-m-control" button--attribute=(concat 'id="' file-upload--id '-browse"')}}
          Upload
        {{/button}}
      {{/input-group-item}}
      {{#> input-group-item}}
        {{#> button button--modifier="pf-m-control"}}
          Clear
        {{/button}}
      {{/input-group-item}}
    {{/input-group}}
  {{/file-upload-file-select}}
  {{#> file-upload-file-details file-upload-file-details--aria-label="Text area"}}Ssh-Rsa AAh3zJFkzjjakCJialksjfB3zJFkzzAAhhMskjjakCJialksjfB3z89z3zJFkz3 +kzMAjsauoox88aaZXphBx4fczJFkzMAjsauoox88aaZXphBx4fczJFkzMAjsauoox88aaZXphBx4fc
  {{/file-upload-file-details}}
{{/file-upload}}
```

### Drag file hover component
```hbs
{{#> file-upload file-upload--id="drag-file-hover-component" file-upload--modifier="pf-m-drag-hover"}}
  {{#> file-upload-file-select}}
    {{#> input-group}}
      {{#> input-group-item input-group-item--IsFill=true}}
        {{> file-upload-text-input file-upload-text-input--aria-label="Drag and drop a file or upload one" file-upload-text-input--attribute=(concat 'readonly placeholder="Drag and drop a file or upload one" aria-describedby="' file-upload--id '-browse"')}}
      {{/input-group-item}}
      {{#> input-group-item}}
        {{#> button button--modifier="pf-m-control" button--attribute=(concat 'id="' file-upload--id '-browse"')}}
          Upload
        {{/button}}
      {{/input-group-item}}
      {{#> input-group-item}}
        {{#> button button--modifier="pf-m-control" button--attribute="disabled"}}
          Clear
        {{/button}}
      {{/input-group-item}}
    {{/input-group}}
  {{/file-upload-file-select}}
  {{#> file-upload-file-details file-upload-file-details--aria-label="Empty text area"}}
  {{/file-upload-file-details}}
{{/file-upload}}
```

### File upload in form with error
```hbs
{{#> form}}
  {{#> form-group}}
    {{#> file-upload file-upload--id="file-upload-error"}}
      {{#> file-upload-file-select}}
        {{#> input-group}}
          {{#> input-group-item input-group-item--IsFill=true}}
            {{> file-upload-text-input
              file-upload-text-input--aria-label="File upload error"
              file-upload-text-input--attribute=(concat 'required value="Sample.png"  aria-describedby="' file-upload--id '-browse"')
              }}
          {{/input-group-item}}
          {{#> input-group-item}}
            {{#> button button--modifier="pf-m-control" button--attribute=(concat 'id="' file-upload--id '-browse"')}}
              Upload
            {{/button}}
          {{/input-group-item}}
          {{#> input-group-item}}
            {{#> button button--modifier="pf-m-control"}}
              Clear
            {{/button}}
          {{/input-group-item}}
        {{/input-group}}
      {{/file-upload-file-select}}
      {{#> file-upload-file-details file-upload-file-details--attribute='aria-describedby="textAreaHelperText1" aria-invalid="true"' file-upload-file-details--aria-label="Empty text area"}}{{/file-upload-file-details}}
    {{/file-upload}}
    {{#> form-helper-text}}
      {{> helper-text helper-text--value="We don't support this file type. Try again with a different file type." helper-text-item--id='textAreaHelperText1' helper-text-item--IsError=true}}
    {{/form-helper-text}}
  {{/form-group}}
{{/form}}
```

### File upload loading
```hbs
{{#> file-upload file-upload--id="file-upload-loading" file-upload--modifier="pf-m-loading"}}
  {{#> file-upload-file-select}}
    {{#> input-group}}
      {{#> input-group-item input-group-item--IsFill=true}}
        {{> file-upload-text-input
          file-upload-text-input--aria-label="Read only filename"
          file-upload-text-input--attribute=(concat 'readonly name="file-upload-loading" value="Sample.png" aria-describedby="' file-upload--id '-browse"')
        }}
      {{/input-group-item}}
      {{#> input-group-item}}
        {{#> button button--modifier="pf-m-control" button--attribute=(concat 'disabled id="' file-upload--id '-browse"')}}
          Upload
        {{/button}}
      {{/input-group-item}}
      {{#> input-group-item}}
        {{#> button button--modifier="pf-m-control"}}
          Clear
        {{/button}}
      {{/input-group-item}}
    {{/input-group}}
  {{/file-upload-file-select}}
  {{#> file-upload-file-details file-upload-file-details--aria-label="Text area" file-upload-file-details--HasSpinner="true"}}Ssh-Rsa AAh3zJFkzjjakCJialksjfB3zJFkzzAAhhMskjjakCJialksjfB3z89z3zJFkz3 +kzMAjsauoox88aaZXphBx4fczJFkzMAjsauoox88aaZXphBx4fczJFkzMAjsauoox88aaZXphBx4fc
  {{/file-upload-file-details}}
{{/file-upload}}
```

## Documentation

### Overview

### Usage

| Class | Applied to | Outcome |
| -- | -- | -- |
| `.pf-v5-c-file-upload` | `<div>`, `<form>` | Initiates the file upload component. **Required**. |
| `.pf-v5-c-file-upload__file-select` | `<div>` | Initiates the file select element. **Required** |
| `.pf-v5-c-file-upload__file-details` | `<div>` | Initiates the file details element. **Required** |
| `.pf-v5-c-file-upload__file-details-spinner` | `<div>` | Initiates the file details element. **Required** |
| `.pf-m-drag-hover` | `.pf-v5-c-file-upload` | Modifies file upload for when an element is dragged or dropped inside of its container. |
| `.pf-m-loading` | `.pf-v5-c-file-upload` | Modifies file upload for the loading state. |
