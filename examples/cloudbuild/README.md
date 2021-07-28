# Cloud Build example

This package demonstrates using `kpt` to manage Cloud Build configurations.

There is a base [Cloud Build package](../../catalog/cloudbuild) which includes a [Cloud Build yaml config](https://cloud.google.com/build/docs/build-config-file-schema).
Each team which wants to reuse this base configuration just fetchs a copy of it using `kpt`. They can then make local modifications to the script for their application.
When they want to update to the latest upstream, they just run `kpt pkg update`.

## Demo

1. Check out the initial package.

    kpt pkg get https://github.com/morgante/blueprints.git/catalog/cloudbuild@2be4346763dc98c479110673bfed3e6a72c27dc9

2. Commit it.

    git add cloudbuild
    git commit -m "Add Cloud Build config"

3. Make some local modifications (ex. add a new step in cloudbuild.yaml)
3. Commit changes

    git add cloudbuild
    git commit -m "local Cloud Build changes"

4. Update the upstream

    kpt pkg update demo/cloudbuild