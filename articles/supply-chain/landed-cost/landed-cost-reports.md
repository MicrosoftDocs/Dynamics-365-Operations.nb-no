---
title: Rapporter for netto innkjøpspris
description: Dette emnet beskriver hvordan du finner og bruker de ulike typene rapporter som er tilgjengelige for modulen Netto innkjøpspris.
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ea60826ddfd9553ba16c22f077d65732bf08e18fa079c6311431d35dd9aaa99f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765496"
---
# <a name="landed-cost-reports"></a>Rapporter for netto innkjøpspris

[!include [banner](../../includes/banner.md)]

## <a name="outstanding-invoices"></a>Utestående fakturaer

I rapporten for utestående fakturaer vises en liste over alle utestående fakturaer på de ulike kostnadsnivåene som er tilknyttet til hver sjøreise. Rapporten brukes til å avstemme sjøreisen og sjøreisekostnadene sammen med finanstransaksjonslisten regelmessig. Når en indirekte kostnad er fakturert, fjernes den fra rapporten.

Følg denne fremgangsmåten for å generere en rapport for utestående fakturaer.

1. Gå til **Netto innkjøpspris \> Rapporter \> Sporing \> Utestående fakturaer**.
1. I dialgoboksen **Utestående fakturaer** angir du en dato i feltet **Per dato**. Alle fakturaer som var utestående på eller før den datoen, vil bli inkludert i rapporten.
1. Under **Vis** velger du ett av følgende alternativer:

    - **Kostnad ikke fakturert** – Inkluder kostnader for fakturerte forsendelser som har en estimert kostnadsverdi, men ingen faktisk kostnad.
    - **Lager ikke fakturert** – Inkluder kostnader som er fakturert, men som bestillingen ennå ikke er mottatt for.
    - **Alt ikke fakturert** – Inkluder resultatene fra både alternativet **Kostnad ikke fakturert** og alternativet **Lager ikke fakturert**.

1. Sett alternativet **Inkluder nye kostnader** til *Ja* hvis du vil inkludere kostnader som ennå ikke har en faktisk kostnad, og som lageret ikke er mottatt for. Hvis du setter det til *Nei*, vil rapporten bare omfatte kostnader som er fakturert.
1. Aktiver hver detaljtype du vil ta med i rapporten, i delen **Vis**.
1. Når du gjør det for andre typer rapporter i Microsoft Dynamics 365 Supply Chain Management, bruker du hurtig kategorien **Mål** til å velge utdataformatet for rapporten.
1. Når du gjør det for andre typer rapporter i Supply Chain Management, kan du bruke hurtigfanen **Poster som skal inkluderes** til ytterligere å begrense postene som blir inkludert i rapporten.
1. Velg **OK** for å generere rapporten.

## <a name="activityprovider-analysis-reports"></a>Rapporter for aktivitets-/leverandøranalyse

Ved å bruke rapportene for aktivitets-/leverandøranalyse kan du gjennomgå nøyaktigheten til tidsestimatene for hver leverandør.

Følg denne fremgangsmåten for å generere en rapport for aktivitets-/leverandøranalyse.

1. Følg ett av disse trinnene, avhengig av rapporttypen du vil opprette:

    - Gå til **Netto innkjøpspris \> Rapporter \> Analyse av aktivitet/leverandør etter aktivitet**. I dette tilfellet grupperes tidsestimatene etter aktivitet.
    - Gå til **Netto innkjøpspris \> Rapporter \> Analyse av aktivitet/leverandør etter leverandør**. I dette tilfellet grupperes tidsestimatene etter leverandør.

    Dialogboksen **Analyse av aktivitet/leverandør etter aktivitet** eller **Analyse av aktivitet/leverandør etter leverandør** vises. Begge dialogboksene har de samme alternativene.

1. Når du gjør det for andre typer rapporter i Supply Chain Management, bruker du hurtigfanen **Mål** til å velge utdataformatet for rapporten.
1. Når du gjør det for andre typer rapporter i Supply Chain Management, kan du bruke hurtigfanen **Poster som skal inkluderes** til ytterligere å begrense postene som blir inkludert i rapporten.
1. Velg **OK** for å generere rapporten.

## <a name="voyage-costing-reports"></a>Etterkalkuleringsrapporter for sjøreise

Etterkalkuleringsrapportene for sjøreise viser kostnaden for varene og importkostnadene per folio, forsendelsescontainer eller sjøreise, avhengig av alternativene du velger når du genererer rapporten. Ved hjelp av hver etterkalkuleringsrapport for sjøreise kan du se den estimerte kostnaden for en sjøreise kontra den faktiske kostnaden, og den kan deles opp av flere identifiserende faktorer.

Følg denne fremgangsmåten for å generere en etterkalkuleringsrapportene for sjøreise.

