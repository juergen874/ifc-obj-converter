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
