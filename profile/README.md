<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/OpenGewerk/.github/main/brand/banner/opengewerk-banner-1280x640-dark.png">
  <img alt="OpenGewerk: Self-hosted CRM &amp; ERP für Handwerksbetriebe" src="https://raw.githubusercontent.com/OpenGewerk/.github/main/brand/banner/opengewerk-banner-1280x640-light.png" width="100%">
</picture>

# OpenGewerk

OpenGewerk ist Open-Source-Software für Handwerksbetriebe und für Betreiber von Gebäuden. Dazu gehören zwei Anwendungen, die auf demselben Fundament aufbauen. Die Handwerkersoftware vereint CRM und ERP in einem Datenmodell, ihr Kernmodul ist Elektro und PV. OpenGewerk Haustechnik ist ein CAFM für das technische Gebäudemanagement.

Beide laufen self-hosted auf eigener Hardware, die Daten bleiben im Betrieb. Oberfläche und Dokumentation sind deutsch. Für Steuerberater ist ein Kanzlei-Hub geplant, der alle Mandanten, die mit der Handwerkersoftware arbeiten, in einer Anwendung bündelt.

## Kein Tarifmodell

OpenGewerk kostet keine Lizenz. Es gibt keine Tarifstufen und keine Nutzerlimits, und niemand hält eine Funktion zurück, um einen höheren Tarif zu verkaufen. Jede Schnittstelle und jede Auswertung steht jedem Betrieb offen, und alles, was die Software kann, liegt im Repository.

Geld kann später mit Leistungen rund um die Software entstehen: Hosting für Betriebe, die nicht selbst hosten wollen, Installation und Migration, Support und Wartung, Schulungen sowie Anbindungen an Messgeräte und Fremdsysteme als Auftragsarbeit. Nötig ist keine davon. Ein Betrieb muss OpenGewerk ohne fremde Hilfe betreiben können, sonst wäre die Beschränkung nur an eine andere Stelle gewandert.

