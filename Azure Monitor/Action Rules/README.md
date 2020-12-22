# Action Rules

Action rules can be used to Suppress Azure Monitor alerts or add an additional action to them.

## actionrule.json

This is the ARM template you can use to deploy the Action Rules.

### parameters-always-suppress-fired-vms-tst.json

This parameter file can be used to **always** suppress alerts that are scoped to the **subscription** and meet the conditions below:
- Monitor Condition: _Fired_ or _Resolved_
- Resource Type: _Virtual Machines_
- Alert Context (Payload) contains: _TST_

### parameters-always-suppress-fired-vms-rg.json

This parameter file can be used to **always** suppress alerts that are scoped to the specified **resourcegroup** and meet the conditions below:
- Monitor Condition: _Fired_
- Resource Type: _Virtual Machines_

### parameters-always-suppress-fired-vms-tst.json

This parameter file can be used to **always** suppress alerts that are scoped to the specified **resource** and meet the conditions below:
- Monitor Condition: _Fired_
- Resource Type: _Virtual Machines_
- Alert Context (Payload) contains: _TST_

### parameters-weekly-suppress-fired-vms-acc-friday.json

This parameter file can be used to suppress alerts on a **weekly** basis that are scoped to the **subscription** and meet the conditions below:
- Monitor Condition: _Fired_
- Resource Type: _Virtual Machines_
- Alert Context (Payload) contains: _ACC_
- Day equals: _Friday_
- Time between: _17:00:00 and 23:00:00 (UTC)_
- Date between: _12/12/2020 and 12/12/2022_

### parameters-weekly-suppress-fired-vms-acc-weekend.json

This parameter file can be used to suppress alerts on a **weekly** basis that are scoped to the **subscription** and meet the conditions below:
- Monitor Condition: _Fired_
- Resource Type: _Virtual Machines_
- Alert Context (Payload) contains: _ACC_
- Day equals: _Saturday and/or Sunday_
- Time between: _23:00:00 and 23:59:59 (UTC)_
- Date between: _12/12/2020 and 12/12/2022_