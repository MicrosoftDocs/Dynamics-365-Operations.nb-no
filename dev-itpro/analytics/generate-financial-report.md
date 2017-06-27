---
title: Generer en finansrapport
description: Dette emnet inneholder generell informasjon generering av finansrapporter.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9b0d8fd9f5ae9d99f299cc71d7caef021ad3fb9d
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="generate-a-financial-report"></a>Generer en finansrapport

[!include[banner](../includes/banner.md)]


Dette emnet inneholder generell informasjon generering av finansrapporter. 

Hvis du vil generere en rapport, åpner du rapportdefinisjonen og klikker deretter Generer på verktøylinjen. Vinduet Status for rapportkø åpnes og angir plasseringen av rapporten i køen. Den genererte rapporten åpnes i webvisningsprogrammet som standard.
| ![Obs!](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Obs!")**Obs!**        |
|------------------------------------------------------------------------------------------------|
| Du kan generere rapporter bare for mapper og plasseringer du har tilgang til. |

Tabellen nedenfor forklarer hvilke alternativer som er tilgjengelige for generering av rapporter.

| Alternativ                                                                                | For mer informasjon |
|---------------------------------------------------------------------------------------|----------------------|
| Konfigurere en tidsplan for å generere en rapport eller en gruppe rapporter automatisk              |                      |
| Se etter manglende kontoer eller dataene i en rapport, og validere nøyaktigheten til en rapport |                      |

Når du genererer en rapport, brukes alternativene du har angitt i kategorien Rapportdefinisjon. Kategorien Utdata og distribusjon lar deg angi en plassering for rapportbibliotek, noe som gjør det enkelt å dele rapporten.

## <a name="schedule-report-generation"></a> Planlegge rapportgenerering
Mange firmaer har et kjernesett med rapporter som kjøres med planlagte intervaller i henhold til forretningsprosessene. Du kan planlegge at en rapport skal genereres regelmessig, for eksempel daglig, ukentlig, månedlig eller årlig. Dette kan være én enkelt rapport eller en gruppe rapporter som omfatter flere firmaer. Du må angi legitimasjonen din for hvert av selskapene som er angitt, for eksempel dem i en rapporteringstredefinisjon. Hvis legitimasjonen ikke er gyldig, viser rapporten bare informasjonen som du har tilgang til, for eksempel firmaet du er logget på. Utdatainformasjon leses først fra rapportgruppen og deretter fra de enkelte rapportene.

Når rapporttidsplaner opprettes og lagres, vises de i navigasjonsruten under Rapporttidsplaner. Du kan opprette mapper for å organisere rapportene. Hvis én enkelt rapport i en plan ikke kjøres, fortsetter alle andre rapporter å kjøre.
| ![Viktig](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Viktig")**Viktig**                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hvis du vil opprette, endre og slette rapporttidsplaner, må du ha rolle som utformer eller administrator. Når en rapport kjøres, brukes legitimasjonen til brukeren som opprettet tidsplanen til å generere rapporten. |

### <a name="create-a-report-schedule"></a>Opprette en rapporttidsplan

1.  Gå til Fil -menyen i Rapportutforming og klikk Ny, og velg deretter Tapporttidsplan. Dialogboksen Ny rapporttidsplan.
2.  Under Innstillinger velger du en enkeltrapport eller en rapportgruppen som skal planlegges. Bare rapporter eller rapportgrupper for firmaet eller byggeblokkutvalget som du er logget på, er tilgjengelig.
3.  Merk av for Aktiv for å aktivere rapporttidsplanen. Bare oppretteren av rapporten eller en administrator kan aktivere eller deaktivere en rapporttidsplan.
4.  Klikk Tillatelser for å angi firmalegitimasjon. Som standard brukes påloggingsinformasjonen for firmaet du er logget på. Hvis andre firmaer er inkludert, for eksempel i rapporteringtredefinisjoner, velger du Bruk egne legitimasjoner, og angi deretter legitimasjonene for andre firmaer som er inkludert i rapporttidsplanen. Du kan velge Windows-godkjenning eller skrive inn et brukernavn og passord for hvert firma. Merk av for Lagre legitimasjoner for å lagre legitimasjonene for disse firmaene, og klikk deretter OK for å lukke dialogboksen.
5.  Under Hyppighet, i feltet Start regelmessighet , velger du datoen da planen skal starte. Som standard velges gjeldende systemdato på klientmaskinen.
6.  I feltet Kjør rapporten velger du tidspunkt da rapporten skal kjøres. Hvis du angir et tidspunkt som er før det gjeldende tidspunkt, kjøres rapporten på den neste planlagte datoen.
7.  I området Mønster for regelmessighet angir du hvor ofte rapporten skal kjøres. Daglig er valgt som standard med verdien 1 for intervall (dager). Andre alternativer omfatter ukentlig, månedlig og årlig.
8.  I området Område for regelmessighet velger du når generering av rapporten skal stoppe.
    -   Ingen sluttdato – Rapporttidsplanen kjøres i det uendelige.
    -   Angi antall forekomster – Rapporttidsplanen kjøres angitt antall ganger, og deretter deaktiveres den.
    -   Avslutt innen – Rapporttidsplanen slutter på den angitte datoen.

9.  Klikk Lagre på verktøylinjen. I dialogboksenden Lagre som skriver du inn et unikt navn og en beskrivelse for rapporttidsplanen.

Hvis du vil kopiere rapporttidsplaner, må du ha rolle som utformer eller administrator. Selv om en administrator endrer rapporttidsplanen, beholder rapporten legitimasjonen for brukeren som opprettet rapporten.
### <a name="copy-a-report-schedule"></a>Kopiere en rapporttidsplan

1.  Klikk Rapporttidsplaner i navigasjonsruten i Rapportutforming, og åpne en rapporttidsplan å kopiere.
2.  På Fil-menyen klikker du Lagre som, og deretter skriver du inn et nytt navn og en beskrivelse for tidsplanen i dialogboksen Lagre som. Klikk OK, og den nye tidsplanen vises i navigasjonsruten.
3.  I den nye tidsplanen kan du endre feltene og informasjon etter behov, og deretter klikker du Lagre på verktøylinjen eller klikker Lagre på Fil-menyen.

Hvis du vil slette en rapporttidsplan, må du være eier av rapporttidsplanen eller ha rollen administrator.
### <a name="delete-a-report-schedule"></a>Slette en rapporttidsplan

1.  Klikk Rapporttidsplaner i navigasjonsruten i Rapportutforming.
2.  Velg rapporttidsplanen som skal slettes, og klikk deretter Slett eller trykk DEL-tasten.
3.  Klikk Ja i dialogboksen for bekreftelse av sletting, for å slette rapporttidsplanen permanent. Hvis du ikke har tillatelse til å slette tidsplanen, vises en melding, og rapporten blir ikke slettet.

### <a name="credentials-and-report-schedules"></a>Legitimasjoner og rapporttidsplaner

Hvis du ikke angir legitimasjoner som kreves for alle firmaer i rapportene, får du en feilmelding når du lagrer rapporttidsplanen: "Du må angi legitimasjon for firmaene som finnes i denne rapporttidsplanen. Velg Tillatelser for å angi legitimasjonene."

Jenny logger for eksempel på firma A med sitt påloggingsnavn og passord. Hun oppretter en tidsplan for en rapport som bruker en rapporteringtredefinisjon til å samle inn data fra flere firmaer. Denne rapporttidsplanen er lagret, blir Jenny bedt om å angi legitimasjonene for de andre firmaene som er angitt i rapporteringstredefinisjonen. Når legitimasjonen utløper, genereres ikke de berørte rapportene i rapporttidsplanen før legitimasjonene er blitt oppdaterte. Det vises en melding i rapportkøen for å angi at tillatelsene må oppdateres. Rapporttidsplanen mislykkes hvis en av følgende situasjoner oppstår (fordi de krever legitimasjon):
-   Et nytt firma er lagt til i et rapporttre for en enkeltrapport.
-   En rapport i en rapportgruppe er endret.
-   Det er lagt til en ny rapport i et rapporttre for et nytt firma.

Klikk Tillatelser i dialogboksen Rapportplanlegging, og angi deretter riktige legitimasjoner.

## <a name="missing-account-analysis-feature"></a> Manglende kontoanalysefunksjon
Du kan søke etter finansielle kontoer og dimensjoner som mangler på tvers av alle raddefinisjoner, rapporteringstredefinisjoner og rapportdefinisjoner i en byggeblokkgruppe. Dette er nyttig når du oppretter eller oppdaterer flere kontoen eller byggeblokker i løpet av en kort tidsperiode, og du vil kontrollere at all ny informasjon inkluderes i rapportene.

Manglende kontoer finnes ved å bruke de laveste og høyeste verdiene fra raddefinisjonen eller rapporteringtredefinisjonen, og viser deretter en liste over kontoer som ikke er i raddefinisjonen eller rapporteringstredefinisjonen, men som er i de økonomiske dataen. Hvis en manglende konto er større eller mindre enn verdiene i raddefinisjon, inkluderes ikke denne kontoen i listen over manglende kontoer.
| ![Tips](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Tips")**Tips**                                             |
|----------------------------------------------------------------------------------------------------------------------------------|
| Denne prosessen skal kjøres for valideringsformål før du genererer månedlige rapporter og når du oppretter nye byggeblokker. |

Rapporter som har områder med verdier har mindre sannsynlig for å mangle kontoer. Hvis det er mulig, bruker du områder i byggeblokken for å ta med nye kontoer når de opprettes. Hvis en rapportdefinisjon er satt til @ANY firma, kan du logge på et bestemt firma og kjøre en analyse for manglende konto for firmaet.
| ![Obs!](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Obs!")**Obs!**                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hvis et nytt firma er lagt til, må du legge til det nye firmaet i rapporteringstrærne i eksisterende rapporter, hvis ikke inkluderes ikke firmaet i analysen for manglende kontoer. |

### <a name="run-missing-account-analysis"></a>Kjøre analyse for manglende konto

1.  Klikk Verktøy i Rapportutforming, og klikk deretter Analyse for manglende konto.
2.  I feltet Firmafilter velger du et firma å filtrere resultatet etter, eller velger Alle (ingen filtre) for å vise resultatet fra alle tilgjengelige firmaer.
3.  I feltet Dimensjonsfilter velger du en dimensjon å filtrere etter, eller velger Alle (ingen filtre) for å vise all dimensionsinformasjon for alle tilgjengelige dimensjoner.
4.  I feltet Grupper etter velger du et alternativ for å sortere resultatet. Du kan sortere resultatet i henhold til byggeblokken som påvirkes, eller du kan sortere resultatet etter dimensjons- og verdisett.
5.  Se gjennom resultatet som vises. Når du velger et element i den øverste ruten, viser den nederste ruten tilleggsinformasjon om unntaket. Dette omfatter tilknyttede dimensjoner, verdier og rapporter.
6.  Hvis du vil åpne det påvirkede elementet, klikker du det tilknyttede ikonet som vises i listeruten, eller høyreklikker elementet og velger Åpne. Hvis du vil velge flere elementer, holder du nede CTRL-tasten mens du merker elementene i den nedre ruten.
7.  Hvis det returneres verdier, byggeblokker eller rapporter som ikke skal inkluderes i analysen, høyreklikker du elementet og velger Utelat, eller merker av for Utelat ved siden av elementet for å fjerne det fra listen. Utelatte elementer inkluderes ikke når listen oppdateres. Hvis du vil velge flere elementer, holder du nede CTRL-tasten mens du merker elementene i den nedre ruten. Hvis du vil vise alle elementer, inkludert resultater som du tidligere har valgt for å utelate fra analysen, merker du av for Vis utelatte byggeblokker og verdier og klikker deretter Oppdater.
8.  Klikk Oppdater for å oppdatere unntak du har angitt. Klikk Ja for å utføre en fullstendig oppdatering av resultatene, eller klikk Nei for å utføre en delvis oppdatering av angitte elementer.
    | ![Obs!](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Obs!")**Obs!**                    |
    |------------------------------------------------------------------------------------------------------------|
    | Skjemaet oppdateres automatisk når det åpnes, med mindre det har vært åpnet de siste 15 minuttene. |

9.  Når problemene er løst, klikker du OK for å lukke dialogboksen.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Hurtigtaster for analyse for manglende konto
Når du kjører en analyse for manglende konto, er følgende hurtigtaster tilgjengelige.

| Hvis du vil gjøre dette                           | Bruk denne hurtigtasten |
|--------------------------------------|----------------------------|
| Filtrer etter firma                    | Alt+C                      |
| Filtrer etter dimensjon                  | Alt+D                      |
| Velg Grupper etter-feltet            | Alt+G                      |
| Vis utelatte blokker og verdier      | Alt+S                      |
| Oppdater resultater                      | Alt+R                      |
| Utelat den valgte byggeblokken  | Alt+X                      |
| Utelat den valgte raddefinisjonen  | Ctrl+B                     |
| Utelat den valgte dimensjonsverdien | Ctrl+D                     |
| Åpne den valgte rapportdefinisjonen  | Ctrl+R                     |
| Åpne den valgte raddefinisjonen     | Ctrl+O                     |

 
<a name="see-also"></a>Se også
--------

[Finansrapportering](financial-reporting-intro.md)

[Grensesnitt for Rapportutforming](report-designer-interface.md)



