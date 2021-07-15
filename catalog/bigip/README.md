# bigip

## Description
sample description

## Usage

### Fetch the package
`kpt pkg get REPO_URI[.git]/PKG_PATH[@VERSION] bigip`
Details: https://kpt.dev/reference/cli/pkg/get/

### View package content
`kpt pkg tree bigip`
Details: https://kpt.dev/reference/cli/pkg/tree/

### Apply the package
```
kpt live init bigip
kpt live apply bigip --reconcile-timeout=2m --output=table
```
Details: https://kpt.dev/reference/cli/live/
