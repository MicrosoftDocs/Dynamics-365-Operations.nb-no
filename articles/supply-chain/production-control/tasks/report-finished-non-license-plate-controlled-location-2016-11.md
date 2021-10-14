---
title: Rapportere som ferdig til en lokasjon som ikke er kontrollert av nummerskilt (program, mai 2016)
description: Denne oppgaveveiledningen viser et eksempel på rapportering som ferdig til en lokasjon som ikke er nummerskiltkontrollert.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f891b2e3b20993a08138dfac1aed4f4bab33c6b1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576718"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a>Rapportere som ferdig til en lokasjon som ikke er kontrollert av nummerskilt (program, mai 2016)

[!include [banner](../../includes/banner.md)]

Denne oppgaveveiledningen viser et eksempel på rapportering som ferdig til en lokasjon som ikke er nummerskiltkontrollert. En gjeldende arbeidspolicy er en forutsetning for denne oppgaven. En tidligere oppgaveveiledning viste oppsettet av arbeidspolicyen. Denne oppgaveveiledningen krever Dynamics AX 7.0.1 eller senere.




## <a name="set-up-an-output-location"></a>Definere en utleveringslokasjon
1. Gå til Organisasjonsstyring > Ressurser > Ressursgrupper.
2. Velg ressursgruppe 5102 i listen.
3. Klikk på Rediger.
4. Angi 51 i feltet Utleveringslager.
5. Angi 001 i feltet Utleveringslokasjon.
    * Lokasjonen 001 er ikke en nummerskiltkontrollert lokasjon. Du kan definere en utleveringslokasjon uten nummerskilt hvis det finnes en gjeldende arbeidspolicy for lokasjonen.  

## <a name="create-a-production-order-and-report-it-as-finished"></a>Opprette en produksjonsordre og rapportere den som avsluttet
1. Lukk siden.
2. Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.
3. Klikk på Ny produksjonsordre.
4. Angi L0101 i feltet Varenummer.
5. Klikk på Opprett.
6. Klikk på Produksjonsordre i handlingsruten.
7. Klikk på Estimer.
8. Klikk på OK.
9. Klikk på Start.
10. Klikk på fanen Generelt.
11. Velg Aldri i feltet Automatisk stykklisteforbruk.
12. Klikk på OK.
13. Klikk på Rapporter som fullført.
14. Klikk på fanen Generelt.
15. Velg Ja i feltet Godtar feil.
16. Klikk på OK.
17. Klikk på Lager i handlingsruten.
18. Klikk på Arbeidsdetaljer.
    * Når produksjonsordren ble rapportert som fullført, ble det ikke generert arbeid for plassering. Dette skjer fordi en arbeidspolicy er definert som hindrer at arbeidet blir generert når produktet L0101 rapporteres som ferdig til lokasjon 001.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]