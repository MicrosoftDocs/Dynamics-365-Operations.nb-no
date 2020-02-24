---
title: Dataintegrering i nær sanntid med Common Data Service
description: Dette emnet inneholder en oversikt over integreringen mellom Finance and Operations og Common Data Service.
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
ms.openlocfilehash: 1c09b0c0bb695e7695acb7a8821ffb99ae1f6f06
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019942"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>Dataintegrering i nær sanntid med Common Data Service

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

I dagens digitale verden bruker bedriftsøkosystemer Microsoft Dynamics 365-apper som en helhet. Fordi data fra personer, kunder, operasjoner og IoT-enheter (tingenes Internett) flyter over i én kilde, finnes det en mulighet for digitale tilbakemeldingsløkker. For å oppnå denne erfaringen er integrering mellom Finance and Operations-apper og Dynamics 365-apper viktig. Noen programmer er bygget på toppen av Common Data Service. Integrasjon mellom Finance and Operations-appdata og Common Data Service lar andre apper kommunisere sammenhengende og jevnt med Finance and Operations.

Finance and Operations-apper og Common Data Service gi datasynkronisering i nær sanntid mellom Finance and Operations-apper og andre Dynamics 365-programmer via et dual-Write-rammeverk. Dekningen er bred og spenner over 28 overflateområder av programmet. Målet er å gi en brukeropplevelse av "Ett Dynamics 365" gjennom sømløse dataflyter som kobler sammen forretningsprosesser på tvers av programmer.

![Oversiktsdiagram over arkitekturen](media/dual-write-overview.jpg)

Følgende verdiforslag er tilgjengelige:

+ [Organisasjonshierarki i Common Data Service](organization-mapping.md)
+ [Bedriftskonsept i Common Data Service](company-data.md)
+ [Integrerte originalkunde](customer-mapping.md)
+ [Integrert finans](ledger-mapping.md)
+ [Samlet produktopplevelse](product-mapping.md)
+ [Integrert original for leverandør](vendor-mapping.md)
+ [Integrerte områder og lagre](sites-warehouses-mapping.md)
+ [Integrert hoveddata for avgift](tax-mapping.md)

## <a name="system-requirements"></a>Systemkrav

Synkrone, toveis dataflyter i nær sanntid krever følgende versjoner:

+ Microsoft Dynamics 365 for Finance and Operations versjon 10.0.4 (juli 2019) med plattformoppdatering 28 eller senere
+ Microsoft Dynamics 365 for Customer Engagement, plattformversjon 9.1 (4.2) eller senere

## <a name="setup-instructions"></a>Installasjonsinstruksjoner

Følg disse trinnene for å sette opp integrasjon mellom Finance and Operations-apper og Common Data Service.
    
1. For oppsett av dual-Write-systemet, se den [trinnvise veiledningen](https://aka.ms/dualwrite-docs) om kunngjøring av forhåndsvisning av Dual Write.
2. Last ned og Installer løsningen fra [Fin Ops og CDS/CE-integreringen via Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096)Yammer-gruppen. Pakken inneholder fem løsninger:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Følg utføringsrekkefølgen for [synkronisering av innledende referansedata](initial-sync.md).
4. Hvis du støter på problemer med dual-write-skrive synkronisering, kan du se [Feilsøkingsveiledning for dataintegrering](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Du kan ikke kjøre dual-write og dobbelt-skrive og [Kundeemne til kontanter](../../../../supply-chain/sales-marketing/prospect-to-cash.md) side ved side. Hvis du kjører Kundeemne til kontanter-løsningen, må du avinstallere den. Du må også deaktivere dual-write-maler for kunde og leverandør som er en del av Kundeemne til kontanter-løsningen.
