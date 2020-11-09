---
title: Veiledning for hvordan du konfigurerer dobbel skriving
description: Dette emnet beskriver scenariene som støttes for oppsett av dobbel skriving.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088512"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a>Veiledning for hvordan du konfigurerer dobbel skriving

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Du kan opprette en dobbelt skrive-tilkobling mellom et Finance and Operations-miljø og et Common Data Service-miljø.

+ Et **Finance and Operations-miljø** gir den underliggende plattformen for **Finance and Operations-apper** (for eksempel Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management og Dynamics 365 Retail).
+ Et **Common Data Service-miljø** gir den underliggende plattformen for **kundeengasjementsapper** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).

>[!IMPORTANT]
>Human Resources i Finance and Operations støtter tilkoblinger med dobbel skriving, men Dynamics 365 Human Resources-appen gjør ikke det.

Installasjonsmekanismen varierer, avhengig av abonnementet og miljøet.

+ Når det gjelder nye forekomster av Finance and Operations-apper, begynner oppsettet av en tilkobling med dobbel skriving i Microsoft Dynamics Lifecycle Services (LCS). Hvis du har en lisens for Power Platform, vil du få et nytt Common Data Service-miljø hvis leieren din ikke har et.
+ For eksisterende forekomster av Finance and Operations-apper begynner oppsettet av en tilkobling med dobbel skriving i Finance and Operations-miljøet.

Før du starter med å skrive på en enhet, kan du kjøre en første synkronisering for å behandle eksisterende data på begge sider av Finance and Operations-apper og kundeengasjementsapper. Du kan hoppe over den innledende synkroniseringen hvis du ikke trenger å synkronisere data mellom de to miljøene.

Ved hjelp av en innledende synkronisering kan du kopiere eksisterende data fra én app til en annen toveis. Det finnes flere forskjellige installasjonsscenarioer, avhengig av hvilke miljøer du allerede har, og hvilken type data som finnes i miljøene.

Følgende oppsettscenarier støttes:

