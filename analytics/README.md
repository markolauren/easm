# Defender EASM Sentinel analytics rule
v0.03b ("works in my computer")

In order to use the analytics rule you need to configure Defender EASM "data connections" / export to your Log Analytics / Sentinel workspace: https://learn.microsoft.com/en-us/azure/external-attack-surface-management/data-connections

### Use case
- Detect new High severity observations which are not present in earlier EASM snapshots

### Setup
- Download the new_easm_finding_high_severity.json
- In Sentinel Analytics - Import - Point to new_easm_finding_high_severity.json

### Configure (optional)
- If you're exporting multiple EASM workspaces to your Sentinel, you need to create separate analytics rules for them (once imported, "clone")
  - Uncomment line 2 and specify your EASM workspace name: "//let easmworkspace = "yourEasmWorkspaceName";"
  - Uncomment lines 6 & 15: "//| where WorkspaceName_s == easmworkspace"
