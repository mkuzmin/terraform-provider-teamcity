---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "teamcity_global_settings Resource - terraform-provider-teamcity"
subcategory: ""
description: |-
  
---

# teamcity_global_settings (Resource)

## Example Usage

```terraform
resource "teamcity_global_settings" "global" {
  root_url = "https://teamcity"
  encryption = {
    key = base64encode(random_id.key.b64_url)
  }
}
```

## Schema

### Optional

- `artifact_directories` (String) New-line delimited. Default: `system/artifacts`
- `root_url` (String) Server URL. Default: `"http://localhost:8111"`
- `max_artifact_size` (Number) Maximum build artifact file size. Default: `300 MB`
- `max_artifact_number` (Number) Maximum number of artifacts per build. Default: `1000`
- `default_execution_timeout` (Number) Default build execution timeout. In minutes, default: `0`
- `default_vcs_check_interval` (Number) Default VCS changes check interval. In seconds, default: `60`
- `enforce_default_vcs_check_interval` (Boolean) Enforce this value as a minimum for all VCS Roots. Default: `false`
- `default_quiet_period` (Number) Default VCS trigger quiet period. In seconds, default: `60`


- `encryption` (Attributes) Use custom encryption key (see [below for nested schema](#nestedatt--encryption))
- `artifacts_domain_isolation` (Attributes) Artifacts Domain isolation protection (see [below for nested schema](#nestedatt--artifacts_domain_isolation))

<a id="nestedatt--encryption"></a>
### Nested Schema for `encryption`

Required:

- `key` (String, Sensitive) 128 bit key encoded with Base64

<a id="nestedatt--artifacts_domain_isolation"></a>
### Nested Schema for `artifacts_domain_isolation`

Required:

- `artifacts_url` (String) a URL to serve build artifacts from. The URL must be different from the Server URL

## Import

```terraform
import {
  to = teamcity_global_settings.global
  id = "any value"
}
```
