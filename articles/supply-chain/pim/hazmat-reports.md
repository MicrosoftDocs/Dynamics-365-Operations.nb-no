---
title: Forespørsler og rapporter om farlige materialer
description: Dette emnet beskriver hvordan du arbeider med de ulike rapportene som er knyttet til farlige materialer. Mange av disse rapportene er obligatoriske, slik at du overholder ulike forskrifter for farlige materialer under forsendelse og lagring.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 188c339ddf5f5c2488133924e9a0288f218f495c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434444"
---
# <a name="hazardous-materials-inquiries-and-reports"></a>Forespørsler og rapporter om farlige materialer

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management tilbyr forskjellige rapporter som er relatert til farlige materialer. Mange av disse rapportene er obligatoriske, slik at du overholder ulike forskrifter for farlige materialer under forsendelse og lagring.

Alle disse rapportene, med unntak av rapporten for **Flermodale farlig varer**, bruker du leveringsmåten som er definert for forsendelsen, til å finne forskriften som skal brukes til å skrive ut forsendelsesteksten for varer. Leveringsmåten er knyttet til transportøren og transportørtjenesten. Derfor må du konfigurere en transportør og en transportørtjeneste og koble dem til en leveringsmåte. Leveringsmåten er knyttet til forskriften for farlig materiale.

Følgende illustrasjon viser rekkefølgen av aktiviteter som oppstår når systemet genererer rapporter for farlig materiale.

![Aktivitetsrekkefølge for rapporter for farlige materialer](media/hazmat-report-sequence.png "Aktivitetsrekkefølge for rapporter for farlige materialer")

## <a name="set-up-hazardous-materials-reporting"></a><a name="set-up"></a>Definere rapportering av farlige materialer

Hvis du leverer varer som inneholder farlige materialer, må du vanligvis generere bestemte rapporter for å ivareta sikkerheten og overholde forskrifter for farlige materialer. Gjør følgende for å konfigurere rapportene.

1. Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.
2. Åpne kategorien **Rapporter**. På hurtigfanen for **rapportparameter for farlig materiale** angir du følgende felt.

    | Del | Felt | beskrivelse |
    |---|---|---|
    | Flermodale farlige varer | Reguleringskode | Velg forskriften som skal brukes når det genereres en rapport om **Flermodale farlige varer**. |
    | Lagringsgrenser for farlig materiale | Reguleringskode | Velg forskriften som skal brukes når lagergrenser evalueres. |
    | Transport av salgsvarer på vei | Forespørsel om katalogvedlikehold - gruppe - produkt | CMR står for carcinogenic, mutagenic og reprotoxic (kreftfremkallende, mutagene og reproduksjonstoksiske stoffer). Sett dette alternativet til **Ja** for å konfigurere systemet til å skrive ut bestemte advarsler og meldinger som er relatert til håndteringen av disse stoffene. |
    | Transport av salgsvarer på vei | Farlig materiale - gruppe - beskrivelse | Angi teksten i bestemte advarsler som er knyttet til CMR og transport av varer på vei. Denne teksten inkluderes i rapporten. |
    | Speditørdeklarasjon | Advarsel | Skriv inn teksten til en advarselsmelding som skal skrives ut på speditørskjemaet (for eksempel "Advarsel: farlige varer, brannfare"). |
    | Speditørdeklarasjon | Bunntekst - deklarering | Skriv inn teksten i en melding som skal skrives ut nederst i forsendelsesdeklareringsdokumentet. |
    | Farlig materiale - rapport - språk | Farlig materiale - innenlandsk - rapport - språk | Velg standardspråk for rapporter for farlige materialer som er tilknyttet innenlandske forsendelser. |
    | Farlig materiale - rapport - språk | Farlig materiale - eksport - rapport - språk | Velg standardspråk for rapporter for farlige materialer som er tilknyttet internasjonale forsendelser. |

## <a name="hazardous-materials-report"></a>Rapport om farlige materialer

Rapporten **Farlige materialer** viser en oversikt over alle varer som er konfigurert og definert slik at har informasjon om farlige varer. Du kan bruke denne rapporten til å overvåke og se gjennom informasjonen du må vedlikeholde. Siden for rapporten viser et begrenset utvalg av felt fra oppsettet for farlig materiale. Du kan imidlertid tilpasse den til å legge til flere felt etter behov.

For å vise denne rapporten, går du til **Behandling av produktinformasjon \> Forespørsler og rapporter \> Forsendelsesdokumentasjon for farlig materiale \> Farlige materialer**.

## <a name="hazardous-material-stock-limit-report"></a><a name="stock-limit-report"></a>Rapport om grense for farlig lagerbeholdning

Rapporten om **grense for farlig lagerbeholdning** lar deg overvåke lagernivåene for farlige materialer på lagerlokasjonene, for å sørge for at de forblir under etablerte sikre grenser. Disse grensene kommer fra grensene som er definert for hvert frigitte produkt.

For å vise denne rapporten går du til **Behandling av produktinformasjon \> Forespørsler og rapporter \> Dokumentasjon for farlig forsendelse \> Lagringsgrenser for farlig materiale**.

