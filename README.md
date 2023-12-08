# cg-python3-boshrelease

For vendoring python3 to BOSH releases

## Updating this release

1. Download a new [supported Python version](https://devguide.python.org/versions/#versions) from <https://www.python.org/downloads/>. Download the `Gzipped source tarball` file, since this release will install Python from source.
1. Add the blob for the downloaded Python tarball
1. Upload the new blob:

    ```shell
    bosh upload-blobs
    ```

    You will likely need to use `aws-vault` to provide credentials in your shell to upload the blob to the blobstore.
1. Update the `packages/python3` files to reference the new Python version

## test-python3 job

> **This job is NOT FOR PRODUCTION**

This job is a hello-world type http server, using python's http.server. It is not useful or safe for production environments.
