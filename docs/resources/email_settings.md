---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "teamcity_email_settings Resource - terraform-provider-teamcity"
subcategory: ""
description: |-
  
---

# teamcity_email_settings (Resource)

## Example Usage

```terraform
resource "teamcity_email_settings" "email" {
  enabled = true
  host = "mail"
  port = 587
  from = "TeamCity"
  login = "teamcity"
  password = "password"
  secure_connection = "STARTTLS"
}
```

## Schema

### Required

- `enabled` (Boolean)
- `host` (String)
- `port` (Number)
- `from` (String)
- `login` (String)
- `password` (String, Sensitive)
- `secure_connection` (String) Values: `NONE`, `STARTTLS`, `SSL`

## Import

```terraform
import {
  to = teamcity_email_settings.email
  id = "any value"
}
```
