<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/opengewerk/.github/main/brand/banner/opengewerk-banner-1280x640-dark.png">
  <img alt="OpenGewerk: Self-hosted CRM &amp; ERP für Handwerksbetriebe" src="https://raw.githubusercontent.com/opengewerk/.github/main/brand/banner/opengewerk-banner-1280x640-light.png" width="100%">
</picture>

# OpenGewerk

OpenGewerk ist Open-Source-Software für Handwerksbetriebe und für Betreiber von Gebäuden. Zwei Anwendungen stehen auf demselben Fundament: die Handwerkersoftware, CRM und ERP in einem einzigen Datenmodell mit Elektro und PV als Kernmodul, und OpenGewerk Haustechnik, ein CAFM für das technische Gebäudemanagement. Beide sind self-hosted, laufen also auf eigener Hardware, und die Daten bleiben im Betrieb. Für Steuerberater ist ein Kanzlei-Hub geplant, der die Mandanten mit der Handwerkersoftware in einer Anwendung bündelt.

**Self-hosted · Open Source · Deutsch**

## Kein Tarifmodell

OpenGewerk kostet keine Lizenz, und niemand hält eine Funktion zurück, um einen höheren Tarif zu verkaufen. Es gibt keine Tarifstufen und keine Nutzerlimits; jede Schnittstelle und jede Auswertung steht jedem Betrieb offen. Der Funktionsumfang ist der, der im Repository liegt.

Geld kann später mit Leistungen rund um die Software entstehen: Hosting für Betriebe, die nicht selbst hosten wollen, Installation und Migration, Support und Wartung, Schulungen, Anbindungen an Messgeräte und Fremdsysteme als Auftragsarbeit. Jede dieser Leistungen ist ein Angebot und keine Voraussetzung. Ein Betrieb muss OpenGewerk ohne fremde Hilfe betreiben können, sonst wäre die Beschränkung nur an eine andere Stelle gewandert.

