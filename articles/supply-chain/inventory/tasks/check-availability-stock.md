--- 
title: Kontrollere lagertilgjengeligheten
description: "Denne fremgangsmåten viser hvordan du kontrollerer beholdning og fysisk lagerbeholdning for et bestemt varenummer."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: 
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 62338fe11c30781f264e626fad835a2ba9dca837
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="check-the-availability-of-stock"></a>Kontrollere lagertilgjengeligheten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du kontrollerer beholdning og fysisk lagerbeholdning for et bestemt varenummer. Den viser også hvordan du henter forsyningsinformasjon som er knyttet til en vare. Fysisk lagerbeholdning er lagerbeholdningen som er tilgjengelig – det vil si den er kjøpt, mottatt og registrert. Lagerbeholdningen inkluderer den tilgjengelige lagerbeholdningen, men også lageret som er bestilt og forventet, men ennå ikke er mottatt eller registrert. Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Hvis du bruker USMF, kan du bruke eksempelverdiene som vises. Disse oppgavene vil vanligvis utføres av en lagermedarbeider.


## <a name="check-on-hand-inventory-for-an-item"></a>Kontrollere lagerbeholdning for en vare
1. Gå til Lagerstyring > Forespørsler og rapporter > Lagerbeholdning.
2. Velg varenummerraden.
    * Hvis du vil spørre om lagerbeholdning etter varenummer, merker du raden der tabellen er satt til Lagerbeholdning og Felt er satt til Varenummer.  
3. Velg varen du vil utføre spørringer for, i Kriterier-feltet.
    * Hvis du bruker demonstrasjonsdatafirmaet USMF, kan du velge M9201.  
4. Klikk OK.
5. Klikk Dimensjoner.
    * I kategorien Dimensjoner kan du velge hvor mange detaljer du vil se om lagerbeholdningen. Hvis du trenger data som er relatert til reservering, må du vise alle lagerdimensjoner for varer som bruker avanserte lagerprosesser (WHS).  
6. Klikk OK.
7. Klikk Relatert informasjon i handlingsruten.
    * Hvis du ikke ser dette, må du kanskje klikke ellipseknappen (...) for å se alternativer for flere handlinger.  
8. Klikk Forsyningsoversikt.
    * Kategorien Forsyningsoversikt gir forsyningsinformasjonen for en bestemt vare, for eksempel antallet på lager, leveringstid og leverandørinformasjon.  
9. Vis Beholdning-delen.
10. Vis Leverandør-delen.
11. Lukk siden.
12. Lukk siden.

## <a name="check-physical-on-hand-inventory"></a>Kontrollere fysisk lagerbeholdning
1. Gå til Lagerstyring > Forespørsler og rapporter > Fysisk lagerbeholdning.
2. Skriv inn en verdi i Varenummer-feltet.
    * Du kan bruke feltene Område og Lager til å filtrere listen over elementer.  
3. Oppdater siden.
4. Klikk Visningsdimensjoner.
    * I kategorien Dimensjonsvisning kan du velge hvor mange detaljer du vil se om lagerbeholdningen.  
5. Klikk OK.
6. Lukk siden.

## <a name="check-on-hand-inventory-by-location"></a>Kontrollere lagerbeholdning etter lokasjon
1. Gå til Lagerstyring > Forespørsler og rapporter > Beholdning etter lokasjon.
2. Skriv inn en verdi i Lager-feltet.
    * Hvis du bruker demonstrasjonsdatafirmaet USMF, kan du bruke "51".  
3. Oppdater siden.
4. Klikk Visningsdimensjoner.
5. Klikk OK.
6. Lukk siden.


