<p align="center">
  <b><a href="#-english">🇬🇧 English</a></b> &nbsp;•&nbsp; <b><a href="#-deutsch">🇩🇪 Deutsch</a></b>
</p>

---

<a name="-english"></a>
# 🏢 IFC ➔ OBJ 3D Converter & Viewer (DIALux evo Optimized)

> **High-performance, pure client-side IFC-to-Wavefront-OBJ converter with integrated interactive 3D WebGL preview.**  
> 100% offline-capable, privacy-friendly, and runs directly in your browser with zero installations or server uploads.

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-brightgreen?style=flat-square&logo=github)](https://juergen874.github.io/ifc-obj-converter/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero%20(Pure%20JS)-orange?style=flat-square)](#)
[![DIALux evo Ready](https://img.shields.io/badge/DIALux%20evo-Ready-blue?style=flat-square)](#)

---

## 🌐 Live Web App & Demo

👉 **[Open directly in browser (GitHub Pages)](https://juergen874.github.io/ifc-obj-converter/)**

---

## 💡 Why this Converter?

In corporate environments and on enterprise PCs, lighting designers, architects, and engineers frequently encounter two major hurdles:

1. **Strict Security Policies (EDR / Antivirus / No Admin Rights):**  
   CLI tools such as `IfcConvert.exe` require downloading untrusted executables, which are often immediately blocked or quarantined by corporate antivirus software.
2. **IFC4 Mesh Issues in DIALux evo:**  
   Modern CAD tools (e.g., SketchUp 2025, Revit) often export IFC4 in *Reference View 1.2* with triangulated surface meshes (`IfcTriangulatedFaceSet`) instead of traditional BREP solids. DIALux evo frequently fails to interpret these as building elements – **however, importing `.obj` files as 3D objects works seamlessly**.

**The Solution:**  
This web app runs **100% inside your browser's secure sandbox** (Edge, Chrome, Firefox). It requires no installation, no admin privileges, triggers **no antivirus alerts**, and never sends sensitive corporate data to external servers.

---

## ✨ Features & Highlights

- **🔒 100% Client-Side & Privacy First:**
  - All IFC parsing and 3D mesh computations run locally in browser memory.
  - Fully offline-capable (works without an internet connection via `file:///...`).
- **🎯 Specifically Optimized for DIALux evo:**
  - **Auto-Centering:** Centers the building footprint at ($X=0, Y=0$) and grounds the bottom of the foundation slab at $Z=0$. When imported into DIALux evo, the model lands right in the workspace rather than kilometers away at UTM/project coordinates.
  - **Unit Scaling:** Automatically detects length units from the IFC header (e.g., millimeters ➔ meters).
  - **Material Export (.mtl):** Generates corresponding material and color definitions (e.g., reinforced concrete, structural steel, surface finishes).
- **🕹️ Interactive 3D WebGL Viewer:**
  - **Rotate:** Left-click + drag
  - **Pan:** Right-click / Shift + Left-click + drag
  - **Zoom:** Mouse wheel / pinch-to-zoom
  - **Render Modes:** Smooth solid shading with directional lighting or wireframe.
  - **Real-Time Diagnostics:** Displays component count, triangles, vertices, and bounding box dimensions ($W \times D \times H$ in meters).
- **⚡ Robust STEP/IFC Parser:**
  - Supports multiline records, ISO 10303-21 STEP syntax, and complex transformation hierarchies (`IfcLocalPlacement` ➔ `IfcAxis2Placement3D`).
  - Handles truncated numeric IFC literals (e.g., `0.`, `-80.` without explicit decimal digits).

---

## 🚀 Quick Start: Import IFC into DIALux evo

1. Open the [Web App](https://juergen874.github.io/ifc-obj-converter/) or local `ifc_obj_converter.html`.
2. **Drag & Drop** your `.ifc` file into the upload zone.
3. Inspect the model in the **3D preview** and verify bounding dimensions.
4. Click **💾 Download OBJ File (.obj)** and optionally **🎨 Download Material File (.mtl)**.
5. In **DIALux evo**:
   - Navigate to **Construction** ➔ **Furniture and objects** in the left menu.
   - Click **Import 3D object** (or drag the `.obj` file directly into the DIALux 3D viewport).
   - The building appears scaled, aligned, and ready for lighting calculation.

---

## 🛠️ Supported Formats & Entities

| Category | Supported IFC Entities |
| :--- | :--- |
| **Geometry** | `IfcTriangulatedFaceSet`, `IfcCartesianPointList3D`, `IfcCartesianPoint`, `IfcDirection` |
| **Placement** | `IfcLocalPlacement`, `IfcAxis2Placement3D` (nested transformation matrices) |
| **Elements** | `IfcColumn`, `IfcBeam`, `IfcSlab`, `IfcWall`, `IfcFooting`, `IfcBuildingElementProxy`, `IfcDoor`, `IfcWindow`, `IfcStair`, `IfcRoof`, `IfcMember`, `IfcPlate` |
| **Materials** | `IfcStyledItem`, `IfcSurfaceStyle`, `IfcSurfaceStyleRendering`, `IfcColourRgb` |
| **CAD Sources** | Trimble SketchUp, Autodesk Revit, Graphisoft ArchiCAD, Nemetschek Allplan, and more. |

---

## 📦 Offline Usage

Download [`ifc_obj_converter.html`](ifc_obj_converter.html) and open it directly:
1. Double-click `ifc_obj_converter.html` in Chrome, Microsoft Edge, or Firefox.
2. Ready! Runs entirely without network connectivity.

---

## 📄 License

Licensed under the [MIT License](LICENSE) – free for private and commercial use.

---
---

<a name="-deutsch"></a>
# 🇩🇪 Deutsche Beschreibung

# 🏢 IFC ➔ OBJ 3D-Konverter & Viewer (DIALux evo optimiert)

> **High-Performance, rein clientseitiger IFC-zu-Wavefront-OBJ-Konverter mit integrierter interaktiver 3D-WebGL-Vorschau.**  
> 100% offline-fähig, datenschutzfreundlich und ohne jegliche Installation oder Server-Uploads direkt im Browser nutzbar.

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-brightgreen?style=flat-square&logo=github)](https://juergen874.github.io/ifc-obj-converter/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero%20(Pure%20JS)-orange?style=flat-square)](#)
[![DIALux evo Ready](https://img.shields.io/badge/DIALux%20evo-Ready-blue?style=flat-square)](#)

---

## 🌐 Live Web-App & Demo

👉 **[Direkt im Browser öffnen (GitHub Pages)](https://juergen874.github.io/ifc-obj-converter/)**

---

## 💡 Warum dieser Konverter?

In gesicherten Unternehmensnetzwerken und auf Firmen-PCs stoßen Lichtplaner, Architekten und Ingenieure häufig auf zwei Hürden:

1. **Strenge Sicherheitsrichtlinien (EDR / Antivirus / Keine Admin-Rechte):**  
   Kommandozeilen-Tools wie `IfcConvert.exe` erfordern Downloads ungesicherter Binärdateien, die von Firmen-Virenscannern sofort blockiert oder unter Quarantäne gestellt werden.
2. **IFC4-Mesh-Probleme in DIALux evo:**  
   Neuere CAD-Tools (z. B. SketchUp 2025, Revit) exportieren oft IFC4 im *Reference View 1.2* mit tessellierten Dreiecksnetzen (`IfcTriangulatedFaceSet`) statt klassischer BREP-Festkörper. DIALux evo kann diese IFC-Dateien oft nicht direkt als Gebäude interpretieren – **unterstützt jedoch den Import von `.obj`-Dateien als 3D-Objekt hervorragend**.

**Die Lösung:**  
Diese Web-App läuft **zu 100% in der sicheren Sandbox Ihres normalen Browsers** (Edge, Chrome, Firefox). Sie benötigt keine Installation, keine Administratorrechte, löst **keinen Virenscanner-Alarm** aus und sendet keine Unternehmensdaten ins Internet.

---

## ✨ Features & Funktionen

- **🔒 100% Client-Side & Datenschutz:**
  - Alle IFC-Parsing- und 3D-Mesh-Berechnungen laufen lokal im JavaScript-Speicher des Browsers.
  - Funktioniert vollständig offline (auch ohne Internetverbindung über `file:///...`).
- **🎯 Speziell für DIALux evo optimiert:**
  - **Auto-Zentrierung:** Setzt den Nullpunkt auf das Zentrum des Gebäudes ($X=0, Y=0$) und platziert die Unterkante der Bodenplatte exakt auf $Z=0$. Dadurch landet das Modell beim Import in DIALux evo direkt im Arbeitsbereich und nicht kilometerweit entfernt bei UTM-/Werkskoordinaten.
  - **Einheiten-Skalierung:** Erkennt automatisch Längeneinheiten aus dem IFC-Header (z. B. Millimeter ➔ Meter).
  - **Material-Export (.mtl):** Generiert passende Material- und Farbdefinitionen (z. B. Stahlbeton, Stahl, Oberflächenfarben).
- **🕹️ Interaktiver 3D-WebGL-Viewer:**
  - **Drehen:** Linksklick + Ziehen
  - **Verschieben (Pan):** Rechtsklick / Umschalt + Linksklick + Ziehen
  - **Zoomen:** Mausrad
  - **Modus-Umschaltung:** Solide Schattierung mit Direktlicht oder Drahtgitter (Wireframe).
  - **Echtzeit-Statistiken:** Anzeige von Bauteilanzahl, Dreiecken, Vertices und Bounding-Box-Maßen ($B \times T \times H$ in Metern).
- **⚡ Robuster STEP/IFC-Parser:**
  - Unterstützt mehrzeilige Datensätze, ISO 10303-21 STEP-Syntax und komplexe Transformations-Hierarchien (`IfcLocalPlacement` ➔ `IfcAxis2Placement3D`).
  - Berücksichtigt verkürzte numerische IFC-Werte (z. B. `0.`, `-80.` ohne Nachkommastelle).

---

## 🚀 Schnellanleitung: IFC in DIALux evo importieren

1. Öffnen Sie die [Web-App](https://juergen874.github.io/ifc-obj-converter/) oder die lokale `ifc_obj_converter.html`.
2. Ziehen Sie Ihre `.ifc`-Datei per **Drag & Drop** in das Upload-Feld.
3. Prüfen Sie das Modell in der **3D-Vorschau** und kontrollieren Sie die Abmessungen.
4. Klicken Sie auf **💾 OBJ-Datei herunterladen (.obj)** und optional auf **🎨 Materialdatei herunterladen (.mtl)**.
5. In **DIALux evo**:
   - Gehen Sie im linken Menü auf **Konstruktion** ➔ **Möbel und Objekte**.
   - Klicken Sie auf **3D-Objekt importieren** (oder ziehen Sie die `.obj`-Datei direkt in die DIALux 3D-Ansicht).
   - Das Gebäude erscheint sofort maßstabsgetreu und einsatzbereit.

---

## 🛠️ Unterstützte Formate & Entitäten

| Kategorie | Unterstützte IFC-Elemente |
| :--- | :--- |
| **Geometrie** | `IfcTriangulatedFaceSet`, `IfcCartesianPointList3D`, `IfcCartesianPoint`, `IfcDirection` |
| **Platzierung** | `IfcLocalPlacement`, `IfcAxis2Placement3D` (verschachtelte Matrix-Multiplikation) |
| **Bauteile** | `IfcColumn`, `IfcBeam`, `IfcSlab`, `IfcWall`, `IfcFooting`, `IfcBuildingElementProxy`, `IfcDoor`, `IfcWindow`, `IfcStair`, `IfcRoof`, `IfcMember`, `IfcPlate` |
| **Materialien** | `IfcStyledItem`, `IfcSurfaceStyle`, `IfcSurfaceStyleRendering`, `IfcColourRgb` |
| **CAD-Quellen** | Trimble SketchUp, Autodesk Revit, Graphisoft ArchiCAD, Nemetschek Allplan, uvm. |

---

## 📦 Lokale Nutzung ohne Internet

Sie können die Datei [`ifc_obj_converter.html`](ifc_obj_converter.html) einfach herunterladen und lokal abspeichern:
1. `ifc_obj_converter.html` per Doppelklick in Chrome, Microsoft Edge oder Firefox öffnen.
2. Fertig! Funktioniert komplett ohne Netzwerkverbindung oder Server.

---

## 📄 Lizenz

Dieses Projekt ist lizenziert unter der [MIT-Lizenz](LICENSE) - frei verwendbar für private und gewerbliche Zwecke.
