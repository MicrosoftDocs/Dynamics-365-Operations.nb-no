---
title: Initialisere data for utgangsverdi i nye Commerce-miljøer
description: Denne artikkelen beskriver dataene som opprettes som en del av initialiseringsprosessen for Dynamics 365 Commerce.
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
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8fd0b2743deab758538922f312853b622a512c0a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000751"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a>Initialisere data for utgangsverdi i nye Commerce-miljøer

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver dataene som opprettes som en del av initialiseringsprosessen for Dynamics 365 Commerce.

Etter at handelsløsningen er distribuert via Microsoft Dynamics Lifecycle Services (LCS) må du initialisere handelskonfigurasjonen for å opprette grunnleggende konfigurasjonsdata.

> [!IMPORTANT]
> Før du initialiserer handelskonfigurasjonen, må du kontrollere at du har angitt et språk og postadresse for hver juridiske enhet der du vil definere butikker. Dette trinnet må fullføres for hver juridiske enhet som du bruker for handel.

Bruk følgende fremgangsmåte for å initialisere konfigurasjonen.

1. Start Handel-klienten.
2. Klikk på **Detaljhandel og handel** &gt; **Hovedkvarteroppsett** &gt; **Parametere** &gt; **Handelsparametere**.
3. Klikk **Initialiser**.

Initialisering oppretter følgende standardkonfigurasjonsdata:

- Jobber og deljobber i Handel-planlegger
- Handelskanalskjema
- Handelsdistribusjonstidsplaner
- Standard skjermoppsett, som inkluderer knappegrupper, bilder og temaer
- Informasjon om tidssone
- Salgsstedsoperasjoner
- Salgsstedstillatelser
- Kanalrapporter
- Attributtmetadata
- Maler for validering av enhet
- Satsvis jobb for å tømme økthistorikk for Commerce Data Exchange

I tillegg aktiveres logging som er knyttet til betalingskortbransjen (PCI) for Handel-databasen.

> [!NOTE]
> Det finnes et alternativ for å konfigurere Handel-planlegger separat. Dette alternativet lar deg tilbakestille Handel-planleggerkonfigurasjonen til standardinnstillingene.

Når initialiseringen er fullført, må du konfigurere tilleggsdata for handel. Her er noen eksempler:

- Handelsparametere
- Parametre for planlegging av handel
- Handelskanaler
- Kasser og enheter
- Assortement
