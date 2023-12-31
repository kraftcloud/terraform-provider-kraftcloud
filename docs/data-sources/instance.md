---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "kraftcloud_instance Data Source - terraform-provider-kraftcloud"
subcategory: ""
description: |-
  Provides state information about a KraftCloud instance.
---

# kraftcloud_instance (Data Source)

Provides state information about a KraftCloud instance.

## Example Usage

```terraform
data "kraftcloud_instance" "example" {
  uuid = "550e8400-e29b-41d4-a716-446655440000"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `uuid` (String) Unique identifier of the [instance](https://docs.kraft.cloud/002-rest-api-v1-instances.html)

### Read-Only

- `args` (List of String)
- `boot_time_us` (Number)
- `created_at` (String)
- `env` (Map of String)
- `fqdn` (String)
- `image` (String)
- `memory_mb` (Number)
- `name` (String)
- `network_interfaces` (Attributes List) (see [below for nested schema](#nestedatt--network_interfaces))
- `private_fqdn` (String)
- `private_ip` (String)
- `service_group` (Attributes) (see [below for nested schema](#nestedatt--service_group))
- `state` (String)

<a id="nestedatt--network_interfaces"></a>
### Nested Schema for `network_interfaces`

Read-Only:

- `mac` (String)
- `name` (String)
- `private_ip` (String)
- `uuid` (String)


<a id="nestedatt--service_group"></a>
### Nested Schema for `service_group`

Read-Only:

- `name` (String)
- `services` (Attributes List) (see [below for nested schema](#nestedatt--service_group--services))
- `uuid` (String)

<a id="nestedatt--service_group--services"></a>
### Nested Schema for `service_group.services`

Read-Only:

- `destination_port` (Number)
- `handlers` (Set of String)
- `port` (Number)
