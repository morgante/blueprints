# Cloud Build package

This package demonstrates using `kpt` to manage Cloud Build configurations.

## Usage

kpt pkg get https://github.com/morgante/blueprints.git/catalog/cloudbuild@demo/cloudbuild

## Demo

1. Check out the initial package.

    kpt pkg get https://github.com/morgante/blueprints.git/catalog/cloudbuild@2be4346763dc98c479110673bfed3e6a72c27dc9

2. Commit it.

    git add cloudbuild
    git commit -m "Add Cloud Build config"

3. Make some local modifications (ex. change the Golang version in cloudbuild.yaml)
3. Commit changes

    git add cloudbuild
    git commit -m "local Cloud Build changes"

4. Update the upstream

    kpt pkg update demo/cloudbuild