---
title: Generer finansrapporter
description: Denne artikkelen inneholder generell informasjon generering av finansrapporter.
author: jinniew
ms.date: 02/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2f55fe1a23735d8631a5918fa49e08f74eee4d37
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802776"
---
# <a name="generate-financial-reports"></a>Generer finansrapporter

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder generell informasjon generering av finansrapporter.

Hvis du vil generere en rapport, åpner du rapportdefinisjonen og velger **Generer** på verktøylinjen. Siden **Rapportkøstatus** åpnes og angir hvor rapporten er i køen.

Etter hvert som rapportgenereringen fremskrider, vises kanskje følgende statusindikatorer for rapportkø på siden **Rapportkøstatus**.

| Status          | Status | Beskrivelse|
|-----------------|--------|--------------------|
| Køing        | Midlertidig |Rapportdefinisjonen valideres før rapporten legges i genereringskøen.                    |
| Satt i kø          | Midlertidig | Rapporten går inn i rapportgenereringskøen og venter på behandling.                      |
| Behandler      | Midlertidig | Denne statusen følger vanligvis statusen **Satt i kø**, og går vanligvis over til tilstanden **Avsluttende** når behandlingen er fullført.       |
| Etterbehandles | Midlertidig | Denne statusen følger statusen **Behandler** og angir at alle rapportdataene samles inn, men at avledede handlinger, for eksempel beregning og opprulling, blir utført.            |
| Annullerer      | Midlertidig | Rapporteringen avbrytes fordi brukeren har bedt om det. Denne tilstanden er et resultat av at en bruker har bedt om avbrudd for en rapport i tilstanden **Satt i kø** eller **Behandler**. Systemet prøver å sette rapporten i tilstanden **Avbrutt** med mindre systemet har kommet for langt og må fullføre den i en annen tilstand. |
| Avbrutt        | Avsluttende | Rapporten er ferdigbehandlet, men ble ikke fullført på grunn av en brukerforespurt stopp.            |
| Fullført       | Avsluttende | Rapporten er klar til bruk.                      |
| Mislykket          | Avsluttende | Rapporten er ferdigbehandlet, men mislyktes og må ikke brukes. |

Den genererte rapporten åpnes i webvisningsprogrammet som standard. Følgende alternativer er tilgjengelige for generering av rapporter:

- Konfigurere en tidsplan for å generere en rapport eller en gruppe rapporter automatisk
- Se etter manglende kontoer eller dataene i en rapport, og validere nøyaktigheten til en rapport

Når du genererer en rapport, brukes alternativene du har angitt i fanene Rapportdefinisjon.

## <a name="generate-a-financial-report"></a>Generer en finansrapport

Hvis du vil generere en økonomisk rapport, går du til **Økonomimodul** \> **Forespørsler og rapporter** \> **Finansrapporter**.

- Velg en rapport som skal genereres, og velg **Generer**.
- Fyll ut **Rapportdato**-feltet og velg **OK**.

Etter at rapporten er generert, vil rapporten være tilgjengelig for visning i **Rapporter**-delen.

Du kan velge å **vise** eller **slette** rapporten.

Hvis du vil generere en rapport med **Rapportutforming**, åpner du rapportdefinisjonen og velger deretter knappen **Generer** på verktøylinjen. Siden **Rapportkøstatus** åpnes og angir plasseringen av rapporten i køen. Den genererte rapporten åpnes i webvisningsprogrammet som standard.

## <a name="report-groups"></a>Rapportgrupper

Rapportgrupper er en effektiv måte å generere flere rapporter på samtidig. La oss for eksempel anta at brukerne genererer åtte rapporter hver måned ved månedsslutt. Opprett en rapportgruppe, og i stedet for å velge **Generer** for hver av de åtte rapportene i gruppen, kan du velge **Generer** for rapportgruppen, og de åtte rapportene blir generert i ett trinn. Når rapportene i den valgte rapportgruppen er generert, kan du gå til **Finansrapporter** (**Økonomimodul > Forespørsler og rapporter > Finansrapporter**) for å vise de individuelle rapportene. Fullfør følgende trinn for å konfigurere en rapportgruppe.

