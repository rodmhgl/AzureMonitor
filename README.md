## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_azurerm"></a> [azurerm](#requirement\_azurerm) | >= 3.71.0 |
| <a name="requirement_azurerm"></a> [azurerm](#requirement\_azurerm) | >= 3.71.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_azurerm"></a> [azurerm](#provider\_azurerm) | >= 3.71.0 >= 3.71.0 |
| <a name="provider_random"></a> [random](#provider\_random) | n/a |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [azurerm_eventhub.eh](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/eventhub) | resource |
| [azurerm_eventhub_namespace.ehnamespace](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/eventhub_namespace) | resource |
| [azurerm_log_analytics_workspace.law](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/log_analytics_workspace) | resource |
| [azurerm_storage_account.sa](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/storage_account) | resource |
| [random_integer.rng](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/integer) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_eventhub_auto_inflate"></a> [eventhub\_auto\_inflate](#input\_eventhub\_auto\_inflate) | (Optional)Eventhub auto inflate settings | `bool` | `false` | no |
| <a name="input_eventhub_capacity"></a> [eventhub\_capacity](#input\_eventhub\_capacity) | (Optional)Eventhub partition capacity if sku is Standard | `number` | `2` | no |
| <a name="input_eventhub_dedicated_cluster"></a> [eventhub\_dedicated\_cluster](#input\_eventhub\_dedicated\_cluster) | (Optional)Eventhub dedicated cluster id | `string` | `null` | no |
| <a name="input_eventhub_message_retention"></a> [eventhub\_message\_retention](#input\_eventhub\_message\_retention) | (Optional)Eventhub throughput if auto inflate is set to true | `number` | `1` | no |
| <a name="input_eventhub_network_rules"></a> [eventhub\_network\_rules](#input\_eventhub\_network\_rules) | Network rules restricting access to the event hub. | <pre>object({<br>    trusted_service_access_enabled = bool<br>    ip_rules                       = list(string)<br>    subnet_ids                     = list(string)<br>  })</pre> | `null` | no |
| <a name="input_eventhub_parition_count"></a> [eventhub\_parition\_count](#input\_eventhub\_parition\_count) | (Optional) Eventhub partition count | `number` | `4` | no |
| <a name="input_eventhub_required"></a> [eventhub\_required](#input\_eventhub\_required) | (Optional) is eventhub required? | `string` | `false` | no |
| <a name="input_eventhub_sku"></a> [eventhub\_sku](#input\_eventhub\_sku) | (Optional) sku for the eh, default is basic | `string` | `"Basic"` | no |
| <a name="input_eventhub_status"></a> [eventhub\_status](#input\_eventhub\_status) | (Optional)Eventhub status | `string` | `"Active"` | no |
| <a name="input_eventhub_throughput"></a> [eventhub\_throughput](#input\_eventhub\_throughput) | (Optional)Eventhub throughput if auto inflate is set to true | `number` | `null` | no |
| <a name="input_eventhub_zone_redundant"></a> [eventhub\_zone\_redundant](#input\_eventhub\_zone\_redundant) | (Optional)Eventhub partition capacity if sku is Standard | `bool` | `false` | no |
| <a name="input_location"></a> [location](#input\_location) | (Required) region of the logging module | `string` | n/a | yes |
| <a name="input_log_analytics_workspace_daily_quota"></a> [log\_analytics\_workspace\_daily\_quota](#input\_log\_analytics\_workspace\_daily\_quota) | (Optional) Log analytics workspace daily quota in GB | `number` | `-1` | no |
| <a name="input_log_analytics_workspace_ingestion"></a> [log\_analytics\_workspace\_ingestion](#input\_log\_analytics\_workspace\_ingestion) | (Optional) Log analytics workspace ingestion over the internet | `bool` | `true` | no |
| <a name="input_log_analytics_workspace_query"></a> [log\_analytics\_workspace\_query](#input\_log\_analytics\_workspace\_query) | (Optional) Log analytics workspace query over the internet | `bool` | `true` | no |
| <a name="input_log_analytics_workspace_reservation"></a> [log\_analytics\_workspace\_reservation](#input\_log\_analytics\_workspace\_reservation) | (Optional) Log analytics workspace reservation if sku is set to CapacityReservation | `number` | `null` | no |
| <a name="input_log_analytics_workspace_retention"></a> [log\_analytics\_workspace\_retention](#input\_log\_analytics\_workspace\_retention) | (Optional) retention for the law, default is 30 | `number` | `30` | no |
| <a name="input_log_analytics_workspace_sku"></a> [log\_analytics\_workspace\_sku](#input\_log\_analytics\_workspace\_sku) | (Optional) sku for the law, default is PerGB2018 | `string` | `"PerGB2018"` | no |
| <a name="input_name"></a> [name](#input\_name) | (Required) Name of the logging module | `string` | n/a | yes |
| <a name="input_resource_group_name"></a> [resource\_group\_name](#input\_resource\_group\_name) | (Required) rg of the logging module | `string` | n/a | yes |
| <a name="input_storage_account_access_tier"></a> [storage\_account\_access\_tier](#input\_storage\_account\_access\_tier) | (Optional) Storage account access tier | `string` | `"Cool"` | no |
| <a name="input_storage_account_kind"></a> [storage\_account\_kind](#input\_storage\_account\_kind) | (Optional) Storage account kind | `string` | `"StorageV2"` | no |
| <a name="input_storage_account_replication_type"></a> [storage\_account\_replication\_type](#input\_storage\_account\_replication\_type) | (Optional) Storage account replication type | `string` | `"LRS"` | no |
| <a name="input_storage_account_required"></a> [storage\_account\_required](#input\_storage\_account\_required) | (Optional) is storage account required? | `string` | `false` | no |
| <a name="input_storage_account_tier"></a> [storage\_account\_tier](#input\_storage\_account\_tier) | (Optional) tier for the sa, default is standard | `string` | `"Standard"` | no |
| <a name="input_tags"></a> [tags](#input\_tags) | (Required) map of tags for the logging module | `map(any)` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_eh_out"></a> [eh\_out](#output\_eh\_out) | n/a |
| <a name="output_ehnamespace_out"></a> [ehnamespace\_out](#output\_ehnamespace\_out) | n/a |
| <a name="output_law_out"></a> [law\_out](#output\_law\_out) | n/a |
| <a name="output_sa_out"></a> [sa\_out](#output\_sa\_out) | n/a |
