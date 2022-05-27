---
title: Forretningsdokumenter som støttes av Globalt lagerregnskap
description: Dette emnet viser forretningsdokumentene som støttes av Globalt lagerregnskap. Det inneholder også et detaljert eksempel for bestillingsdokumenter.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 44081be35c6737aa0d16b6e11a5fc8f94b41e872
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674456"
---
# <a name="business-documents-supported-by-global-inventory-accounting"></a>Forretningsdokumenter som støttes av Globalt lagerregnskap

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Når tillegget for globalt lagerregnskap er ferdig konfigurert, er det klart til å behandle lagerrelaterte dokumenter som angis i Microsoft Dynamics 365 Supply Chain Management.

## <a name="supported-business-documents"></a>Støttede forretningsdokumenter

Det er to typer forretningsdokumenter:

- **Dokumenter som har en journal** – Disse dokumentene omfatter produktkvitteringer, innkjøpsfakturaer, følgesedler og salgsfakturaer.
- **Dokumenter som ikke har en journal** – Disse dokumentene omfatter opptellings-, bevegelses- og lagerjusteringsdokumenter.

Senere i dette emnet brukes bestillinger som et eksempel på prosessen.

Tabellen nedenfor viser dokumentene som gjeldende frigivelse støtter.

| Dokumenttype      | Dokument        |
|--------------------|-----------------|
| Bestilling     | Produktkvittering |
| Bestilling     | Faktura         |
| Salgsordre        | Følgeseddel    |
| Salgsordre        | Faktura         |
| Lagerjournaler | Bevegelse        |
| Lagerjournaler | Justering      |
| Lagerjournaler | Opptelling        |
| Lagerjournaler | Overfør        |
| Overføringsordre     | Forsendelse        |
| Overføringsordre     | Motta         |

> [!IMPORTANT]
> Globalt lagerregnskap behandler dokumentene som angis i Supply Chain Management, asynkront. Ingen feilmeldinger vil vises for problematiske dokumenter.

## <a name="example-purchase-order"></a>Eksempel: Bestilling

### <a name="product-receipt"></a>Produktkvittering

Poster produktkvitteringer på vanlig måte. Velg en bestilling på siden **Alle bestillinger**, og deretter, på handlingssiden i fanen **Motta**, velger du **Produktkvittering** for å åpne siden **Produktkvitteringsjournal**. En operasjonshendelse og en Globalt lagerregnskap-hendelse genereres for hver linje. Derfor velger du kategorien **Linjer**, og deretter velger du **Lager \> Hendelser og målinger** for å åpne **Hendelser og målinger**-siden.

Globalt lagerregnskap er et regnskapssystem som er basert på hendelser og målinger. Rutenettet for målingslinjen på **Hendelser og målinger**-siden viser en liste over målinger. Hvert mål har en liste over dimensjoner.

For hver operasjonshendelse finnes det to typer mål:

- **Måleoperasjoner** – Disse målene beskriver forretningsdokumenter med generiske termer. Ett mål er produktantallet som bruker måleenheten som brukes i dokumentet. Det er også mål som påvirker lagerverdien, for eksempel utvidet pris, rabatt, rabattprosent og linjetillegg.
- **Målinger for ressursregnskap** – Disse målingene kommer fra lagerbeholdningsperspektivet. De beskriver dokumentets innvirkning på lageret i lagermåleenheten. Hvis det finnes flere lagerregistreringer, finnes det flere linjer med målinger for ressursregnskap.

Dimensjonene er organisert på følgende måte:

- **Dualitet** – Dualitet beskriver agentene som deltar i de økonomiske hendelsene. Når det gjelder eksterne forretningsdokumenter, beskriver de primære dimensjonene den juridiske enheten der dokumentet er lagt inn, mens de dobbeltdimensjonene beskriver leverandøren, kunden og så videre. Når det gjelder interne forretningsdokumenter (for eksempel overføringsordrer), beskriver de dobbeltdimensjonene motpartslageret.
- **Dimensjonstype** – Dimensjonstypene kategoriserer dimensjonene.
- **Dimensjon** – Navnet på dimensjonen.
- **Dimensjonsverdi** – Navnet på dimensjonen.

### <a name="global-inventory-accounting-event"></a>Globalt lagerregnskap-hendelse

Globalt lagerregnskap tar driftshendelsene og målingene som inndata. Deretter utføres gjeldende regnskap for hver tilknyttede hovedbok basert på tilknyttet valuta og konvensjon. Du kan velge **Hendelser og målinger for Globalt lagerregnskap** for å vise Globalt lagerregnskap-hendelsen. Globale lagerregnskap-hendelsen følger samme metode som operasjonshendelser, men den bruker ulike målinger. Det finnes tre hovedmåletyper: produktkostnadsantall, produktkostnad og avvik.

Underfinanskontoer brukes til å klassifisere målingene ytterligere. Det kan være flere finanskontoer. Disse finanskontoene er koblet til den juridiske enheten der dokumentet er angitt. Du kan vise hendelsene og målene for hver hovedbok ved å endre verdien i **Hovedbok**-feltet.

### <a name="cost-element"></a>Kostnadselement

På grunnlag av policyen for kostnadselement som er knyttet til finanskontoen, tilordner systemet et kostnadselement til hver beregnede driftshendelsesmåling som påvirker lagerkosten. Disse målene omfatter utvidet pris, rabatt, rabattprosent og linjetillegg.

### <a name="measurement-line-details"></a>Detaljer om målingslinje

Kategorien **Oversikt** viser detaljene for de tilknyttede policyene. Kostnadsobjektdimensjonene viser kostnadsobjektet, basert på kostnadsobjektpolicyen. Bestemte identifikasjonsdimensjoner viser partinummeret hvis kostnadsflytantagelsen er *Spesifikk – Parti*.

### <a name="purchase-invoice"></a>Innkjøpsfaktura

Poster fakturaen på vanlig måte. Deretter, i handlingsruten i fanen **Faktura** i gruppen **Journaler**, velger du **Faktura** for å åpne fakturajournalen. En operasjonshendelse og en Globalt lagerregnskap-hendelse genereres for hver linje. Derfor velger du kategorien **Linjer**, og deretter velger du **Lager \> Hendelser og målinger** for å åpne **Hendelser og målinger**-siden. Siden **Hendelser og målinger** viser samme målingstype. Med fordi siden viser forskjellig målingsrolle og målmodifikator, er innvirkningen på agenten (juridisk enhet) forskjellig.

Velg **Hendelser og målinger for Globalt lagerregnskap** for å vise Globalt lagerregnskap-hendelsen. Lagerantallet og kostnaden flyter nå ut fra underfinanskontoen for *mottatte varer som ikke er fakturert* og inn i underfinanskontoen for *kjøpte varers kost*.
