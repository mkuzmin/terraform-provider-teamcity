---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "teamcity_cleanup Resource - terraform-provider-teamcity"
subcategory: ""
description: |-
  
---

# teamcity_cleanup (Resource)

## Example Usage

```terraform
resource "teamcity_cleanup" "settings" {
  enabled = true
  max_duration = 0

  daily = {
    hour = 2
    minute = 0
  }
}
```

## Schema

### Required

- `enabled` (Boolean)
- `max_duration` (Number) Stop clean-up if it takes longer than (in minutes)

### Optional

- `daily` (Attributes) (see [below for nested schema](#nestedatt--daily))
- `cron` (Attributes) (see [below for nested schema](#nestedatt--cron))

<a id="nestedatt--daily"></a>
### Nested Schema for `daily`

Required:

- `hour` (Number)
- `minute` (Number)

<a id="nestedatt--cron"></a>
### Nested Schema for `cron`

#### Example Usage

```terraform
cron = {
    minute = 15
    hour = 2
    day = 2
    month = "*"
    day_week = "?"
}
```

Required:

- `minute` (String) Minutes
- `hour` (String) Hours
- `day` (String) Day of month
- `month` (String) Month
- `day_week` (String) Day of week

## Import

```terraform
import {
  to = teamcity_cleanup.settings
  id = "any value"
}
```