1. Velg **Rapportgrupper** i **Report Designer**. 
2. Velg de eksisterende rapportdefinisjonene som skal tas med i rapportgruppen. 
3. Velg innstillinger for overstyring av firma, detaljer og datoer fra alle rapportene som skal tas med i gruppen.
   Det anbefales å angi innstillingene **Firma**, **Periode**, **År** og **Detaljnivå** for hver rapport. 
4. Lagre rapportgruppen.

## <a name="schedule-report-generation"></a>Planlegge rapportgenerering
Mange firmaer har et kjernesett med rapporter som kjører i planlagte intervaller for å justeres mot forretningsprosessene. Du kan planlegge at en rapport skal genereres regelmessig, for eksempel daglig, ukentlig, månedlig eller årlig. Dette kan være én rapport eller en gruppe med rapporter som inkluderer flere firmaer. Du må angi legitimasjonen for hvert av firmaene som er angitt, for eksempel firmaene i en definisjon av rapporteringstre. Hvis legitimasjonen ikke er gyldig, viser rapporten bare informasjonen du har tilgang til, for eksempel firmaet du er logget på. Utdatainformasjon leses først fra rapportgruppen og deretter fra de enkelte rapportene.

Når rapporttidsplaner opprettes og lagres, vises de i navigasjonsruten under **Rapporttidsplaner**. Du kan opprette mapper for å ordne rapportene. Hvis én rapport i en plan ikke kjører, fortsetter alle andre rapporter å kjøre.

> [!IMPORTANT]
> Hvis du vil opprette, redigere og slette rapportplaner, må du ha en rolle som utformer eller administrator. Når en rapport kjøres, brukes legitimasjonen til brukeren som opprettet tidsplanen til å generere rapporten.

### <a name="create-a-report-schedule"></a>Opprette en rapporttidsplan

1. Gå til **Fil**-menyen i **Report Designer**, og velg **Ny**, og velg deretter **Rapportplan**. Dialogboksen **Ny rapporttidsplan** åpnes.
2. Under **Innstillinger** velger du en enkeltrapport eller en rapportgruppen som skal planlegges. Bare rapporter eller rapportgrupper for firmaet eller utvalget av byggeblokker som du for øyeblikket er logget på, er tilgjengelige.
3. Merk av for **Aktiv** for å aktivere rapporttidsplanen. Bare oppretteren av rapporten eller en administrator kan aktivere eller deaktivere en rapportplan.
4. Velg knappen **Tillatelser** for å angi firmalegitimasjon. Som standard brukes påloggingsinformasjonen din for firmaet der du er logget på. Hvis andre firmaer er inkludert, for eksempel i rapporteringtredefinisjoner, velger du **Bruk egne legitimasjoner**, og angi deretter legitimasjonene for andre firmaer som er inkludert i rapporttidsplanen. Du kan velge **Windows-godkjenning** eller skrive inn et brukernavn og passord for hvert firma. Merk av for **Lagre legitimasjoner** for å lagre legitimasjonene for disse firmaene, og velg deretter **OK** for å lukke dialogboksen.
5. Under **Hyppighet** i feltet **Start regelmessighet** velger du datoen da planen skal starte. Som standard velges den gjeldende systemdatoen for klientdatamaskinen.
6. I feltet **Kjør rapporten** velger du tidspunkt da rapporten skal kjøres. Hvis du angir et klokkeslett som er tidligere enn det gjeldende systemklokkeslettet, kjører rapporten på den neste planlagte datoen.
7. I området **Mønster for regelmessighet** angir du hvor ofte rapporten skal kjøres. **Daglig** er valgt som standard med verdien **1** for **Intervall (dager)**. Andre alternativer omfatter **Ukentlig**, **Månedlig** og **Årlig**.
8. I området **Gjentakelsesområde** velger du når generering av rapporten skal stoppe.

    - **Ingen sluttdato** – Rapporttidsplanen kjøres i det uendelige.
    - **Angi antall forekomster** – Rapporttidsplanen kjøres angitt antall ganger, og deretter deaktiveres den.
    - **Avslutt innen** – Rapporttidsplanen slutter på den angitte datoen.

