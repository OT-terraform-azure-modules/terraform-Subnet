Azure Subnet Terraform module
=====================================

[![Opstree Solutions][opstree_avatar]][opstree_homepage]

[Opstree Solutions][opstree_homepage] 

  [opstree_homepage]: https://opstree.github.io/
  [opstree_avatar]: https://img.cloudposse.com/150x150/https://github.com/opstree.png

Terraform module which creates Subnet on Azure.

These types of resources are supported:

* [Subnet](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/subnet)

Terraform versions
------------------

Terraform 0.13.

Usage
------

```hcl
module "Subnet" {
  source                  = "git::https://github.com/OT-terraform-azure-modules/terraform-Subnet.git"
  subnet_name             = "TerraformSubnet"
  subnet_vnet_name        = "Terraformvnet"
  subnet_address_prefixes = "10.0.1.0/24"
  subnet_rg_name          = "TerraformRG"
}

```



Inputs
------
| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| subnet_name | Name of the subnet | `string` | `"TerraformSubnet"` | yes |
| subnet_address_prefixes | Address prefix to associate with the subnet | `string` | `"10.0.1.0/24"` | no |
| subnet_vnet_name | Virtual Network in which Subnet would be created | `string` | `"Terraformvnet"` | yes |
| subnet_rg_name | Resource Group in which the Subnet would be created | `string` | `"TerraformRG"` | yes |

Output
------
| Name | Description |
|------|-------------|
|subnet_Details |This variable will give all the details of Subnet like RG name, Vnet name, address prefix |

## Related Projects

Check out these related projects. 
* [Subnet Implementation](https://github.com/lakshayarora476/terraform-Subnet-setup)

### Contributors

|  [![Lakshay Arora][lakshay_avatar]][lakshay_homepage]<br/>[Lakshay Arora][lakshay_homepage] |
|---|

  [lakshay_homepage]: https://github.com/lakshayarora476
  [lakshay_avatar]: https://avatars.githubusercontent.com/lakshayarora476

