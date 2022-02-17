---
title: Veiledning for oppsett av dobbel skriving
description: Dette emnet beskriver scenariene som støttes for oppsett av dobbel skriving.
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6de449b14bcdd82336e3e255bf62ad069d3daaf5
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061610"
---
# <a name="guidance-for-dual-write-setup"></a>Veiledning for oppsett av dobbel skriving

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Du kan opprette en dobbelt skrive-tilkobling mellom et økonomi- og driftsmiljø og et Dataverse-miljø.

+ Et **økonomi- og driftsmiljø** gir den underliggende plattformen for **økonomi- og driftsapper** (for eksempel Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Human Resources).
+ Et **Dataverse-miljø** gir den underliggende plattformen for **kundeengasjementsapper** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).

> [!IMPORTANT]
> Personale-modulen i Dynamics 365 Finance støtter tilkoblinger med dobbel skriving, men det gjør ikke appen Dynamics 365 Human Resources.

Oppsettmekanismen varierer, avhengig av abonnementet og miljøet:

+ Når det gjelder nye forekomster av økonomi- og driftsapper, begynner oppsettet av en tilkobling med dobbel skriving i Microsoft Dynamics Lifecycle Services (LCS). Hvis du har en lisens for Microsoft Power Platform, vil du få et nytt Dataverse-miljø hvis leieren din ikke har et.
+ Når det gjelder eksisterende økonomi- og driftsapper, begynner oppsettet av en tilkobling med dobbel skriving i økonomi- og driftsmiljøet.

Før du starter dobbel skriving på en enhet, kan du kjøre en første synkronisering for å behandle eksisterende data på begge sider: økonomi- og driftsapper og Customer Engagement-apper. Du kan hoppe over den innledende synkroniseringen hvis du ikke må synkronisere data mellom de to miljøene.

En innledende synkronisering gjør at du kan kopiere eksisterende data fra én app til en annen begge veier. Det finnes flere forskjellige oppsettscenarioer, avhengig av miljøene du allerede har, og typen som finnes i dem.

Følgende oppsettscenarier støttes:

