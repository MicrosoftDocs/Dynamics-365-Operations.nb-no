---
title: Konfigurasjon for Finance Insights
description: Dette emnet forklarer konfigurasjonstrinnene som gjør at systemet kan bruke funksjonene i Finance Insights.
author: ShivamPandey-msft
ms.date: 1/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 5668d3ddff777645b4f1c6608f025d0c5a63208a
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752984"
---
# <a name="configuration-for-finance-insights"></a>Konfigurasjon for Finance Insights

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance Insights kombinerer funksjonalitet fra Microsoft Dynamics 365 Finance med Dataverse, Azure og AI Builder for å gi organisasjonen kraftige prognoseverktøy. Dette emnet forklarer konfigurasjonstrinnene som gjør at systemet kan bruke funksjonene i Finance Insights. Hvis du vil fullføre prosedyrene i dette emnet, må du ha tilgang som Systemadministrator og Systemtilpasser i [administrasjonssenteret for Power Portal](https://admin.powerplatform.microsoft.com/), tilgang som Systemadministrator i Dynamics 365 Finance og tilgang til å opprette miljøer i Microsoft Dynamics Lifecycle Services (LCS).

> [!NOTE]
> Følgende fremgangsmåter for å konfigurere Finance Insights er gyldige for Dynamics 365 Finance-versjon 10.0.21 og senere.

## <a name="deploy-dynamics-365-finance"></a>Klargjøre Dynamics 365 Finance

Følg denne fremgangsmåten for å distribuere miljøene.

1. Opprett eller oppdater et Dynamics 365 Finance-miljø i LCS. Miljøet krever appversjon 10.0.21 eller nyere.

    > [!NOTE]
    > Miljøet må være et miljø med høy tilgjengelighet. (Denne typen miljø kalles også et miljø på lag 2.) Hvis du vil ha mer informasjon, kan du se [Miljøplanlegging](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

2. Hvis du konfigurerer Finance Insights i et sandkassemiljø, må du kanskje kopiere produksjonsdata til dette miljøet før prediksjoner kan fungere. Prediksjonsmodellen bruker flere år med data til å bygge prediksjoner. Contoso-demodataene inneholder ikke nok historiske data til at prediksjonsmodellen kan læres opp tilstrekkelig. 

## <a name="configure-dataverse"></a>Konfigurer Dataverse

Følg fremgangsmåten nedenfor til å konfigurere Dataverse for Finance Insights.

- Åpne miljøsiden i LCS, og kontroller at **Power Platform-integrering** allerede er konfigurert.

    - Hvis den allerede er konfigurert, skal Dataverse-miljønavnet som er koblet til Finance-miljøet, vises.
    - Hvis det ikke er konfigurert, velger du **Installasjon**. Konfigurasjonen av Dataverse-miljøet kan ta opptil en time. Når konfigurasjonen er fullført, skal navnet på Dataverse-miljøet som er koblet til Finance-miljøet, vises.

## <a name="configure-the-finance-insights-add-in"></a>Konfigurere Finance Insights-tillegget

Hvis du tidligere har installert Finance Insights-tillegget, avinstallerer du det før du fullfører fremgangsmåten nedenfor.

> [!NOTE]
> Hvis du allerede har installert Data Lake-tillegget i LCS, vil Finance Insights bruke det til å lagre data som er nødvendige for prediksjoner. Hvis du ikke har installert Data Lake-tillegget i LCS ennå, vil Finance Insights-tillegget opprette en administrert Data Lake for deg.

Følg denne fremgangsmåten for å installere Finance Insights-tillegget.

1. Logg på LCS, og velg deretter **Detaljerte opplysninger** under miljønavnet til høyre på siden.
2. I delen **Miljøtillegg** velger du **Installer et nytt tillegg**.
3. Velg **Finance Insights**-tillegget.
4. Godta betingelsene, og velg deretter **Installer**.

Det kan ta flere minutter å installere tillegget.

## <a name="one-last-thing"></a>En siste ting ...

Når tillegget er installert, kan det ta opptil en time før du kan aktivere Finance Insights-funksjoner i arbeidsområdet **Funksjonsbehandling** i Dynamics 365 Finance. Hvis du ikke vil vente så lenge, kan du kjøre prosessen **Statuskontroll for klargjøring av innsikt** manuelt. 

1. I Dynamics 365 Finance går du til **Systemadministrasjon \> Oppsett \> Prosessautomatisering**.
2. I kategorien **Bakgrunnsprosesser** finner du **Statuskontroll for klargjøring av innsikt** og velger **Rediger**.
3. Sett feltet **Neste utførelse** til 30 minutter før gjeldende tid.

   Denne endringen skal tvinge prosessen **Statuskontroll for klargjøring av innsikt** til å kjøre umiddelbart.

   Når prosessen **Statuskontroll for klargjøring av innsikt** er kjørt, kan du aktivere Finance Insights-funksjoner i arbeidsområdet **Funksjonsbehandling**.

## <a name="feedback-and-support"></a>Tilbakemelding og støtte

Hvis du er interessert i å gi tilbakemelding eller trenger kundestøtte, kan du sende en e-postmelding til [Finance Insights (forhåndsversjon)](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
