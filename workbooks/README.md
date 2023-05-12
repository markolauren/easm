# Defender EASM Sentinel Workbook

Ever wondered how your EASM observations trend? What was the status last week? or before that?


In order to use the workbook you need to configure Defender EASM "data connections" / export to your Log Analytics / Sentinel workspace: https://learn.microsoft.com/en-us/azure/external-attack-surface-management/data-connections

Deploy:
1. Copy raw json template
2. "Add workbook" in Sentinel > Edit > Advanced editor
3. Replace the template with the workbook json > Apply
4. Save workbook

Usage:
1. Choose subscription/workspace where you've configured the EASM export
2. Choose EASM workspace name (in case you're exporting multiple workspaces)
3. Define Time Range
4. Enjoy the views

Views:
1. All observations - drill into all observations by selecting severity level, observation type, asset
2. New observations - only new observations from the latest snapshot/export (which were not identified in earlier snapshots)
3. High/Medium/Low - investigate observations by severity
4. Asset Risk - observations based on latest snapshot (high,med,low) and their cumulative risk
5. Vulnerabilities & Exploits - correlates web component vulnerabilities and if they are exploitable (correlates asset last seen to web component last seen value, only when those match)

> NOTICE: if you've just configured the export and there isn't many snapshots yet - the graphs do not have much data to populate yet!

# Examples

All observations:

![image](https://github.com/markolauren/easm/assets/133347791/1636fb5c-ffdb-4cbf-83e7-7d4bf896ce27)

Asset risk:

![image](https://github.com/markolauren/easm/assets/133347791/d30c54a2-30cc-45b3-817d-d6d907885140)

Vulnerabilities & Exploits:

![image](https://github.com/markolauren/easm/assets/133347791/76f434e3-2807-4df1-865b-774bbd02b7a4)