Deshalb wird es keine kommerzielle Fassung und keine bezahlten Erweiterungen geben, auch nicht vom Projekt selbst, und es gibt kein Contributor License Agreement. Die Begründung steht in [Leitentscheidung 9 der Feature-Gliederung](https://github.com/OpenGewerk/opengewerk/blob/main/docs/konzept/Feature-Gliederung.md#0-leitentscheidungen).

## Die Repositories

| Repository | Wofür |
| --- | --- |
| [opengewerk](https://github.com/OpenGewerk/opengewerk) | Die Handwerkersoftware, CRM und ERP in einem und GoBD-konform: Angebot, Regiebericht, Rechnung und E-Rechnung, Zeiterfassung, Plantafel, Prüfprotokolle für Elektro und PV und eine Baustellen-App, die ohne Netz arbeitet. Die Buchhaltung folgt mit Phase 3. |
| [opengewerk-haustechnik](https://github.com/OpenGewerk/opengewerk-haustechnik) | Das CAFM für das technische Gebäudemanagement: Liegenschaften, Räume und Anlagen in einem Datenmodell, Betreiberpflichten als überwachte Fristen, Rundgänge und Prüfungen auch ohne Netz und Nachweise, die sich nicht mehr ändern lassen. Es steht auf demselben Fundament wie die Handwerkersoftware. |
| [opengewerk-kanzlei](https://github.com/OpenGewerk/opengewerk-kanzlei) | Der geplante Hub für Steuerberater. Er bündelt alle OpenGewerk-Mandanten in einer Anwendung, die Daten bleiben dabei beim Mandanten (föderiert). |
| [opengewerk-api-spec](https://github.com/OpenGewerk/opengewerk-api-spec) | Der API-Vertrag zwischen Handwerkersoftware und Kanzlei-Hub: OpenAPI-Definition, JSON-Schemas und Konformitätstests, versioniert nach SemVer. |
| [opengewerk-website](https://github.com/OpenGewerk/opengewerk-website) | Die Website unter [opengewerk.de](https://opengewerk.de), mit Astro als statisches HTML gebaut. |
| [.github](https://github.com/OpenGewerk/.github) | Dieses Profil, die Beitragsregeln, der Verhaltenskodex, die Sicherheitsrichtlinie und die Marke. |

## Stand

Von der Handwerkersoftware sind das Fundament und Phase 1 gebaut, das MVP für den Pilotbetrieb. Die neueste Fassung ist [OpenGewerk 0.7.0](https://github.com/OpenGewerk/opengewerk/releases) vom 03.11.2026. Installiert wird sie über Docker Compose auf eigener Hardware, auf x86_64 wie auf ARM64. Jedes Release bringt signierte Abbilder mit, eingerichtet wird im Browser, und jede Nacht sichert sich die Installation selbst.

Ein Betrieb führt damit Kunden, Objekte, Anlagen und Aufträge und schreibt Angebote, Rechnungen und E-Rechnungen (XRechnung, ZUGFeRD). Auf der Baustelle entstehen Regiebericht und Zeiterfassung, auch ohne Netz, und für Elektro das Stromkreisverzeichnis und das Prüfprotokoll nach DIN VDE 0100-600.

Gebaut wird an Phase 2, dem Kern für Elektro und PV. Der größte Teil davon ist mit 0.7.0 erschienen: die Prüfprotokolle nach DIN VDE 0105-100 und DGUV Vorschrift 3, PV, Netzbetreiber, Lager, Plantafel sowie Abnahme und Mängel. Vor dem produktiven Einsatz fehlen noch die fachliche Abnahme der Regelpakete und ein Praxistest der E-Rechnung bei einem echten Empfänger. Was im Einzelnen fertig ist, steht in [Funktionsumfang und Stand](https://github.com/OpenGewerk/opengewerk/blob/main/docs/funktionsumfang.md).

OpenGewerk Haustechnik kam am 01.10.2026 dazu, als CAFM für alle, die Gebäude betreiben und dafür eigene Haustechniker haben. Dafür wurde das Fundament der Handwerkersoftware in eigene Pakete herausgelöst ([ADR 0010](https://github.com/OpenGewerk/opengewerk/blob/main/docs/adr/0010-fundament-als-pakete.md)). Phase 1, das MVP für den Pilotbetrieb, erschien am 15.10.2026. Phase 2 mit den vollständigen Betreiberpflichten folgte am 21.10.2026 als Fassung 0.2.0, die neueste ist [OpenGewerk Haustechnik 0.2.6](https://github.com/OpenGewerk/opengewerk-haustechnik/releases) vom 05.11.2026. Der Pilotbetrieb, ein Träger mit rund zwanzig Liegenschaften, hat seine bisherige Anwendung abgeschaltet und arbeitet nur noch mit OpenGewerk Haustechnik. Was sie kann, steht in [Funktionsumfang und Stand](https://github.com/OpenGewerk/opengewerk-haustechnik/blob/main/docs/funktionsumfang.md).

Der Kanzlei-Hub ist noch in der Planung. Er baut auf der Buchhaltung der Handwerkersoftware auf, die dort mit Phase 3 kommt. Bis dahin wird der gemeinsame API-Vertrag weitergeführt.

Den vollständigen Funktionsumfang beschreiben die drei Konzepte:

- [Feature-Gliederung der Handwerkersoftware](https://github.com/OpenGewerk/opengewerk/blob/main/docs/konzept/Feature-Gliederung.md)
- [Planungskonzept von OpenGewerk Haustechnik](https://github.com/OpenGewerk/opengewerk-haustechnik/blob/main/docs/konzept/Planungskonzept.md)
- [Planungskonzept des Kanzlei-Hubs](https://github.com/OpenGewerk/opengewerk-kanzlei/blob/main/docs/konzept/Planungskonzept.md)

Einen Überblick, auch im Vergleich mit anderen Lösungen, gibt [opengewerk.de](https://opengewerk.de). Fachliche Rückmeldung aus dem Alltag eines Betriebs oder einer Kanzlei hilft gerade mehr als Code.

## Mitmachen

Die [Beitragsregeln](https://github.com/OpenGewerk/.github/blob/main/CONTRIBUTING.md) und der [Verhaltenskodex](https://github.com/OpenGewerk/.github/blob/main/CODE_OF_CONDUCT.md) gelten für alle Repositories der Organisation. Sicherheitslücken bitte über den Weg in [SECURITY.md](https://github.com/OpenGewerk/.github/blob/main/SECURITY.md) melden, nicht als öffentliches Issue.

Für kurze Fragen gibt es einen [Discord-Server](https://discord.gg/NRrEvbQdxz), für den Austausch unter Betrieben das Subreddit [r/OpenGewerk](https://www.reddit.com/r/OpenGewerk/). Beide ersetzen die Discussions nicht. Was dort geklärt wird und auch für andere zählt, gehört hinterher in eine Discussion oder ein Issue.

## Branding

Logo, Bildmarke, App-Icons und Banner liegen in diesem Repository unter [`brand/`](https://github.com/OpenGewerk/.github/tree/main/brand), und nur hier. Die anderen Repositories binden die Dateien per Raw-URL ein, damit keine Kopien entstehen. Farben, Dateizuordnung und Schutzraum stehen in [`brand/README.md`](https://github.com/OpenGewerk/.github/blob/main/brand/README.md).
