# Defender EASM Sentinel Workbook

In order to use the workbook you need to configure Defender EASM "data connections" / export to your Log Analytics / Sentinel workspace: https://learn.microsoft.com/en-us/azure/external-attack-surface-management/data-connections

Deploy Workbook:
1. Copy raw json template
2. "Add workbook" in Sentinel > Edit > Advanced editor
3. Replace the template with the workbook json > Apply
4. Save workbook

Usage:
1. Choose subscrption/workspace where you've configured the EASM export
2. Choose EASM workspace name (in case you're exporting multiple workspaces)
3. Define TimeRange
4. Enjoy the views

Views:
1. All observations - drill into all observations by selecting severity level, observation type, asset
2. New observations - only new observations from the latest snapshot/export (which were not identified in earlier snapshots)
3. High/Medium/Low - investigate observations by severity
4. Asset Risk - observations based on latest snapshot (high,med,low) and their cumulative risk
5. Vulnerabilities & Exploits - correlates web component vulnerabilities and if they are exploitable (correlates asset last seen to web component last seen value, only when those match)



