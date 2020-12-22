# Action Rules

Action rules can be used to Suppress or set additional actions for Azure Monitor alerts.

For more info see the [Microsoft Docs](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/alerts-action-rules?tabs=portal)

## Suppression parameter examples

### actionrule.json

This is the ARM template you can use to deploy the Action Rules.

### parameters.always-suppress-vms-tst.json

This parameter file can be used to **always** suppress alerts that are scoped to the **subscription** and meet the conditions below:

- Monitor Condition: _Fired_ or _Resolved_
- Resource Type: _Virtual Machines_
- Alert Context (Payload) contains: _TST_

### parameters.always-suppress-vms-rg.json

This parameter file can be used to **always** suppress alerts that are scoped to the specified **resourcegroup** and meet the conditions below:

- Monitor Condition: _Fired_ or _Resolved_
- Resource Type: _Virtual Machines_

### parameters.always-suppress-vms-tst.json

This parameter file can be used to **always** suppress alerts that are scoped to the specified **resource** and meet the conditions below:

- Monitor Condition: _Fired_ or _Resolved_
- Resource Type: _Virtual Machines_
- Alert Context (Payload) contains: _TST_

### parameters.weekly-suppress-vms-acc-friday.json

This parameter file can be used to suppress alerts on a **weekly** basis that are scoped to the **subscription** and meet the conditions below:

- Monitor Condition: _Fired_ or _Resolved_
- Resource Type: _Virtual Machines_
- Alert Context (Payload) contains: _ACC_
- Day equals: _Friday_
- Time between: _17:00:00 and 23:00:00 (UTC)_
- Date between: _12/12/2020 and 12/12/2022_

### parameters.weekly-suppress-vms-acc-weekend.json

This parameter file can be used to suppress alerts on a **weekly** basis that are scoped to the **subscription** and meet the conditions below:

- Monitor Condition: _Fired_ or _Resolved_
- Resource Type: _Virtual Machines_
- Alert Context (Payload) contains: _ACC_
- Day equals: _Saturday and/or Sunday_
- Time between: _23:00:00 and 23:59:59 (UTC)_
- Date between: _12/12/2020 and 12/12/2022_

## Action Group parameters

### parameters.always-actiongroup-vms-tst-sev01.json

This parameter file can be used to **always** action alerts that are scoped to the **subscription** and meet the conditions below:

- Alert Severity: _Sev0_
- Monitor Condition: _Fired_ or _Resolved_
- Resource Type: _Virtual Machines_
- Alert Context (Payload) contains: _TST_

### parameters.always-actiongroup-sev01.json

This parameter file can be used to **always** action alerts that are scoped to the **subscription** and meet the conditions below:

- Alert Severity: _Sev0_