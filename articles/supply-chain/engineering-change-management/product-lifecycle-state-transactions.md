---
title: Produktstatuser og transaksjoner
description: Dette emnet beskriver hvordan du kan kontrollere hvilke transaksjoner som er tillatt for hver status når et teknisk produkt går gjennom livssyklusen.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 69ee39479424c1b629388c18e8bfefd023036d22
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/29/2020
ms.locfileid: "4434860"
---
# <a name="product-lifecycle-states-and-transactions"></a>Produktstatuser og transaksjoner

[!include [banner](../includes/banner.md)]

Når et teknisk produkt går gjennom livssyklusen, er det viktig at du kan kontrollere hvilke transaksjoner som er tillatt for hver status. Produkter som ennå ikke er i en moden status, bør for eksempel ikke legges på en salgsordre. Hvis et produkt nærmer seg slutten av levetiden, kan det være lurt å styre innflyten av dette produktet.

Når det gjelder et teknisk produkt, er endringer i statusen koblet til produktets tekniske versjoner. Derfor kan produktets status også kobles til de tekniske versjonene. Når produktstatusen er koblet til en teknisk versjon, kan du bruke statusen til å kontrollere hvilke transaksjoner som er tillatt for den tekniske versjonen.

## <a name="create-and-manage-product-lifecycle-states"></a>Opprett og administrer produktstatuser

Hvis du vil arbeide med produktstatuser, går du til **Behandling av teknisk endring \> Oppsett \> Produktstatus**. Følg deretter ett av disse trinnene.

- Hvis du vil opprette en ny status, velger du **Nytt** i handlingsruten, og deretter angir du feltene som beskrevet i følgende underavsnitt.
- Hvis du vil redigere en eksisterende status, velger du det i listeruten, velger **Rediger** i handlingsruten og angir deretter feltene som beskrevet i følgende underavsnitt.
- Hvis du vil slette en eksisterende status, velger du det i listeruten, og deretter velger du **Slett** i handlingsruten.

> [!NOTE]
> Tekniske produkter bruker de samme produktstatusene som standard (ikke-tekniske) produkter. Du kan også åpne **Produktstatus**-siden som er beskrevet i dette emnet, ved å gå til **Behandling av produktinformasjon \> Oppsett \> Produktstatus**. Hvis du vil ha mer informasjon om produktstatuser, for både tekniske produkter og standardprodukter, kan du se [Oversikt over produktstatus](../pim/product-lifecycle.md).

### <a name="header"></a>Hode

Angi følgende felter i toppteksten til en produktstatus.

| Felt | beskrivelse |
|---|---|
| Status | Angi et navn for produktstatusen. |
| beskrivelse | Angi en beskrivelse av produktstatusen. |

### <a name="general-fasttab"></a>Hurtigfanen Generelt

Angi følgende felter i hurtigfanen **Generelt**.

| Felt | beskrivelse |
|---|---|
| Standard når frigitt til en juridisk enhet | For standardprodukter setter du dette alternativet til *Ja* hvis denne statusen skal brukes på alle produkter som standard når de først er frigitt. Sett det til *Nei* hvis denne statusen skal brukes manuelt senere.<p>Denne innstillingen gjelder ikke tekniske produkter. Statusen til en teknisk produktversjon etter at den er opprettet i det tekniske firmaet, er angitt i kategorien for teknisk produkt. Når produktet frigis til et driftsfirma, kopieres statusen til produktet. Med andre ord har det samme status som det hadde i det tekniske firmaet, når et teknisk produkt utgis til et driftsfirma. Statusen kan overskrives i driftsfirmaet.</p> |
| Er aktiv for planlegging | Sett dette alternativet til *Ja* for å ta med produkter som er i denne statusen, i beregninger med nivåene hovedplanlegging og stykkliste. Sett det til *Nei* for å utelate produkter som er i denne statusen, fra beregningene. |

### <a name="enabled-business-processes-fasttab"></a>Hurtigfanen Aktiverte forretningsprosesser

Bruk hurtigfanen **Aktiverte forretningsprosesser** til å styre hvilke av de tilgjengelige forretningsprosessene som kan brukes med produkter i gjeldende status. Prosessene som vises på denne hurtigfanen, finnes automatisk på følgende måte:

- Første gang du lagrer en ny status, laster siden inn forretningsprosessene som for øyeblikket er tilgjengelige.
- Hvis du legger til nye forretningsprosesser i systemet, kan du oppdatere listen i hurtigfanen **Aktiverte forretningsprosesser** for en eksisterende status ved å velge **Se etter oppdateringer** i handlingsruten.

Følgende felter er tilgjengelige for hver prosess som er oppført på hurtigfanen **Aktiverte forretningsprosesser**.

| Felt | beskrivelse |
|---|---|
| Behandle | Dette skrivebeskyttede feltet viser navnet på en eksisterende forretningsprosess. |
| Prosessområde | Dette skrivebeskyttede feltet viser navnet på et eksisterende forretningsområde. |
| Polise | Velg en av følgende verdier for å kontrollere om og hvordan gjeldende prosess skal være tillatt for produkter som er i denne statusen:<ul><li>**Aktivert** – Forretningsprosessen er tillatt.</li><li>**Blokkert** – Prosessen er ikke tillatt. Hvis en bruker prøver å bruke prosessen for et produkt i denne statusen, vil systemet blokkere forsøket og vise en feil i stedet. Du kan for eksempel blokkere at produkter som nærmer seg slutten av levetiden, kan kjøpes.</li><li>**Aktivert med advarsel** – Prosessen er tillatt, men det vil bli vist en advarsel. Det kan for eksempel hende at du vil at et prototypprodukt skal plasseres på en produksjonsordre som opprettes av avdelingen for forskning og utvikling. Andre avdelinger bør imidlertid være oppmerksomme på at de ikke bør produsere produktet ennå.</li></ul> |

Hvis du legger til flere statusregler som en tilpasning, kan du vise disse reglene i brukergrensesnittet (UI) ved å velge **Oppdater prosesser** i den øvre ruten. **Oppdater prosesser**-knappen er bare tilgjengelig for administratorer.
