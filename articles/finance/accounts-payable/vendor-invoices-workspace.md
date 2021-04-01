---
title: Arbeidsområde for leverandørfakturaoppføring
description: Dette emnet beskriver hvordan du konfigurerer arbeidsområdet som er relatert til leverandørfakturaer, og som viser informasjonen som er tilgjengelig via Microsoft Power BI.
author: abruer
manager: AnnBe
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2020-09-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0a32fc46fe6ac33abe5fcebb2ee5e2c92f468f84
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254134"
---
# <a name="vendor-invoice-entry-workspace"></a>Arbeidsområde for leverandørfakturaoppføring

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet beskriver hvordan du konfigurerer arbeidsområdet som er relatert til leverandørfakturaer, og som viser informasjonen som er tilgjengelig via Microsoft Power BI. Leverandørfakturainformasjonen i dette arbeidsområdet er filtrert for bestemte brukere, og vises i et grafisk format.

## <a name="overview"></a>Oversikt

Arbeidsområdet for **leverandørfakturaoppføring** viser informasjon som er knyttet til behandling av leverandørfaktura. Det inneholder en **Mitt arbeid**-visning og en **Analyse – alle selskaper**-side. **Mitt arbeid**-visningen viser sammendragsfliser, rutenett for leverandørtransaksjoner og tilknyttet leverandørinformasjon. Siden **Analyse – alle selskaper** bruker funksjonene i Microsoft Power BI for å vise bilder som er knyttet til leverandørfakturaer.

## <a name="set-up-the-workspace-to-show-power-bi-content"></a>Angi at arbeidsområdet skal vise Power BI-innhold

Du må fullføre oppsettet før data kan vises i Power BI-visualiseringer i arbeidsområdet for **leverandørfakturaoppføring**.

1. I arbeidsområdet for **funksjonsbehandling** filtrerer du listen for å finne funksjonen **Automatisering av leverandørfaktura**.
3. Velg **Aktiver nå**.
4. Hvis du vil sikre at fakturaer kan behandles fra begynnelse til slutt uten at det kreves manuell handling, definerer du en arbeidsflyt for leverandørfaktura. Hvis du vil konfigurere en arbeidsflyt, går du **Leverandører \> Oppsett \> Arbeidsflyter for leverandør**.
5. Gå til **Leverandører \> Oppsett \> Arbeidsflyter for leverandør**, og velg kategorien **Automatisering av leverandørfaktura** Hvis du vi ha mer informasjon, se [Oppsettsalternativer for automatisering av leverandørfakturaer](vnd-invoice-set-up-options.md).
6. Angi alternativet **Send automatisk importerte fakturaer til arbeidsflyt** til **Ja**.
7. Hvis produktkvitteringer skal samsvares automatisk, setter du alternativet **Samsvar automatisk produktkvitteringer med fakturalinjer** til **Ja**.
8. Se gjennom de gjenværende, valgfrie innstillingene, og konfigurer dem i henhold til organisasjonens krav.
9. Gå til **Systemadministrasjon \> Oppsett \> Systemparametere**, og angi feltene **Systemvaluta** og **Valutakurs for system**.
10. Gå til **Økonomimodul \> Oppsett \> Finans**, og angi feltene **Regnskapsvaluta** og **Type valutakurs**.
11. Gå til **Økonomimodul \> Valutaer \> Valutakurser**, og angi valutakursene mellom transaksjonsvalutaen og regnskapsvalutaen, og mellom regnskapsvalutaen og systemvalutaen.
12. Gå til **Systemadministrasjon \> Oppsett \> Enhetslager**, og se etter **Automatiseringsmål for leverandørfaktura**. Velg **Oppdater**.

Hvis du vil vise informasjonen som vises i arbeidsområdet, må du ha sikkerhetsrollen Regnskapssjef leverandørreskontro eller Regnskapsassistent.

## <a name="my-work-view"></a>Mitt arbeid-visning

### <a name="company-selection"></a>Firmavalg

Når funksjonen **Automatiser leverandørfakturaer** er aktivert, vises **Firma**-feltet øverst i arbeidsområdet. Valget i **Firma**-feltet påvirker alle opplysningene som vises i arbeidsområdet. Som standard viser visningen informasjon for firmaet du logget deg på. Hvis du velger et annet firma i **Firma**-feltet, kan du vise informasjon for dette firmaet på arbeidsområdet. Du kan deretter velge en flis i arbeidsområdet for å gå til den tilknyttede siden i det valgte firmaet.

### <a name="summary-tiles"></a>Sammendrag-fliser

Flisene i delen **Sammendrag av utestående fakturaer** i **Mitt arbeid**-visningen gir en oversikt over statusen til leverandørfakturaene. Du kan vise journaler som ennå ikke er bokført og fakturaer som er på vent. I tillegg er det fire fliser som er knyttet til funksjonen for automatisering av leverandørfaktura:

- Manuelt samsvar for mottak kreves
- Samsvarsvalidering mislyktes
- Fakturaer ble ikke sendt til arbeidsflyt
- Fakturaer ble ikke importert

(Disse fire flisene krever at funksjonen for automatisering av leverandørfaktura er aktivert i funksjonsbehandling.)

Hvis du vil bruke flisen **Gjenopprett leverandørfakturaer**, må du aktivere funksjonen i leverandørparametere. Gå til **Leverandører \> Leverandørparametere**, og deretter, i kategorien **Faktura**, angir du alternativet **Tillat gjenoppretting av leverandørfaktura** til **Ja**.

