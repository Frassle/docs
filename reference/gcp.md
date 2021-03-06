---
title: "GCP"
---

The GCP (Google Cloud Platform) provider for Pulumi can be used to provision any of the cloud resources available in [GCP](https://cloud.google.com/).  The GCP provider must be configured with credentials to deploy and update resources in Google Cloud.

See the [full API documentation](./pkg/nodejs/@pulumi/gcp/index.html) for complete details of the available GCP provider APIs.

## Example

```javascript
const gcp = require("@pulumi/gcp")

const bucket = new gcp.storage.Bucket("my-bucket");
```

You can find additional examples of using Google Cloud in [the Pulumi examples repo](https://github.com/pulumi/examples):
* [Google Compute Engine](https://github.com/pulumi/examples/tree/master/gcp-js-webserver)
* [Google Cloud Functions](https://github.com/pulumi/examples/tree/master/gcp-ts-functions)

## Libraries

The following packages are available in packager managers:
* JavaScript/TypeScript: https://www.npmjs.com/package/@pulumi/gcp
* Python: https://pypi.org/project/pulumi-gcp/
* Go: `github.com/pulumi/pulumi-aws/sdk/go/gcp`

The CGP provider is open source and available in the [pulumi/pulumi-gcp](https://github.com/pulumi/pulumi-gcp) repo. 

## Authentication

The GCP provider supports several options for providing access to Google Cloud credentials.  See [GCP installation page](/install/gcp.html) for details.

## Configuration

The GCP provider accepts the following configuration settings.  These can be provided to the default GCP provider via `pulumi config set gcp:<option>`, or passed to the constructor of `new gcp.Provider` to construct a specific instance of the GCP provider.

* `project`: (Required) The ID of the project to apply any resources to. This can also be specified using any of the following environment variables (listed in order of precedence): `GOOGLE_PROJECT`, `GOOGLE_CLOUD_PROJECT`, `GCLOUD_PROJECT`, `CLOUDSDK_CORE_PROJECT`.
* `credentials`: (Optional) Contents of a file that contains your service account private key in JSON format. You can download your existing Google Cloud service account file from the Google Cloud Console, or you can create a new one from the same page. Credentials can also be specified using any of the following environment variables (listed in order of precedence): `GOOGLE_CREDENTIALS`, `GOOGLE_CLOUD_KEYFILE_JSON`, `GCLOUD_KEYFILE_JSON`. The `GOOGLE_APPLICATION_CREDENTIALS` environment variable can also contain the path of a file to obtain credentials from. If no credentials are specified, the provider will fall back to using the Google Application Default Credentials. If you are running Pulumi from a GCE instance, see [Creating and Enabling Service Accounts for Instances](https://cloud.google.com/compute/docs/access/create-enable-service-accounts-for-instances) for details.
* `region`: (Optional) The region to operate under, if not specified by a given resource. This can also be specified using any of the following environment variables (listed in order of precedence): `GOOGLE_REGION`, `GCLOUD_REGION`, `CLOUDSDK_COMPUTE_REGION`.
* `zone`: (Optional) The zone to operate under, if not specified by a given resource.  This can also be specified using any of the following environment variables (listed in order of precedence): `GOOGLE_ZONE`, `GCLOUD_ZONE`, `CLOUDSDK_COMPUTE_ZONE`.