+ [En ny økonomi- og driftsappforekomst og en ny Customer Engagement-appforekomst](#new-new)
+ [En ny økonomi- og driftsappforekomst og en eksisterende Customer Engagement-appforekomst](#new-existing)
+ [En ny økonomi- og driftsappforekomst som har data og en ny Customer Engagement-appforekomst](#new-data-new)
+ [En ny økonomi- og driftsappforekomst som har data og eksisterende Customer Engagement-appforekomst](#new-data-existing)
+ [En eksisterende økonomi- og driftsappforekomst og ny Customer Engagement-appforekomst](#existing-new)
+ [En eksisterende økonomi- og driftsappforekomst og eksisterende Customer Engagement-appforekomst](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>En ny økonomi- og driftsappforekomst og en ny Customer Engagement-appforekomst

Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en økonomi- og driftsapp som ikke har noen data, og en ny forekomst av en Customer Engagement-app, følger du fremgangsmåten i [Oppsett av dobbel skriving fra Lifecycle Services](lcs-setup.md). Når tilkoblingsoppsettet er fullført, skjer følgende handlinger automatisk:

- Et nytt, tomt økonomi- og driftsmiljø klargjøres.
- En ny, tom forekomst av en kundeengasjementsapp er klargjort, der CRM-hovedløsningen er installert.
- Det opprettes en dobbel skriving-tilkobling for DAT-firmadata.
- Tabelltilordninger er aktivert for direkte synkronisering.

Begge miljøene er så klare for direkte synkronisering av data.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>En ny økonomi- og driftsappforekomst og en eksisterende Customer Engagement-appforekomst

Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en økonomi- og driftsapp som ikke har noen data, og en eksisterende forekomst av en Customer Engagement-app, følger du fremgangsmåten i [Oppsett av dobbel skriving fra Lifecycle Services](lcs-setup.md). Når tilkoblingsoppsettet er fullført, skjer følgende handlinger automatisk:

- Et nytt, tomt økonomi- og driftsmiljø klargjøres.
- Det opprettes en dobbel skriving-tilkobling for DAT-firmadata.
- Tabelltilordninger er aktivert for direkte synkronisering.

Begge miljøene er så klare for direkte synkronisering av data.

Følg denne fremgangsmåten for å synkronisere de eksisterende Dataverse-dataene med økonomi- og driftsappen.

1. Opprett et nytt firma i økonomi- og driftsappen.
2. Legg til firmaet i oppsettet for dobbelt skriving-tilkobling.
3. [Starte opp](bootstrap-company-data.md) Dataverse-dataene ved hjelp av en ISO-firmakode (International Organization for Standardization) på tre tegn.
4. Kjør funksjonaliteten **Innledende synkronisering** for tabellen du vil synkronisere data for.

Hvis du vil ha koblinger til et eksempel og en alternativ tilnærming, kan du se [Eksempel](#example)-delen senere i dette emnet.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>En ny økonomi- og driftsappforekomst som har data og en ny Customer Engagement-appforekomst

Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en økonomi- og driftsapp som har data og en ny forekomst av en Customer Engagement-app, følger du fremgangsmåten i delen [En ny økonomi- og driftsappforekomst og en ny Customer Engagement-appforekomst](#new-new) tidligere i dette emnet. Når tilkoblingsoppsettet er fullført, følger du denne fremgangsmåten hvis du vil synkronisere dataene med kundeengasjementsappen.

1. Åpne økonomi- og driftsappen fra LCS-siden, logg på og gå til **Databehandling \> Dobbel skriving**.
2. Kjør funksjonaliteten **Innledende synkronisering** for tabellen du vil synkronisere data for.

Hvis du vil ha koblinger til et eksempel og en alternativ tilnærming, kan du se [Eksempel](#example)-delen.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>En ny økonomi- og driftsappforekomst som har data og eksisterende Customer Engagement-appforekomst

Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en økonomi- og driftsapp som har data og en eksisterende forekomst av en Customer Engagement-app, følger du fremgangsmåten i delen [En ny økonomi- og driftsappforekomst og en eksisterende Customer Engagement-appforekomst](#new-existing) tidligere i dette emnet. Når tilkoblingsoppsettet er fullført, følger du denne fremgangsmåten hvis du vil synkronisere dataene med kundeengasjementsappen.

1. Åpne økonomi- og driftsappen fra LCS-siden, logg på og gå til **Databehandling \> Dobbel skriving**.
2. Kjør funksjonaliteten **Innledende synkronisering** for tabellen du vil synkronisere data for.

Følg denne fremgangsmåten for å synkronisere de eksisterende Dataverse-dataene med økonomi- og driftsappen.

1. Opprett et nytt firma i økonomi- og driftsappen.
2. Legg til firmaet i oppsettet for dobbelt skriving-tilkobling.
3. [Starte opp](bootstrap-company-data.md) Dataverse-dataene ved hjelp av en ISO-firmakode på tre tegn.
4. Kjør funksjonaliteten **Innledende synkronisering** for tabellen du vil synkronisere data for.

Hvis du vil ha koblinger til et eksempel og en alternativ tilnærming, kan du se [Eksempel](#example)-delen.

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>En eksisterende økonomi- og driftsappforekomst og en ny Customer Engagement-appforekomst

Oppsettet av en dobbel skriving-tilkobling mellom en eksisterende forekomst av en økonomi- og driftsapp og en ny forekomst av en Customer Engagement-app forekommer i økonomi- og driftsmiljøet.

1. [Konfigurer tilkoblingen fra økonomi- og driftsappen](enable-dual-write.md).
2. Kjør funksjonaliteten **Innledende synkronisering** for tabellen du vil synkronisere data for.

Hvis du vil ha koblinger til et eksempel og en alternativ tilnærming, kan du se [Eksempel](#example)-delen.

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>En eksisterende økonomi- og driftsappforekomst og eksisterende Customer Engagement-appforekomst

Oppsettet av en dobbel skriving-tilkobling mellom en eksisterende forekomst av en økonomi- og driftsapp og en eksisterende forekomst av en Customer Engagement-app forekommer i økonomi- og driftsmiljøet.

1. [Konfigurer tilkoblingen fra økonomi- og driftsappen](enable-dual-write.md).
2. Hvis du vil synkronisere de eksisterende Dataverse-dataene til økonomi- og driftsappen, [starter du opp](bootstrap-company-data.md) Dataverse-dataene ved hjelp av en ISO-firmakode på tre bokstaver.
3. Kjør funksjonaliteten **Innledende synkronisering** for tabellen du vil synkronisere data for.

Hvis du vil ha koblinger til et eksempel og en alternativ tilnærming, kan du se [Eksempel](#example)-delen.

## <a name="example"></a>Eksempel

Hvis du vil ha et eksempel, kan du se [Aktivere tabelltilordningen Kunder V3 til kontakter](enable-entity-map.md#enable-table-map)

Hvis du vil ha en alternativ tilnærming som er basert på datavolumer i hver enhet som må kjøre en innledende synkronisering, kan du se [Hensyn ved innledende synkronisering](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]