Når funksjonen er slått på, vil du også se tre fliser gruppert på arbeidsområdet i en del som kalles **Journaler**. Flisene har tittelen **Journaler**, **Journaler - tilordnet til meg** og **Fakturapulje**. 

Informasjonen i delen **Sammendrag av utestående fakturaer** er for firmaet som er definert som standardfirma for påloggingen.

### <a name="creating-new-records"></a>Oppretting av nye poster

Hvis du vil opprette en ny fakturapost, velger du **Ny**, og deretter velger du én av følgende oppføringstyper i listen:

- Leverandørfaktura
- Fakturajournal
- Global fakturajournal
- Ankomstregistrering
- Fakturagodkjenning

Legg merke til at posten du oppretter, er basert på firmafilteret, ikke firmaet du er logget på. Du er for eksempel logget på **UMSF**-firmaet, men firmafilteret er satt til **GBSI**. Når du velger **Ny** i dette tilfellet, og deretter velger en posttype i listen, opprettes posten i GBSI-firmaet.

### <a name="documents-not-invoiced-grids"></a>Rutnett for dokumenter som ikke er fakturert

Delen **Dokumenter som ikke er fakturert**, inneholder rutenett som viser dokumenter som venter på leverandørfakturaer.

Rutenettet **Åpne bestillinger** viser alle bestillinger som ennå ikke er fullstendig fakturert. Du kan bruke **Fakturer nå**-knappen til å opprette en leverandørfaktura for en bestilling. Du kan bruke **Forskuddsbetalt faktura nå**-knappen til å opprette en forskuddsbetalt faktura for en bestilling.

Rutenettet **Produktkvitteringer** viser alle transaksjonene for kjøpsmottak som ennå ikke er fullstendig fakturert. Du kan bruke **Fakturer nå**-knappen til å opprette en leverandørfaktura for en bestilling.

Rutenettet **Ventende leverandørfakturaer** viser alle leverandørfakturaer som ikke er sendt til arbeidsflytsystemet. Du kan bruke **Søk**-feltet og/eller firmafilteret til å søke etter en bestemt leverandørfaktura. Du kan bruke **Rediger**-knappen til å redigere en transaksjon som vises i rutenettet.

I rutenettet **Søk etter bestilling** kan du bruke **søke**-feltet til å søke etter en bestemt bestilling.

### <a name="related-information"></a>Beslektet informasjon

Du kan vise informasjon om posterte fakturaer ved hjelp av koblingene på høyre side av arbeidsområdet. Disse koblingene omfatter **Åpne leverandørfakturaer**, **Fakturajournal** og **Fakturahistorikk og samsvarende detaljer**. I **Leverandører**-delen kan du få tilgang til en filtrert liste som viser alle leverandører som er på vent, eller du kan bruke koblingen **Alle leverandører**. Koblingene **Alle bestillinger** og **Åpne forskuddsbetalinger** er også tilgjengelige.

### <a name="analytics--all-companies-page"></a>Siden Analyse – alle firmaer

Når alternativet **Send automatisk importerte fakturaer til arbeidsflyt** er satt til **Ja** på siden **Leverandørparametere**, kan du vise automatiseringsanalyse. Siden **Analyse – alle firmaer** inneholder viktige mål, for eksempel leverandørfakturaer som er under godkjenning av godkjenner og firma. Denne siden inneholder fem rapportsider. Én side gir en oversikt, og de andre sidene inneholder opplysninger om mål for leverandørautomatisering.

Tabellen nedenfor viser visuaiseringene som er tilgjengelig på hver rapportside.

| Rapportside                    | Visualiseringer |
|--------------------------------|----------------|
| Oversikt over leverandørfaktura        | <ul><li>Ventende leverandørfakturaer i automatisering i systemvaluta</li><li>Fakturaer som ikke ble importert</li><li>Fakturaer i arbeidsflyt</li><li>Berøringsfrie fakturaer siste 30 dager</li><li>Totale automatiserte fakturaer siste 30 dager</li><li>Saldo for åpne fakturaer i systemvaluta</li><li>Årsaker til feil, siste 30 dager</li><li>Prosentandel posterte fakturaer som ble behandlet automatisk</li><li>Antall dager en faktura skal behandles</ul></li> |
| Automatiseringsstatus              | <ul><li>Berøringsfrie fakturaer siste 30 dager</li><li>Berøringsfrie fakturaer siste 30 dager etter firma</li><li>Berøringsfrie fakturaer siste 30 dager etter leverandørfaktura</li><li>Prosentandel posterte fakturaer som ble behandlet automatisk</li><li>Antall dager en faktura skal behandles</li></ul> |
| Fakturaer som ikke ble importert | <ul><li>Fakturaer som ikke ble importert</li><li>Fakturaer som ikke ble importert av firma</li></ul> |
| Årsaker til automatiseringsfeil | <ul><li>Fakturaer som mislyktes</li><li>Fakturaer som mislyktes av firma</li><li>Fakturaer som mislyktes av leverandørgruppe</li></ul> |
| Arbeidsflytstatus                | <ul><li>Fakturaer i arbeidsflyt</li><li>Arbeidsflytforekomster for leverandfaktura</li><li>Tilordning per godkjenner</li><li>Arbeidsflyt for leverandørfaktura per firma</li><li>Gjennomsnittlig antall dager i arbeidsflyt etter godkjenner</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]