---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "teamcity_user Resource - terraform-provider-teamcity"
subcategory: ""
description: |-
  
---

# teamcity_user (Resource)

## Example Usage

```terraform
resource "teamcity_user" "test" {
  username = "test"
  password = "test"

  roles = [
    {
      id      = "SYSTEM_ADMIN"
      global  = true
    }
  ]
}
```

## Schema

### Required

- `password` (String, Sensitive)
- `username` (String)

### Optional

- `roles` (Attributes Set) (see [below for nested schema](#nestedatt--roles))

### Read-Only

- `id` (String) The ID of this resource.

<a id="nestedatt--roles"></a>
### Nested Schema for `roles`

Required:

- `id` (String)

Optional:

- `global` (Boolean)
- `project` (String)

## Import

```terraform
import {
  to = teamcity_user.user
  id = "username"
}
```
