---
title: Initialisere utgangsverdidata i nye miljøer for detaljhandel
description: Denne artikkelen beskriver dataene som opprettes som en del av initialiseringsprosessen for Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 52f0c52748958f0bebb6c40df01cfac10c0ed427
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "327901"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a>Initialisere data for utgangsverdi i nye Retail-miljøer

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver dataene som opprettes som en del av initialiseringsprosessen for Microsoft Dynamics 365 for Retail.

Etter at detaljhandelsløsningen er distribuert via Microsoft Dynamics Lifecycle Services (LCS) må du initialisere detaljhandelskonfigurasjonen for å opprette grunnleggende konfigurasjonsdata.

> [!IMPORTANT]
> Før du initialiserer detaljhandelskonfigurasjonen, må du kontrollere at du har angitt et språk og postadresse for hver juridiske enhet der du vil definere detaljhandelsbutikker. Dette trinnet må fullføres for hver juridiske enhet som du bruker for detaljhandel.

Bruk følgende fremgangsmåte for å initialisere detaljhandelskonfigurasjonen.

1. Start Dynamics 365 for Retail-klienten.
2. Klikk **Detaljhandel** &gt; **Hovedkvarteroppsett** &gt; **Parametere** &gt; **Detaljhandelsparametere**.
3. Klikk **Initialiser**.

Initialisering oppretter følgende standardkonfigurasjonsdata:

- Detaljhandel Planlegger jobber og deljobber
- Handelskanalskjema
- Distribusjonstidsplaner for detaljhandel
- Standard skjermoppsett, som inkluderer knappegrupper, bilder og temaer
- Informasjon om tidssone
- Salgsstedsoperasjoner
- Salgsstedstillatelser
- Kanalrapporter
- Attributtmetadata
- Maler for validering av enhet
- Satsvis jobb for å tømme økthistorikk for Commerce Data Exchange

I tillegg aktiveres logging som er knyttet til betalingskortbransjen (PCI) for Dynamics 365 for Retail-databasen.

> [!NOTE]
> Det finnes et alternativ for å konfigurere Detaljhandel Planlegger separat. Dette alternativet lar deg tilbakestille Detaljhandel Planlegger-konfigurasjonen til standardinnstillingene.

Når initialiseringen er fullført, må du konfigurere tilleggsdata for detaljhandel. Her er noen eksempler:

- Detaljhandelsparametere
- Parametre for Detaljhandel Planlegger
- Detaljhandelskanaler
- Kasser og enheter
- Assortement
