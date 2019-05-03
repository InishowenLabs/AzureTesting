# Standard IT Tags Policy Initiative

Specify cost Center tag and product name tag

## Try with PowerShell

````powershell
$policydefinitions = "https://github.com/InishowenLabs/AzureTesting/blob/master/azurepolicyset.definitions.json"
$policysetparameters = "https://github.com/InishowenLabs/AzureTesting/blob/master/azurepolicyset.parameters.json"

$policyset= New-AzPolicySetDefinition -Name "standard-it-tags" -DisplayName "Central IT - Standard Tag Initiative" -Description "Specify standard tags used by Central IT" -PolicyDefinition $policydefinitions -Parameter $policysetparameters 
 
New-AzPolicyAssignment -PolicySetDefinition $policyset -Name <assignmentname> -Scope <scope>  -instanceCostCenterValue <required value for instance Cost Center tag> -instanceNameValue <required value for instance Name tag>
````
