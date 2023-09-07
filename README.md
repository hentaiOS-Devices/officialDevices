![Header Image](.static/officialDevicesHeader.png)

# hentaiOS Official Devices Database

## Swiggity Swooty, I am inside your walls

This is hentaiOS Official Devices database, it is a database, You can become an entry inside it. I hope you are not startled by the YAML file.

This repository has the following structure:

```Treeview
.
├── buildChangeMeta.yaml
├── changelog/
│   ├── *.md
├── changelogData.yaml
└── furdata.yaml
```

`changelogData` contains changelog metadata file that will be rendered into the [Handlebars](https://handlebarsjs.com) template within the changelog file.

`changelogData` specified in the following format:

```yaml
# DO NOT EDIT THESE TWO FIELDS
version: 1
data_class: AD:LANNEOLIV:xx/eo

changeset_data:
   # the filename of the changelog that is placed on changelog directory
 - name: string
   # A subfield with encrypted data
   encrypted-field:
    data: string
    data_encrypted: true
   # A subfield with unencrypted data
   unencrypted-field: string
```

`furdata` contains Furries (Maintainer, Red.) metadata, specified in the following format:

```yaml
# DO NOT EDIT THESE TWO FIELDS
version: 1
data_class: AD:LANNEOLIV:xx/eo

devices:
 - name: string
   family: string
   brand_override: string,optional
   marketname_override: string,optional
furries:
 - family: string
   brand: string
   furs:
    - string
```

`buildChangeMeta` contains build to changelog relationship, specified in the following format:

```yaml
# DO NOT EDIT THESE TWO FIELDS
version: 1
data_class: INVIERNO:aa/xo

build_rel:
  - tag: string
    type: string
```
