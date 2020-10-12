---
title: Scenarier som støttes for oppsett av dobbel skriving
description: Dette emnet beskriver scenariene som støttes for oppsett av dobbel skriving.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b4f69e7933bc5a50cccad6911c99cf08d2768578
ms.sourcegitcommit: b3df62842e62234e8eaa16992375582518976131
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/17/2020
ms.locfileid: "3818602"
---
# <a name="supported-scenarios-for-dual-write-setup"></a>Scenarier som støttes for oppsett av dobbel skriving

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Du kan opprette en dobbelt skrive-tilkobling mellom et Finance and Operations-miljø og et Common Data Service-miljø.

+ Et **Finance and Operations-miljø** gir den underliggende plattformen for **Finance and Operations-apper** (for eksempel Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management og Dynamics 365 Retail).
+ Et **Common Data Service-miljø** gir den underliggende plattformen for **modelldrevne apper i Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).

>[!IMPORTANT]
>Human Resources i Finance and Operations støtter tilkoblinger med dobbel skriving, men Dynamics 365 Human Resources-appen gjør ikke det.

Installasjonsmekanismen varierer, avhengig av abonnementet og miljøet.

+ Når det gjelder nye forekomster av Finance and Operations-apper, begynner oppsettet av en tilkobling med dobbel skriving i Microsoft Dynamics Lifecycle Services (LCS). Hvis du har en lisens for Power Platform, vil du få et nytt Common Data Service-miljø hvis leieren din ikke har et.
+ For eksisterende forekomster av Finance and Operations-apper begynner oppsettet av en tilkobling med dobbel skriving i Finance and Operations-miljøet.

Følgende oppsettscenarier støttes:

+ [En ny Finance and Operations-appforekomst og en ny modelldrevet appforekomst](#new-new)
+ [En ny Finance and Operations-appforekomst og en eksisterende modelldrevet appforekomst](#new-existing)
+ [En ny Finance and Operations-appforekomst som har demodata og en ny modelldrevet appforekomst](#new-demo-new)
+ [En ny Finance and Operations-appforekomst som har demodata og en eksisterende modelldrevet appforekomst](#new-demo-existing)
+ [En eksisterende Finance and Operations-appforekomst og en ny eller eksisterende modelldrevet appforekomst](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a>En ny Finance and Operations-appforekomst og en ny modelldrevet appforekomst

Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som ikke har noen data, og en ny forekomst av en modelldrevet app i Dynamics 365, følger du fremgangsmåten i [Oppsett av dobbel skriving fra Lifecycle Services](lcs-setup.md). Når tilkoblingsoppsettet er fullført, skjer følgende handlinger automatisk:

- Et nytt, tomt Finance and Operations-miljø er klargjort.
- En ny, tom forekomst av en modelldrevet app er klargjort, der CRM-hovedløsningen er installert.
- Det opprettes en dobbel skriving-tilkobling for DAT-firmadata.
- Enhetstilordninger er aktivert for direkte synkronisering.

Begge miljøene er så klare for direkte synkronisering av data.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a>En ny Finance and Operations-appforekomst og en eksisterende modelldrevet appforekomst

Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som ikke har noen data, og en eksisterende forekomst av en modelldrevet app i Dynamics 365, følger du fremgangsmåten i [Oppsett av dobbel skriving fra Lifecycle Services](lcs-setup.md). Når tilkoblingsoppsettet er fullført, skjer følgende handlinger automatisk:

- Et nytt, tomt Finance and Operations-miljø er klargjort.
- Det opprettes en dobbel skriving-tilkobling for DAT-firmadata.
- Enhetstilordninger er aktivert for direkte synkronisering.

Begge miljøene er så klare for direkte synkronisering av data.

Følg denne fremgangsmåten for å synkronisere de eksisterende Common Data Service-dataene med Finance and Operations-appen.

1. Opprette et nytt firma i Finance and Operations-appen.
2. Legg til firmaet i oppsettet for dobbelt skriving-tilkobling.
3. [Starte opp](bootstrap-company-data.md) Common Data Service-dataene ved hjelp av en ISO-firmakode (International Organization for Standardization) på tre tegn.

Fordi dobbel skriving er i modus for direkte synkronisering, begynner dataene fra Common Data Service å strømme til Finance and Operations-appen automatisk.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a>En ny Finance and Operations-appforekomst som har demodata og en ny modelldrevet appforekomst

Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som har demodata og en ny forekomst av en modelldrevet app i Dynamics 365, følger du fremgangsmåten i delen [En ny Finance and Operations-appforekomst og en ny modelldrevet appforekomst](#new-new) tidligere i dette emnet. Når tilkoblingsoppsettet er fullført, følger du denne fremgangsmåten hvis du vil synkronisere demonstrasjonsdataene med den modelldrevne appen.

1. Åpne Finance and Operations-appen fra LCS-siden, logg på og gå til **Databehandling \> Dobbel skriving**.
2. Kjør **Innledende synkronisering**-funksjonaliteten for enhetene du vil synkronisere data for.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a>E<a id="new-demo-existing"></a>En ny Finance and Operations-appforekomst som har demodata og en eksisterende modelldrevet appforekomst

Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som har en eksisterende forekomst av en modelldrevet app i Dynamics 365, følger du fremgangsmåten i delen [En ny Finance and Operations-appforekomst og en eksisterende modelldrevet appforekomst](#new-existing) tidligere i dette emnet. Når tilkoblingsoppsettet er fullført, følger du denne fremgangsmåten hvis du vil synkronisere demonstrasjonsdataene med den modelldrevne appen.

1. Åpne Finance and Operations-appen fra LCS-siden, logg på og gå til **Databehandling \> Dobbel skriving**.
2. Kjør **Innledende synkronisering**-funksjonaliteten for enhetene du vil synkronisere data for.

Følg denne fremgangsmåten for å synkronisere de eksisterende Common Data Service-dataene med Finance and Operations-appen.

1. Opprette et nytt firma i Finance and Operations-appen.
2. Legg til firmaet i oppsettet for dobbelt skriving-tilkobling.
3. [Starte opp](bootstrap-company-data.md) Common Data Service-dataene ved hjelp av en ISO-firmakode på tre tegn.

Fordi dobbel skriving er i modus for direkte synkronisering, begynner dataene fra Common Data Service å strømme til Finance and Operations-appen automatisk.

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a>En eksisterende Finance and Operations-appforekomst og en ny eller eksisterende modelldrevet appforekomst

Oppsettet av en dobbel skriving-tilkobling mellom en eksisterende forekomst av en Finance and Operations-app og en ny eller eksisterende forekomst av en modelldrevet app i Dynamics 365 forekommer i Finance and Operation-miljøet.

1. Angi tilkoblingen fra Finance and Operations-appen.
2. Hvis du vil synkronisere de eksisterende Common Data Service-dataene til Finance and Operations-appen, [starter du opp](bootstrap-company-data.md) Common Data Service-dataene ved hjelp av en ISO-firmakode på tre bokstaver.

Fordi dobbel skriving er i modus for direkte synkronisering, begynner dataene fra Common Data Service å strømme til Finance and Operations-appen automatisk.