9. Velg **Lagre**. I dialogboksen **Lagre som** skriver du inn et unikt navn og en beskrivelse for rapporttidsplanen.

Hvis du vil kopiere rapporttidsplaner, må du ha rolle som utformer eller administrator. Selv om en administrator endrer rapporttidsplanen, beholder rapporten legitimasjonen for brukeren som opprettet rapporten.

### <a name="copy-a-report-schedule"></a>Kopiere en rapporttidsplan

1. Velg **Rapporttidsplaner** i navigasjonsruten i Report Designer, og åpne en rapporttidsplan å kopiere.
2. På **Fil**-menyen velger du **Lagre som**, og deretter skriver du inn et nytt navn og en beskrivelse for tidsplanen i dialogboksen **Lagre som**. Velg **OK**, og den nye tidsplanen vises i navigasjonsruten.
3. I den nye tidsplanen kan du endre feltene og informasjon etter behov, og deretter velger du **Lagre** på verktøylinjen eller velger **Lagre** på **Fil**-menyen.

Hvis du vil slette en rapporttidsplan, må du være eier av rapporttidsplanen eller ha rollen administrator.

### <a name="delete-a-report-schedule"></a>Slette en rapporttidsplan

1. Velg **Rapporttidsplaner** i navigasjonsruten i Report Designer.
2. Velg rapporttidsplanen som skal slettes, og velg deretter **Slett** eller trykk **DEL**-tasten.
3. Velg **Ja** i dialogboksen for bekreftelse av sletting, for å slette rapporttidsplanen permanent. Hvis du ikke har tillatelse til å slette tidsplanen, vises en melding, og rapporten blir ikke slettet.

### <a name="credentials-and-report-schedules"></a>Legitimasjon og rapportplaner

Hvis du ikke angir legitimasjoner som kreves for alle firmaer i rapportene, får du en feilmelding når du lagrer rapporttidsplanen: "Du må angi legitimasjon for firmaene som finnes i denne rapporttidsplanen. Velg **Tillatelser** for å angi legitimasjonen."

En bruker logger for eksempel på Firma A ved hjelp av påloggingsinformasjon og passord. Brukeren oppretter en tidsplan for en rapport som bruker en rapporteringtredefinisjon til å samle inn data fra flere firmaer. Når rapportplanen lagres, blir brukeren bedt om å angi legitimasjonen for de andre firmaene som er angitt i definisjonen av rapporteringstre. Når legitimasjonen utløper, genereres ikke de berørte rapportene i rapporttidsplanen før legitimasjonen er oppdatert. Det vises en melding i rapportkøen for å angi at tillatelsene må oppdateres. Rapporttidsplanen mislykkes hvis en av følgende situasjoner oppstår (fordi de krever legitimasjon):

- Et nytt firma er lagt til i et rapporttre for en enkeltrapport.
- En rapport i en rapportgruppe har blitt endret.
- En ny rapport for et ekstra firma har blitt lagt til i en rapportgruppe.

Velg **Tillatelser** i dialogboksen **Rapportplanlegging**, og angi deretter riktige legitimasjoner.

## <a name="missing-account-analysis-feature"></a>Funksjonen Analyse av manglende konto
Du kan søke etter finansielle kontoer og dimensjoner som mangler på tvers av alle raddefinisjoner, rapporteringstredefinisjoner og rapportdefinisjoner i en byggeblokkgruppe. Dette er nyttig når du oppretter eller oppdaterer flere kontoer eller byggeblokker i løpet av en kort tidsperiode, og du vil kontrollere at all ny informasjon inkluderes i rapportene.

Hvilke kontoer som mangler, fastsettes ved å bruke de laveste og høyeste verdiene fra raddefinisjonen eller rapporteringstredefinisjonen, og deretter vises en liste over kontoer som ikke er i raddefinisjonen eller rapporteringstredefinisjonen, men som er i de økonomiske dataene. Hvis en manglende konto er større eller mindre enn verdiene i raddefinisjonen, tas ikke denne kontoen med i listen over manglende kontoer.

> [!TIP]
> Ved validering må denne prosessen kjøres før du genererer månedlige rapporter, og når du oppretter nye byggeblokker.