+ [En ny Finance and Operations-appforekomst og en ny kundeengasjementsapp-forekomst](#new-new)
+ [En ny Finance and Operations-appforekomst og en eksisterende kundeengasjementsapp-forekomst](#new-existing)
+ [En ny Finance and Operations-appforekomst som har data og en kundeengasjementsapp-forekomst](#new-data-new)
+ [En ny Finance and Operations-appforekomst som har data og en eksisterende kundeengasjementsapp-forekomst](#new-data-existing)
+ [En eksisterende Finance and Operations-appforekomst og en ny kundeengasjementsapp-forekomst](#existing-new)
+ [En eksisterende Finance and Operations-appforekomst og en eksisterende kundeengasjementsapp-forekomst](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>En ny Finance and Operations-appforekomst og en ny kundeengasjementsapp-forekomst

Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som ikke har noen data, og en ny kundeengasjementsapp-forekomst, følger du fremgangsmåten i [Oppsett av dobbel skriving fra Lifecycle Services](lcs-setup.md). Når tilkoblingsoppsettet er fullført, skjer følgende handlinger automatisk:

- Et nytt, tomt Finance and Operations-miljø er klargjort.
- En ny, tom forekomst av en kundeengasjementsapp er klargjort, der CRM-hovedløsningen er installert.
- Det opprettes en dobbel skriving-tilkobling for DAT-firmadata.
- Enhetstilordninger er aktivert for direkte synkronisering.

Begge miljøene er så klare for direkte synkronisering av data.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>En ny Finance and Operations-appforekomst og en eksisterende kundeengasjementsapp-forekomst

Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som ikke har noen data, og en eksisterende kundeengasjementsapp-forekomst, følger du fremgangsmåten i [Oppsett av dobbel skriving fra Lifecycle Services](lcs-setup.md). Når tilkoblingsoppsettet er fullført, skjer følgende handlinger automatisk:

- Et nytt, tomt Finance and Operations-miljø er klargjort.
- Det opprettes en dobbel skriving-tilkobling for DAT-firmadata.
- Enhetstilordninger er aktivert for direkte synkronisering.

Begge miljøene er så klare for direkte synkronisering av data.

Følg denne fremgangsmåten for å synkronisere de eksisterende Common Data Service-dataene med Finance and Operations-appen.

1. Opprette et nytt firma i Finance and Operations-appen.
2. Legg til firmaet i oppsettet for dobbelt skriving-tilkobling.
3. [Starte opp](bootstrap-company-data.md) Common Data Service-dataene ved hjelp av en ISO-firmakode (International Organization for Standardization) på tre tegn.
4. Kjør **Innledende synkronisering** -funksjonaliteten for enhetene du vil synkronisere data for.

Hvis du vil ha et eksempel og en alternativ metode, se [Eksempel](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>En ny Finance and Operations-appforekomst som har data og en kundeengasjementsapp-forekomst

Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som har data og en ny forekomst av en kundeengasjementsapp, følger du fremgangsmåten i delen [En ny Finance and Operations-appforekomst og en ny kundeengasjementsapp-forekomst](#new-new) tidligere i dette emnet. Når tilkoblingsoppsettet er fullført, følger du denne fremgangsmåten hvis du vil synkronisere dataene med kundeengasjementsappen.

1. Åpne Finance and Operations-appen fra LCS-siden, logg på og gå til **Databehandling \> Dobbel skriving**.
2. Kjør **Innledende synkronisering** -funksjonaliteten for enhetene du vil synkronisere data for.

Hvis du vil ha et eksempel og en alternativ metode, se [Eksempel](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>En ny Finance and Operations-appforekomst som har data og en eksisterende kundeengasjementsapp-forekomst

Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som har data og en eksisterende forekomst av en kundeengasjementsapp, følger du fremgangsmåten i delen [En ny Finance and Operations-appforekomst og en eksisterende kundeengasjementsapp-forekomst](#new-existing) tidligere i dette emnet. Når tilkoblingsoppsettet er fullført, følger du denne fremgangsmåten hvis du vil synkronisere dataene med kundeengasjementsappen.

1. Åpne Finance and Operations-appen fra LCS-siden, logg på og gå til **Databehandling \> Dobbel skriving**.
2. Kjør **Innledende synkronisering** -funksjonaliteten for enhetene du vil synkronisere data for.

Følg denne fremgangsmåten for å synkronisere de eksisterende Common Data Service-dataene med Finance and Operations-appen.

1. Opprette et nytt firma i Finance and Operations-appen.
2. Legg til firmaet i oppsettet for dobbelt skriving-tilkobling.
3. [Starte opp](bootstrap-company-data.md) Common Data Service-dataene ved hjelp av en ISO-firmakode på tre tegn.
4. Kjør **Innledende synkronisering** -funksjonaliteten for enhetene du vil synkronisere data for.

Hvis du vil ha et eksempel og en alternativ metode, se [Eksempel](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>En eksisterende Finance and Operations-appforekomst og en ny kundeengasjementsapp-forekomst

Oppsettet av en dobbel skriving-tilkobling mellom en eksisterende forekomst av en Finance and Operations-app og en ny forekomst av en kundeengasjementsapp forekommer i Finance and Operation-miljøet.

1. [Angi tilkoblingen fra Finance and Operations-appen](enable-dual-write.md).
2. Kjør **Innledende synkronisering** -funksjonaliteten for enhetene du vil synkronisere data for.

Hvis du vil ha et eksempel og en alternativ metode, se [Eksempel](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>En eksisterende Finance and Operations-appforekomst og en eksisterende kundeengasjementsapp-forekomst

Oppsettet av en dobbel skriving-tilkobling mellom en eksisterende forekomst av en Finance and Operations-app og en eksisterende forekomst av en kundeengasjementsapp forekommer i Finance and Operation-miljøet.

1. Angi tilkoblingen fra Finance and Operations-appen.
2. Hvis du vil synkronisere de eksisterende Common Data Service-dataene til Finance and Operations-appen, [starter du opp](bootstrap-company-data.md) Common Data Service-dataene ved hjelp av en ISO-firmakode på tre bokstaver.
3. Kjør **Innledende synkronisering** -funksjonaliteten for enhetene du vil synkronisere data for.

Hvis du vil ha et eksempel og en alternativ metode, se [Eksempel](#example).

## <a name="example"></a>Eksempel

Hvis du vil ha et eksempel, se [Aktivere enhetstilordningen Kunder V3 til kontakter](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)

Hvis du vil ha en alternativ tilnærming basert på datavolumer i hver enhet som må kjøre første synkronisering, kan du se [Hensyn ved innledende synkronisering](initial-sync-guidance.md).
