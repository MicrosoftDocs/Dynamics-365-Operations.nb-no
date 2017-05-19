---
title: "Initialisere utgangsverdidata i et nytt miljø for detaljhandel"
description: Denne artikkelen beskriver dataene som opprettes som en del av initialiseringsprosessen for Microsoft Dynamics 365 Operations - Retail.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: b5290bb62ab8ad71b06b0478ccaf6dbb61454170
ms.contentlocale: nb-no
ms.lasthandoff: 04/26/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Initialisere utgangsverdidata i et nytt miljø for detaljhandel

[!include[banner](includes/banner.md)]


Denne artikkelen beskriver dataene som opprettes som en del av initialiseringsprosessen for Microsoft Dynamics 365 Operations - Retail.

Etter at detaljhandelsløsningen er distribuert via Microsoft Dynamics Lifecycle Services (LCS) må du initialisere detaljhandelskonfigurasjonen for å opprette grunnleggende konfigurasjonsdata. **Viktig:** Før du initialiserer detaljhandelskonfigurasjonen må du kontrollere at du har angitt et språk og postadresse for hver juridiske enhet der du vil definere detaljhandelsbutikker. Dette trinnet må fullføres for hver juridiske enhet som du bruker for detaljhandel. Bruk følgende fremgangsmåte for å initialisere detaljhandelskonfigurasjonen.

1.  Start Dynamics 365 for Operations-klienten.
2.  Klikk **Detaljhandel og handel** &gt; **Hovedkvarteroppsett** &gt; **Parametere** &gt; **Detaljhandelsparametere**.
3.  Klikk **Initialiser**.

Initialisering oppretter følgende standardkonfigurasjonsdata:

-   Detaljhandel Planlegger jobber og deljobber
-   Handelskanalskjema
-   Distribusjonstidsplaner for detaljhandel
-   Standard skjermoppsett, som inkluderer knappegrupper, bilder og temaer
-   Informasjon om tidssone
-   Salgsstedsoperasjoner
-   Salgsstedstillatelser
-   Kanalrapporter
-   Attributtmetadata
-   Maler for validering av enhet
-   Satsvis jobb for å tømme økthistorikk for Commerce Data Exchange

I tillegg aktiveres logging som er knyttet til betalingskortbransjen (PCI) for Dynamics 365 for Operations-databasen. **Obs!** Det finnes et alternativ for å konfigurere Detaljhandel Planlegger separat. Dette alternativet lar deg tilbakestille Detaljhandel Planlegger-konfigurasjonen til standardinnstillingene. Når initialiseringen er fullført, må du konfigurere tilleggsdata for detaljhandel. Her er noen eksempler:

-   Detaljhandelsparametere
-   Parametre for Detaljhandel Planlegger
-   Detaljhandelskanaler
-   Kasser og enheter
-   Assortement





