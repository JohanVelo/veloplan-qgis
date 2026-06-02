# Install VeloPlan in QGIS (team)

## Fastest — one paste (QGIS Python Console)
**Plugins → Python Console**, paste this, press Enter:

```python
from qgis.core import QgsSettings
import pyplugin_installer
s = QgsSettings()
s.setValue('app/plugin_repositories/VeloPlan/url',
           'https://raw.githubusercontent.com/JohanVelo/veloplan-qgis/main/plugins.xml')
s.setValue('app/plugin_repositories/VeloPlan/authcfg', '')
s.setValue('app/plugin_repositories/VeloPlan/enabled', True)
pi = pyplugin_installer.instance(); pi.reloadAndExportData(); pi.fetchAvailablePlugins(True)
print('VeloPlan repo added — Plugins → search FiberNetworkAutomation → Install')
```

Then **Plugins → Manage and Install Plugins → All** → search **FiberNetworkAutomation** → **Install**.
From then on QGIS shows **Upgrade** automatically when a new version ships.

## Manual (no console)
Plugins → Manage and Install Plugins → **Settings → Add…**
- Name: `VeloPlan`
- URL: `https://raw.githubusercontent.com/JohanVelo/veloplan-qgis/main/plugins.xml`

→ **All** tab → search **FiberNetworkAutomation** → Install.

## Using it
Everything is under the **VeloPlan** menu in the QGIS menu bar:
AI Mapping (New Project wizard, AI Detect/Erven/AutoDetect, **Erven Studio**) ·
Labelling · FT Pipeline (FT1–7) · QA & Output · Tools · Automation Pipeline (BOM, OES, …).

> AI/detection tools need the team Python venv (torch / SAM2 / geopandas).