Rapporter som har områder med verdier har mindre sannsynlig for å mangle kontoer. Hvis det er mulig, bruker du områder i byggeblokken til å ta med nye kontoer når de opprettes. Hvis en rapportdefinisjon er satt til firmaet @ANY, kan du logge på et bestemt firma og kjøre en analyse av manglende konto for det firmaet.

> [!NOTE]
> Hvis et nytt firma er lagt til, må du legge til det nye firmaet i rapporteringstrærne i eksisterende rapporter, hvis ikke inkluderes ikke firmaet i analysen for manglende kontoer.

### <a name="run-missing-account-analysis"></a>Kjøre analyse for manglende konto

1. Velg **Verktøy** i Report Designer, og velg deretter **Analyse for manglende konto**.
2. I feltet **Firmafilter** velger du et firma å filtrere resultatet etter, eller velger **Alle (ingen filtre)** for å vise resultatet fra alle tilgjengelige firmaer.
3. I feltet **Dimensjonsfilter** velger du en dimensjon å filtrere etter, eller velger **Alle (ingen filtre)** for å vise all dimensionsinformasjon for alle tilgjengelige dimensjoner.
4. I feltet **Grupper etter** velger du et alternativ for å sortere resultatet. Du kan sortere resultater i henhold til byggeblokkene som påvirkes, eller du kan sortere resultater etter dimensjons- og verdisett.
5. Se gjennom resultatene som vises. Når du velger et element i den øverste ruten, viser den nederste ruten tilleggsinformasjon om unntaket. Dette inkluderer relaterte dimensjoner, verdier og rapporter.
6. Hvis du vil åpne det påvirkede elementet, velger du det tilknyttede ikonet som vises i listeruten, eller høyreklikker elementet og velger **Åpne**. Hvis du vil velge flere elementer, holder du nede **CTRL**-tasten mens du merker elementene i den nedre ruten.
7. Hvis det returneres verdier, byggeblokker eller rapporter som ikke skal tas med i analysen, høyreklikker du på elementet og velger **Utelat**, eller merker av for **Utelat** ved siden av elementet for å fjerne det fra listen. Utelatte elementer tas ikke med når listen oppdateres. Hvis du vil velge flere elementer, holder du nede **CTRL**-tasten mens du merker elementene i den nedre ruten. Hvis du vil vise alle elementer, inkludert resultater som du tidligere valgte å utelate fra analysen, merker du av for **Vis ekskluderte byggeblokker og verdier**, og deretter klikker du **Oppdater**.
8. Velg **Oppdater** for å oppdatere unntak du har angitt. Velg **Ja** for å utføre en fullstendig oppdatering av resultatene, eller velg **Nei** for å utføre en delvis oppdatering av angitte elementer.

    > [!NOTE]
    > Siden oppdateres automatisk når det åpnes, hvis ikke det har blitt åpnet de siste 15 minuttene.

9. Når problemene er løst, velger du **OK** for å lukke dialogboksen.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Hurtigtaster for analyse for manglende konto
Når du kjører en analyse for manglende konto, er følgende hurtigtaster tilgjengelige.

| Hvis du vil gjøre dette                           | Trykk  |
|--------------------------------------|----------------------------|
| Filtrer etter firma                    | Alt+C                      |
| Filtrer etter dimensjon                  | ALT+D                      |
| Velg Grupper etter-feltet.            | Alt+G                      |
| Vis ekskluderte blokker og verdier      | Alt+S                      |
| Oppdater resultater                      | Alt+R                      |
| Utelat den valgte byggeblokken  | Alt+X                      |
| Utelat den valgte raddefinisjonen  | Ctrl+B                     |
| Utelat den valgte dimensjonsverdien | Ctrl+D                     |
| Åpne den valgte rapportdefinisjonen  | Ctrl+R                     |
| Åpne den valgte raddefinisjonen     | Ctrl+O                     |


## <a name="additional-resources"></a>Tilleggsressurser

[Finansrapportering](financial-reporting-intro.md)

[Grensesnitt for Rapportutforming](report-designer-interface.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
