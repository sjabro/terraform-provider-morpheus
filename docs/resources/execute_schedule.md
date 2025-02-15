---
page_title: "morpheus_execute_schedule Resource - terraform-provider-morpheus"
subcategory: ""
description: |-
  Provides an execution schedule resource
---

# morpheus_execute_schedule

Provides an execution schedule resource

## Example Usage

```terraform
resource "morpheus_execute_schedule" "tf_example_execute_schedule" {
  name        = "Run daily at 7 AM"
  description = "This schedule runs daily at 7 AM Mountain Time"
  enabled     = false
  time_zone   = "America/Denver"
  schedule    = "7 0 * * *"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **name** (String) The name of the execute schedule
- **schedule** (String) The cron style syntax for the scheduled execution
- **time_zone** (String) The time zone used for scheduling

### Optional

- **description** (String) The description of the execute schedule
- **enabled** (Boolean) Whether the execute schedule is enabled

### Read-Only

- **id** (String) The ID of the execute schedule

## Import

Import is supported using the following syntax:

```shell
terraform import morpheus_execute_schedule.tf_example_execute_schedule 1
```
