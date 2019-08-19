---
title: Dataintegrasjon i nær sanntid mellom Finance and Operations og Common Data Service
description: Dette emnet inneholder en oversikt over integreringen mellom Microsoft Dynamics 365 for Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797234"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a>Dataintegrasjon i nær sanntid mellom Finance and Operations og Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

I dagens digitale verden bruker bedriftsøkosystemer Microsoft Dynamics 365-pakken som en helhet. Fordi data fra personer, kunder, operasjoner og IoT-enheter (tingenes Internett) flyter over i én kilde, finnes det en mulighet for digitale tilbakemeldingsløkker. For å oppnå denne erfaringen er integrering mellom Dynamics 365 for Finance and Operations og Dynamics 365 for Customer Engagement-programmer viktig. Customer Engagement-programmer er bygget på toppen av Common Data Service. Integrasjon mellom Finance and Operations-data med Common Data Service lar Customer Engagement-programmer kommunisere sammenhengende og flytende med Finance and Operations.

Finance and Operations og Common Data Service gir nær sanntid datasynkronisering mellom Finance and Operations og Customer Engagement-programmer via et dual-Write-rammeverk. Dekningen er bred og spenner over 28 overflateområder av Finance and Operations. Målet er å gi en brukeropplevelse av "Ett Dynamics 365" gjennom sømløse dataflyter som kobler sammen forretningsprosesser på tvers av programmer.

![Oversiktsdiagram over arkitekturen](media/dual-write-overview.jpg)

Følgende verdiforslag er tilgjengelige for kunder:

+ [Organisasjonshierarki i Common Data Service](dual-write-organization.md)
+ [Bedriftskonsept i Common Data Service](dual-write-company.md)
+ [Integrerte originalkunde](dual-write-customer.md)
+ [Integrert original for leverandør](dual-write-vendor.md)
+ Ensartet produktstandard

## <a name="system-requirements"></a>Systemkrav

Synkrone, toveis dataflyter i nær sanntid krever følgende versjoner:

+ Microsoft Dynamics 365 for Finance and Operations versjon 10.0.4 (juli 2019) med plattformoppdatering 28 eller senere
+ Microsoft Dynamics 365 for Customer Engagement, plattformversjon 9.1 (4.2) eller senere

## <a name="setup-instructions"></a>Installasjonsinstruksjoner

Følg dissse trinnene for å konfigurere integrasjonen mellom Finance and Operations og Common Data Service.
    
1. For oppsett av dual-Write-systemet, se den [trinnvise veiledningen](https://aka.ms/dualwrite-docs) om kunngjøring av forhåndsvisning av Dual Write.
2. Last ned og installer løsningen fra gruppen [Finance and Operations, Common Data Service Customer Engagement-integrasjon](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer. Pakken inneholder fem løsninger:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Følg utføringsrekkefølgen for [synkronisering av innledende referansedata](dual-write-initial.md).
4. Hvis du støter på problemer med dual-write-skrive synkronisering, kan du se [Feilsøkingsveiledning for dataintegrering](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Du kan ikke kjøre dual-write og dobbelt-skrive og [Kundeemne til kontanter](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side ved side. Hvis du kjører Kundeemne til kontanter-løsningen, må du avinstallere den. Du må også deaktivere dual-write-maler for kunde og leverandør som er en del av Kundeemne til kontanter-løsningen.