1. Følg ett av disse trinnene, avhengig av rapporttypen du vil opprette:

    - Gå til **Netto innkjøpspris \> Rapporter \> Etterkalkulering \> Etterkalkulering av sjøreise basert på individuell kost**. I dette tilfellet vil det individuelle kostnadsalternativet vise importkostnader per kostnadsområde per kosttypekode.
    - Gå til **Netto innkjøpspris \> Rapporter \> Etterkalkulering \> Etterkalkulering av sjøreise basert på rapporteringskategori**. I dette tilfellet blir importkostnaden inndelt i de ulike rapporteringskategoriene. Kosttyper grupperes etter rapporteringskategorier.

    Dialogboksen **Etterkalkulering av sjøreise basert på individuell kost** eller **Etterkalkulering av sjøreise basert på rapporteringskategori** vises. Disse dialogboksene ligner på hverandre. Eventuelle forskjeller bemerkes i resten av denne fremgangsmåten.

1. Hvis du åpnet dialogboksen **Etterkalkulering av sjøreise basert på rapporteringskategori**, velger du en av følgende verdier i feltet **Kostnad**:

    - **Kostnadsverdi** – Verdien beregnes ved å bruke automatiske kostnader eller opprettes manuelt i kostnadsområdet.
    - **Estimert** – Etter at varene er mottatt, angis den estimerte kostnaden.
    - **Faktisk** – Når ordren er fakturert, settes den faktiske kostnaden til kostnaden på fakturaen.
    - **Best** – Systemet vil bruke det av de tre alternativene som er mest nøyaktig. (Det anbefales at du velger dette alternativet.)

1. Sett alternativet **Per vare** til *Ja* for å vise kostnaden for hver vare. Sett det til *Nei* for å vise kostnader per sjøreise.
1. I delen **Vis** velger du kategoriene du vil dele inn kostnaden i.
1. I delen **Dimensjoner** velger du dimensjonene som skal tas med i rapporten.
1. Når du gjør det for andre typer rapporter i Supply Chain Management, bruker du hurtigfanen **Mål** til å velge utdataformatet for rapporten.
1. Når du gjør det for andre typer rapporter i Supply Chain Management, kan du bruke hurtigfanen **Poster som skal inkluderes** til ytterligere å begrense postene som blir inkludert i rapporten.
1. Velg **OK** for å generere rapporten.

## <a name="shipping-container-receipts-list"></a>Liste over mottak av fraktcontainer

Mottakslisten for forsendelsescontainer inneholder alle ikke-forfalte antall som forfaller på eller før en forventet dato. Lagerpersonalet kan bruke denne rapporten til å identifisere de forventede varene i en forsendelsescontainer. Den kan også brukes til å validere varer manuelt når de mottas på en forsendelsescontainer.

Følg denne fremgangsmåten for å generere en liste over forsendelsescontainere.

1. Gå til **Netto innkjøpspris \> Rapporter \> Sporing \> Mottaksliste for forsendelsescontainer**.
1. I dialogboksen **Mottaksliste for forsendelsescontainer** angir du en dato i feltet **Forventet dato**. Alle antall som ikke ble mottatt på eller før den datoen, vil bli inkludert i rapporten.
1. I delen **Dimensjoner** velger du dimensjonene som skal tas med i rapporten.
1. Når du gjør det for andre typer rapporter i Supply Chain Management, bruker du hurtigfanen **Mål** til å velge utdataformatet for rapporten.
1. Når du gjør det for andre typer rapporter i Supply Chain Management, kan du bruke hurtigfanen **Poster som skal inkluderes** til ytterligere å begrense postene som blir inkludert i rapporten.
1. Velg **OK** for å generere rapporten.

## <a name="expected-delivery-report"></a>Rapport for forventet levering

Rapporten for forventet levering inneholder grunnleggende informasjon om sjøreise, forsendelsescontainer, folio, varer og forventet leveringsdato.

Følg denne fremgangsmåten for å generere en rapport for forventet levering.

1. Gå til **Netto innkjøpspris \> Rapporter \> Sporing \> Forventet levering**.
1. Velg datoen da leveringen av varene til det endelige mållageret forventes, i feltet **Forventet dato** dialogboksen **Foreventet levering**. Alle sjøreiselinjer som har en forventet dato på eller før den datoen, og som ennå ikke er mottatt, blir inkludert i utdataene.
1. Valgfritt: Velg en leverandørkonto for å inkludere bare leveringer fra en bestemt leverandør, i feltet **Leverandørkonto**.
1. I delen **Dimensjoner** velger du dimensjonene som skal tas med i rapporten.
1. Når du gjør det for andre typer rapporter i Supply Chain Management, bruker du hurtigfanen **Mål** til å velge utdataformatet for rapporten.
1. Når du gjør det for andre typer rapporter i Supply Chain Management, kan du bruke hurtigfanen **Poster som skal inkluderes** til ytterligere å begrense postene som blir inkludert i rapporten.
1. Velg **OK** for å generere rapporten.
