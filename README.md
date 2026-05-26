# openshift-pipeline-badges

Public badge data for all OpenShift CI/CD pipelines, read by [shields.io](https://shields.io/endpoint) to render live status badges.

## Structure

```text
{TEAM}/{PROJECT}/{APP_NAME}-status.json
{TEAM}/{PROJECT}/{APP_NAME}-version.json
{TEAM}/{PROJECT}/{APP_NAME}-lastbuilt.json
```

Files are written automatically by the `update-pipeline-badge` Tekton task on every pipeline run.

---

## Examples by Team

### dcm / pin-pad-verification

<!-- pin-pad-verification-app -->

[![Pipeline](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/wakefern/openshift-pipeline-badges/main/dcm/pin-pad-verification/pin-pad-verification-app-status.json)](https://github.com/wakefern/openshift-pipeline-badges)
[![Version](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/wakefern/openshift-pipeline-badges/main/dcm/pin-pad-verification/pin-pad-verification-app-version.json)](https://github.com/wakefern/openshift-pipeline-badges)
[![Last Built](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/wakefern/openshift-pipeline-badges/main/dcm/pin-pad-verification/pin-pad-verification-app-lastbuilt.json)](https://github.com/wakefern/openshift-pipeline-badges)

### devops / openshift-demos

<!-- openshift-test-app -->

[![Pipeline](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/wakefern/openshift-pipeline-badges/main/devops/openshift-demos/openshift-test-app-status.json)](https://github.com/wakefern/openshift-pipeline-badges)
[![Version](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/wakefern/openshift-pipeline-badges/main/devops/openshift-demos/openshift-test-app-version.json)](https://github.com/wakefern/openshift-pipeline-badges)
[![Last Built](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/wakefern/openshift-pipeline-badges/main/devops/openshift-demos/openshift-test-app-lastbuilt.json)](https://github.com/wakefern/openshift-pipeline-badges)

---

## For Developers — Add badges to your app README

Replace `{TEAM}`, `{PROJECT}`, and `{APP_NAME}` with your values:

```markdown
[![Pipeline](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/wakefern/openshift-pipeline-badges/main/{TEAM}/{PROJECT}/{APP_NAME}-status.json)](https://github.com/wakefern/openshift-pipeline-badges)
[![Version](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/wakefern/openshift-pipeline-badges/main/{TEAM}/{PROJECT}/{APP_NAME}-version.json)](https://github.com/wakefern/openshift-pipeline-badges)
[![Last Built](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/wakefern/openshift-pipeline-badges/main/{TEAM}/{PROJECT}/{APP_NAME}-lastbuilt.json)](https://github.com/wakefern/openshift-pipeline-badges)
```

Your values are set in your pipeline's `finally` block. Ask your platform team or check your pipeline YAML for `TEAM`, `PROJECT`, and confirm `APP_NAME` from the pipeline run logs.

| Team     | Project                | App Name                   | Values to use                                                           |
| -------- | ---------------------- | -------------------------- | ----------------------------------------------------------------------- |
| `dcm`    | `digital-profile`      | `digitalprofile`           | TEAM=dcm PROJECT=digital-profile APP_NAME=digitalprofile                |
| `dcm`    | `duo-mfa`              | `duo-mfa-device-portal`    | TEAM=dcm PROJECT=duo-mfa APP_NAME=duo-mfa-device-portal                 |
| `dcm`    | `pin-pad-verification` | `pin-pad-verification-app` | TEAM=dcm PROJECT=pin-pad-verification APP_NAME=pin-pad-verification-app |
| `dcm`    | `smart-label`          | `smart-label-frontend`     | TEAM=dcm PROJECT=smart-label APP_NAME=smart-label-frontend              |
| `devops` | `openshift-demos`      | `openshift-test-app`       | TEAM=devops PROJECT=openshift-demos APP_NAME=openshift-test-app         |
