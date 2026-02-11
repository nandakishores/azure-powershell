# Upcoming breaking changes in Azure PowerShell

The breaking changes listed in this article are planned for the next major release of the Az
PowerShell module unless otherwise noted. Per our
[Support lifecycle](azureps-support-lifecycle.md), breaking changes in Azure PowerShell occur twice
a year with major versions of the Az PowerShell module.

Preview modules are not included in this list. Read more about [module version types](azureps-support-lifecycle.md#module-version-types).

## Az.Network

### `Invoke-AzFirewallPacketCapture`

- Cmdlet breaking-change will happen to all parameter sets
  - The cmdlet is being deprecated. There will be no replacement for it.
  - This change is expected to take effect from Az.Network version: Az.Network: 8.0.0 and Az version: Az: 15.0.0

## Az.Resources

### `Get-AzRoleDefinition`

- Cmdlet breaking-change will happen to all parameter sets
  - The output type PSRoleDefinition is changing. The flattened properties 'Actions', 'NotActions', 'DataActions', 'NotDataActions', 'Condition', and 'ConditionVersion' are being removed. Use 'Permissions[n].Actions', 'Permissions[n].DataActions', etc. instead to access the full permission structure with per-permission conditions.
  - This change is expected to take effect from Az.Resources version: 10.0.0 and Az version: 16.0.0

### `Get-AzRoleManagementPolicy`

- Cmdlet breaking-change will happen to all parameter sets
  - The output type 'Microsoft.Azure.PowerShell.Cmdlets.Resources.Authorization.Models.IRoleManagementPolicy' is changing
  - The following properties in the output type are being deprecated : 'EffectiveRule[]' 'Rule[]'
  - The following properties are being added to the output type : 'List[EffectiveRule]' 'List[Rule]'
  - This change will take effect on '11/3/2025'- The change is expected to take effect from Az version : '15.0.0'
  - The change is expected to take effect in 'Az.Resources' from version : '9.0.0'

### `New-AzRoleDefinition`

- Cmdlet breaking-change will happen to all parameter sets
  - The -InputFile JSON format and -Role parameter are changing. The flattened properties 'Actions', 'NotActions', 'DataActions', 'NotDataActions' at the root level are being replaced by a 'Permissions' array. Each permission object contains 'Actions', 'NotActions', 'DataActions', 'NotDataActions', 'Condition', and 'ConditionVersion' properties. The output type PSRoleDefinition is also changing accordingly.
  - This change is expected to take effect from Az.Resources version: 10.0.0 and Az version: 16.0.0

### `Remove-AzRoleDefinition`

- Cmdlet breaking-change will happen to all parameter sets
  - The -InputObject parameter type PSRoleDefinition is changing. The flattened properties 'Actions', 'NotActions', 'DataActions', 'NotDataActions', 'Condition', 'ConditionVersion' are being replaced by a 'Permissions' array containing permission objects with these properties. The output when using -PassThru is also changing accordingly.
  - This change is expected to take effect from Az.Resources version: 10.0.0 and Az version: 16.0.0

### `Set-AzRoleDefinition`

- Cmdlet breaking-change will happen to all parameter sets
  - The -InputFile JSON format and -Role parameter are changing. The flattened properties 'Actions', 'NotActions', 'DataActions', 'NotDataActions' at the root level are being replaced by a 'Permissions' array. Each permission object contains 'Actions', 'NotActions', 'DataActions', 'NotDataActions', 'Condition', and 'ConditionVersion' properties. The output type PSRoleDefinition is also changing accordingly.
  - This change is expected to take effect from Az.Resources version: 10.0.0 and Az version: 16.0.0

### `Update-AzRoleManagementPolicy`

- Cmdlet breaking-change will happen to all parameter sets
  - The output type 'Microsoft.Azure.PowerShell.Cmdlets.Resources.Authorization.Models.IRoleManagementPolicy' is changing
  - The following properties in the output type are being deprecated : 'EffectiveRule[]' 'Rule[]'
  - The following properties are being added to the output type : 'List[EffectiveRule]' 'List[Rule]'
  - This change will take effect on '11/3/2025'- The change is expected to take effect from Az version : '15.0.0'
  - The change is expected to take effect in 'Az.Resources' from version : '9.0.0'

- Parameter breaking-change will happen to parameter set `UpdateAzRoleManagementPolicy_UpdateExpanded`
  - `-Rule`
    - The parameter : 'Rule' is changing.
    The type of the parameter is changing from 'Array' to 'List'.
    - This change will take effect on '11/3/2025'- The change is expected to take effect from Az version : '15.0.0'
    - The change is expected to take effect in 'Az.Resources' from version : '9.0.0'

- Parameter breaking-change will happen to parameter set `UpdateAzRoleManagementPolicy_UpdateViaIdentityExpanded`
  - `-Rule`
    - The parameter : 'Rule' is changing.
    The type of the parameter is changing from 'Array' to 'List'.
    - This change will take effect on '11/3/2025'- The change is expected to take effect from Az version : '15.0.0'
    - The change is expected to take effect in 'Az.Resources' from version : '9.0.0'
