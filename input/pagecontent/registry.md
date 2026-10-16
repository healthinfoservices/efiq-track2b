SIU messages identify organisations and namespaces by short codes (for example `SIMHOSP` in PID-3.4 or AIL-3.4). AU Core needs more than a code in several places, so the service reads a JSON registry (`config/au-registry.json`, or the path in the `AU_REGISTRY` environment variable).

| Registry section | Keyed by | Used for |
|---|---|---|
| `assigningAuthorities.{code}.name` | PID-3.4 | `identifier.assigner.display` on MRN / patient internal identifiers (required by those AU Base identifier profiles) |
| `assigningAuthorities.{code}.systems.{type}` | PID-3.4 + PID-3.5 | The identifier system URI, e.g. the hospital's MRN namespace |
| `facilities.{code}.name` | AIL-3.4 | `Organization.name` (required by AU Core Organization) |
| `facilities.{code}.hpio` | AIL-3.4 | HPI-O identifier (validated: 16 digits, prefix 800362, Luhn) |
| `facilities.{code}.address` | AIL-3.4 | `Organization.address` |
| `locationTypes.{code}` | AIL-4.1 | A Coding from ServiceDeliveryLocationRoleType - AU Extended |
{:.grid}

Keys starting with `_` are ignored, so they can hold comments and examples.

The sample registry in this project holds simulated values only. Without a registry entry the service still produces conformant resources, using fallbacks and logging a warning: an MRN without an assigner (valid as a plain identifier), and the facility code as the Organization name.
