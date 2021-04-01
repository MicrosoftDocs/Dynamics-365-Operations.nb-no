---
title: Kontrollere lagertilgjengeligheten
description: Denne fremgangsmåten viser hvordan du kontrollerer beholdning og fysisk lagerbeholdning for et bestemt varenummer.
author: ShylaThompson
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2153117d9c921b43658edeade49a8403553e371
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238068"
---
# <a name="check-the-availability-of-stock"></a>Kontrollere lagertilgjengeligheten

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du kontrollerer beholdning og fysisk lagerbeholdning for et bestemt varenummer. Den viser også hvordan du henter forsyningsinformasjon som er knyttet til en vare. Fysisk lagerbeholdning er lagerbeholdningen som er tilgjengelig – det vil si den er kjøpt, mottatt og registrert. Lagerbeholdningen inkluderer den tilgjengelige lagerbeholdningen, men også lageret som er bestilt og forventet, men ennå ikke er mottatt eller registrert. Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Hvis du bruker USMF, kan du bruke eksempelverdiene som vises. Disse oppgavene vil vanligvis utføres av en lagermedarbeider.


## <a name="check-on-hand-inventory-for-an-item"></a>Kontrollere lagerbeholdning for en vare
1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Forespørsler og rapporter > Lagerbeholdning**.
2. Velg **Varenummer**-raden. Hvis du vil spørre om lagerbeholdning etter varenummer, merker du raden der tabellen er satt til **Lagerbeholdning** og Felt er satt til **Varenummer**.
3. Velg varen du vil utføre spørringer for, i **Kriterier**-feltet. Hvis du bruker demonstrasjonsdatafirmaet USMF, kan du velge M9201.  
4. Klikk på **OK**.
5. Klikk på **Dimensjoner** i **handlingsruten**. I fanen **Dimensjoner** kan du velge hvor mange detaljer du vil se om lagerbeholdningen. Hvis du trenger data som er relatert til reservering, må du vise alle lagerdimensjoner for varer som bruker avanserte lagerprosesser (WMS).
6. Klikk på **OK**.
7. Klikk på **Relatert informasjon** i **handlingsruten**. Hvis du ikke ser dette alternativet, må du kanskje klikke ellipseknappen (...) for å se alternativer for flere handlinger.
8. Klikk på **Forsyningsoversikt**. fanen **Forsyningsoversikt** gir forsyningsinformasjonen for en bestemt vare, for eksempel antallet på lager, leveringstid og leverandørinformasjon.  
9. Vis **Beholdning**-delen.
10. Vis **Leverandør**-delen.
11. Lukk siden.
12. Lukk siden.

## <a name="check-physical-on-hand-inventory"></a>Kontrollere fysisk lagerbeholdning
1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Forespørsler og rapporter > Fysisk lagerbeholdning**.
2. Skriv inn en verdi i **Varenummer**-feltet. Du kan bruke feltene Område og Lager til å filtrere listen over elementer. 
3. Oppdater siden.
4. I **handlingsruten** klikker du på **Visningsdimensjoner**. I fanen Dimensjonsvisning kan du velge hvor mange detaljer du vil se om lagerbeholdningen.
5. Klikk på **OK**.
6. Lukk siden.

## <a name="check-on-hand-inventory-by-location"></a>Kontrollere lagerbeholdning etter lokasjon
1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Forespørsler og rapporter > Beholdning etter lokasjon**.
2. Skriv inn en verdi i **Lager**-feltet. Hvis du bruker demonstrasjonsdatafirmaet USMF, kan du bruke "51".  
3. Oppdater siden.
4. Klikk på **Visningsdimensjoner**.
5. Klikk på **OK**.
6. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]