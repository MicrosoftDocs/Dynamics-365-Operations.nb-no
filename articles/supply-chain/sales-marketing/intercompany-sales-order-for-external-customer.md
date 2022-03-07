---
title: Opprette og fakturere en konsernintern salgsordre for en ekstern kunde
description: Dette emnet forklarer hvordan du oppretter og fakturerer en konsernintern salgsordre for en ekstern kunde
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 72273a125da2e6c4a2fc16b449cd5077f3d767df
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548441"
---
# <a name="create-and-invoice-an-intercompany-sales-order-for-an-external-customer"></a>Opprette og fakturere en konsernintern salgsordre for en ekstern kunde

[!include [banner](../../includes/banner.md)]

Du kan bruke konsernintern handel til å registrere salget av et produkt fra en juridisk enhet til en annen juridisk enhet som er i samme organisasjon.

Når du oppretter den opprinnelige salgsordren, kan du opprette en konsernintern bestilling automatisk for den konserninterne leverandøren. Dette oppretter automatisk en konsernintern salgsordre i den juridiske enheten til den konserninterne leverandøren.

Illustrasjonen nedenfor viser transaksjonsflyten når du oppretter en salgsordre for en ekstern kunde, men produktet må bestilles fra en annen juridisk enhet i organisasjonen før du kan levere produktet til kunden. I dette tilfellet opprettes en konsernintern bestilling for leverandørkontoen som representerer den juridiske enheten. Dette fører til at det opprettes en konsernintern salgsordre i den andre juridiske enheten for kundekontoen som representerer din juridiske enhet. Når en konsernintern bestilling faktureres, posterer fakturaen automatisk for den opprinnelige salgsordren hvis det er en direktelevering.

![Konsernintern ekstern salgsprosess](media/intercompanyexternalsalesprocess.png)

Hvis du bruker direktelevering og velger **Følgeseddel** i **Antall**-feltet på siden **Postering av faktura**, blir den konserninterne leverandørfakturaen basert på den konserninterne produktkvitteringen som ble postert tidligere.

## <a name="prerequisites"></a>Forutsetninger

Før du begynner, må du kontrollere at følgende forhåndskrav er oppfylt, slik at du kan postere og skrive ut de konserninterne fakturaene automatisk.

1. Gå til **Salg og markedsføring \> Kunder \> Alle kunder**.
1. Velg **Konsernintern** i fanen **Generelt** i handlingsruten.
1. Gå til **Innkjøp og leverandører \> Leverandører \> Alle leverandører**.
1. Velg **Konsernintern** i fanen **Generelt** i handlingsruten.
1. På **Konsernintern**-siden for leverandøren eller kunden, i området **Bestillingspolicyer** i feltgruppen **Konserninterne bestillinger (direktelevering)**, merker du av for **Poster faktura automatisk**.
1. I området **Bestillingspolicyer** i feltgruppen **Opprinnelig salgsordre (direktelevering)** merker du av for **Poster faktura automatisk**. Velg denne avmerkingsboksen hvis du vil at fakturaen for den opprinnelige salgsordren skal skrives ut automatisk når du posterer den konserninterne leverandørfakturaen.

> [!NOTE]
> Utskriftsinnstillingene for fakturaen bestemmes av oppsettet for modulen, dokumentet eller transaksjonen, på siden **Oppsett for utskriftsbehandling**.

## <a name="create-an-original-sales-order-for-an-external-customer"></a>Opprette en opprinnelig salgsordre for en ekstern kunde

Gjør følgende i juridisk enhet A. Dette tilsvarer merket 1 i illustrasjonen.

1. Gå til **Kunde \> Salgsordrer \> Alle salgsordrer**.
1. Opprett den opprinnelige salgsordren fra **Alle salgsordrer**-listesiden. Feltverdiene kopieres fra kundekontoen til salgsordren.
1. På **Salgsordre**-siden velger du **Topptekstvisning** i handlingsruten.
1. I hurtigfanen for **Konserninterne innstillinger** merker du av for **Opprett konserninterne ordrer automatisk**.
1. Hvis du vil at den konserninterne leverandøren skal levere varen direkte til den eksterne kunden, merker du av for **Direktelevering**.
1. Når du er ferdig med å registrere salgsordren, lukker du **Salgsordre**-siden.

Den konserninterne bestillingen opprettes automatisk for alle varene som er tilordnet en konsernintern leverandør, og deretter opprettes den konserninterne salgsordren. En informasjonsmelding forteller deg at det er opprettet en konsernintern bestilling og konsernintern salgsordre. Meldingen inneholder også koblinger til disse ordrene. Hvis en vare ikke finnes, vises det en rød advarsel som betyr at ordreopprettingsprosessen ikke ble fullført.

> [!NOTE]
> Hvis du oppretter ordrer i flere ulike juridiske enheter, og varene ikke finnes i den ene av de juridiske enhetene, stopper ordreopprettelsesprosessen, selv for de juridiske enhetene som kan oppfylle ordrene sine.

## <a name="invoice-an-intercompany-sales-order"></a>Fakturere en konsernintern salgsordre

Når en konsernintern salgsordre faktureres, faktureres den tilsvarende konserninterne bestillingen automatisk. Hvis den opprinnelige salgsordren er en direkteleveringsordre, faktureres deretter den opprinnelige salgsordren automatisk.

Gjør følgende i juridisk enhet B. Dette tilsvarer merket 2 i illustrasjonen.

1. Gå til **Kunde \> Salgsordrer \> Alle salgsordrer**.
1. På listesiden **Alle salgsordrer** velger du den konserninterne salgsordren.
1. Velg kategorien **Faktura** i handlingsruten, og velg deretter **Faktura**.
1. Merk av i **Postering**-avmerkingsboksen.
1. Velg salgsordren, og klikk deretter **OK**.

Kundefakturaen for den konserninterne salgsordren posteres automatisk i juridisk enhet B. Den konserninterne leverandørfakturaen opprettes deretter automatisk og posteres i juridisk enhet A. Hvis den opprinnelige salgsordren er definert som en direktelevering, opprettes kundefakturaen for den opprinnelige salgsordren i juridisk enhet A.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