Daraus folgt zweierlei: Es wird keine kommerzielle Fassung und keine bezahlten Erweiterungen geben, auch nicht vom Projekt selbst, und es gibt kein Contributor License Agreement. Ausführlich steht das in [Leitentscheidung 9 der Feature-Gliederung](https://github.com/opengewerk/opengewerk/blob/main/docs/konzept/Feature-Gliederung.md#0-leitentscheidungen).

## Die Repositories

| Repository | Wofür |
| --- | --- |
| [opengewerk](https://github.com/opengewerk/opengewerk) | Die Open-Source-Handwerkersoftware, CRM und ERP in einem: Angebot, Regiebericht, Rechnung und E-Rechnung, Zeiterfassung, Prüfprotokolle für Elektro und PV, eine Baustellen-App, die ohne Netz arbeitet, GoBD-konform. Plantafel und Buchhaltung folgen. |
| [opengewerk-haustechnik](https://github.com/opengewerk/opengewerk-haustechnik) | Open-Source-CAFM für das technische Gebäudemanagement: Liegenschaften, Räume und Anlagen in einem Datenmodell, Betreiberpflichten als überwachte Fristen, Rundgänge und Prüfungen auch ohne Netz, unveränderliche Nachweise. Steht auf demselben Fundament wie die Handwerkersoftware. |
| [opengewerk-kanzlei](https://github.com/opengewerk/opengewerk-kanzlei) | Der Hub für Steuerberater, der alle OpenGewerk-Mandanten in einer Anwendung bündelt. Föderiert: die Daten bleiben beim Mandanten. In Planung. |
| [opengewerk-api-spec](https://github.com/opengewerk/opengewerk-api-spec) | Der gemeinsame API-Vertrag zwischen beiden: OpenAPI-Definition, JSON-Schemas und Konformitätstests, versioniert nach SemVer. |
| [opengewerk-website](https://github.com/opengewerk/opengewerk-website) | Die Website unter [opengewerk.de](https://opengewerk.de), als statisches HTML mit Astro gebaut. |
| [.github](https://github.com/opengewerk/.github) | Dieses Profil, die Beitragsregeln, der Verhaltenskodex, die Sicherheitsrichtlinie und die Marke. |

## Stand

**Handwerkersoftware.** Das Fundament und Phase 1, das MVP für den Pilotbetrieb, sind gebaut; die neueste Fassung ist [OpenGewerk 0.6.5](https://github.com/opengewerk/opengewerk/releases) vom 30.10.2026. Eine Installation läuft über Docker Compose auf eigener Hardware, auf x86_64 wie auf ARM64, kommt als Release mit signierten Abbildern, wird im Browser eingerichtet und sichert sich jede Nacht selbst. Ein Betrieb führt damit Kunden, Objekte, Anlagen und Aufträge und schreibt Angebote, Rechnungen und E-Rechnungen (XRechnung, ZUGFeRD). Auf der Baustelle entstehen Regiebericht und Zeiterfassung, auch ohne Netz, und für Elektro das Stromkreisverzeichnis und das Prüfprotokoll nach DIN VDE 0100-600. Gebaut wird an Phase 2, dem Kern für Elektro und PV. Vor dem produktiven Einsatz stehen noch die fachliche Abnahme der Regelpakete und ein Praxistest der E-Rechnung bei einem echten Empfänger aus. Was im Einzelnen fertig ist, steht in [Funktionsumfang und Stand](https://github.com/opengewerk/opengewerk/blob/main/docs/funktionsumfang.md).

**OpenGewerk Haustechnik** ist am 01.10.2026 dazugekommen, als CAFM für alle, die Gebäude betreiben und dafür eigene Haustechniker haben. Das Fundament der Handwerkersoftware wurde dafür in eigene Pakete herausgelöst ([ADR 0010](https://github.com/opengewerk/opengewerk/blob/main/docs/adr/0010-fundament-als-pakete.md)). Phase 1, das MVP für den Pilotbetrieb, erschien am 15.10.2026, Phase 2 mit den vollständigen Betreiberpflichten am 21.10.2026 als Fassung 0.2.0; die neueste ist [OpenGewerk Haustechnik 0.2.5](https://github.com/opengewerk/opengewerk-haustechnik/releases) vom 30.10.2026. Der Pilotbetrieb, ein Träger mit rund zwanzig Liegenschaften, hat seine bisherige Anwendung abgeschaltet und arbeitet nur noch mit OpenGewerk Haustechnik. Was sie kann, steht in [Funktionsumfang und Stand](https://github.com/opengewerk/opengewerk-haustechnik/blob/main/docs/funktionsumfang.md).

Der Kanzlei-Hub ist noch in der Planung. Er baut auf der Buchhaltung der Handwerkersoftware auf, die dort mit Phase 3 kommt; bis dahin wird der gemeinsame API-Vertrag weitergeführt.

Den vollständigen Funktionsumfang beschreiben die drei Konzepte:

- [Feature-Gliederung der Handwerkersoftware](https://github.com/opengewerk/opengewerk/blob/main/docs/konzept/Feature-Gliederung.md)
- [Planungskonzept von OpenGewerk Haustechnik](https://github.com/opengewerk/opengewerk-haustechnik/blob/main/docs/konzept/Planungskonzept.md)
- [Planungskonzept des Kanzlei-Hubs](https://github.com/opengewerk/opengewerk-kanzlei/blob/main/docs/konzept/Planungskonzept.md)

Einen Überblick, auch im Vergleich mit anderen Lösungen, gibt [opengewerk.de](https://opengewerk.de). Fachliche Rückmeldung aus dem Betriebs- oder Kanzleialltag hilft gerade mehr als Code.

## Mitmachen

Die [Beitragsregeln](https://github.com/opengewerk/.github/blob/main/CONTRIBUTING.md) und der [Verhaltenskodex](https://github.com/opengewerk/.github/blob/main/CODE_OF_CONDUCT.md) gelten für alle Repositories der Organisation. Sicherheitslücken bitte über den Weg in [SECURITY.md](https://github.com/opengewerk/.github/blob/main/SECURITY.md) melden, nicht als öffentliches Issue.

Für kurze Fragen gibt es einen [Discord-Server](https://discord.gg/NRrEvbQdxz), für den Austausch unter Betrieben das Subreddit [r/OpenGewerk](https://www.reddit.com/r/OpenGewerk/). Beide ersetzen die Discussions nicht: was dort geklärt wird und für andere zählt, gehört hinterher in eine Discussion oder ein Issue.

## Branding

Logo, Bildmarke, App-Icons und Banner liegen in diesem Repository unter [`brand/`](https://github.com/opengewerk/.github/tree/main/brand). Das ist die einzige Quelle; die anderen Repositories binden die Dateien per Raw-URL ein, damit es keine Kopien gibt. Farben, Dateizuordnung und Schutzraum stehen in [`brand/README.md`](https://github.com/opengewerk/.github/blob/main/brand/README.md).