Hvis du vil ha mer informasjon om hvordan du angir lagergrenser for et frigitt produkt, kan du se [Angi lagringsgrenser for farlige produkter](hazmat-items.md#stock-limits).

Forskriften som brukes for lagergrenser, er definert på siden **Lagerstyringsparametere**. Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**, og deretter, i kategorien **Rapporter** i **Grense for farlig lagerbeholdning**, angir du en forskriftskode. Hvis du vil ha mer informasjon, kan du se [Definere rapportering av farlige materialer](#set-up) tidligere i dette emnet.

## <a name="verified-gross-mass-report"></a>Rapporten Bekreftet bruttomasse

Med rapporten **Bekreftet bruttomasse** kan du skrive ut informasjon om vekten til en forsendelse.

Hvis du vil generere og skrive ut denne rapporten, går du til **Lagerstyring \> Forsendelser \> Alle forsendelser** og åpner den relevante forsendelsen. Deretter, i handlingsruten i kategorien **Forsendelser** i gruppen **Dokument for farlige materialer**, velger du **Bekreftet bruttomasse**.

## <a name="multimodal-dangerous-goods-report"></a>Rapporten Flermodale farlige varer

Rapporten **Flermodale farlige varer** tilbys for forsendelser som må flyttes ved hjelp av en kombinasjon av transportmetoder. Det brukes vanligvis når en forsendelse flyttes først på vei og deretter på sjøen.

Hvis du vil generere og skrive ut denne rapporten, går du til **Lagerstyring \> Forsendelser \> Alle forsendelser** og åpner den relevante forsendelsen. Deretter, i handlingsruten i kategorien **Forsendelser** i gruppen **Dokument for farlige materialer**, velger du **Flermodale farlige varer**.

Når du genererer denne rapporten, lagres informasjonen slik at du kan redigere den og/eller skrive ut rapporten på nytt hvis du trenger det. Hvis du vil redigere en generert rapport, kan du gå til **Lagerstyring \> Forespørsler og rapporter \> Forsendelsesdokumentasjon for farlige materialer \> Flermodale farlige varer** og finne den relevante rapporten i listen. Når du er ferdig med å redigere innholdet som du ønsker, velger du **Skriv ut** i handlingsruten for å skrive ut rapporten.

## <a name="shippers-declaration-report"></a>Rapporten Speditørdeklarasjon

Rapporten **Speditørdeklarasjon** lar deg skrive ut informasjon som er knyttet til en deklarering av materialene som er inkludert i forsendelsen.

Hvis du vil generere og skrive ut denne rapporten, går du til **Lagerstyring \> Forsendelser \> Alle forsendelser** og åpner den relevante forsendelsen. Deretter, i handlingsruten i kategorien **Forsendelser** i gruppen **Dokument for farlige materialer**, velger du **Speditørdeklarasjon**.

## <a name="carriage-of-merchandise-by-road-report"></a>Rapporten Transport av salgsvarer på vei

Rapporten **Transport av salgsvarer på vei** ligner på et fraktbrev, men brukes vanligvis til veitransport i Europa i henhold til avtalen som gjelder forskrifter som er knyttet til den internasjonale transporten av farlig gods på veier (ADR). Denne rapporten bruker utskriftsteksten for levering for en vare, med mindre du angir feltet **Beskrivelse av farlig materialgruppe** på siden **Lagerstyringsparametere**.

Hvis du vil generere og skrive ut denne rapporten, går du til **Lagerstyring \> Forsendelser \> Alle forsendelser** og åpner den relevante forsendelsen. Deretter, i handlingsruten i kategorien **Forsendelser** i gruppen **Dokument for farlige materialer**, velger du **Transport av salgsvarer på vei**.

Når du genererer denne rapporten, lagres informasjonen slik at du kan redigere den og/eller skrive ut rapporten på nytt hvis du trenger det. Hvis du vil redigere en generert rapport, kan du gå til **Lagerstyring \> Forespørsler og rapporter \> Forsendelsesdokumentasjon for farlige materialer \> Transport av salgsvarer på vei** og finne den relevante rapporten i listen. Når du er ferdig med å redigere innholdet som du ønsker, velger du **Skriv ut** i handlingsruten for å skrive ut rapporten.

## <a name="shipment-summary-report"></a>Sammendragsrapport for forsendelse

Rapporten **Forsendelsessammendrag** gir informasjon som oppsummeres av transportkategorien som er knyttet til de frigitte varene.

Hvis du vil generere og skrive ut denne rapporten, går du til **Lagerstyring \> Forsendelser \> Alle forsendelser** og åpner den relevante forsendelsen. Deretter, i handlingsruten i kategorien **Forsendelser** i gruppen **Dokument for farlige materialer**, velger du **Forsendelsessammendrag**.

## <a name="bill-of-lading-report"></a>Rapporten Fraktbrev

Når funksjonen for farlige materialer er aktivert i systemet, inneholder rapporten **Fraktbrev** en **Farlige materialer**-kolonne som angir om en last inneholder farlige materialer. Denne rapporten er tilgjengelig fra siden **Alle laster** som vanlig.

## <a name="packing-list-report"></a>Rapporten Følgeseddelliste

Når funksjonen for farlige materialer er aktivert i systemet, inkluderer følgeseddellister tilleggsinformasjon som er knyttet til forsendelsesteksten for en vare. Denne rapporten er tilgjengelig fra siden **Alle laster** som vanlig.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]