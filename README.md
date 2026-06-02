# VeloPlan — QGIS plugin (auto-update channel)

Public distribution of the **VeloPlan / FiberNetworkAutomation** QGIS plugin.

## One-time setup (per machine)
QGIS → **Plugins → Manage and Install Plugins → Settings → Add…** a plugin repository:
- **Name:** VeloPlan
- **URL:** `https://raw.githubusercontent.com/JohanVelo/veloplan-qgis/main/plugins.xml`

Then **Plugins → All** → search **FiberNetworkAutomation** → Install. QGIS will show **Upgrade**
automatically whenever a new version is published here.

> AI/detection tools require the team Python venv (torch / SAM2 / geopandas).

## Manual install (alternative)
Download `FiberNetworkAutomation.zip` and use **Install from ZIP**.
