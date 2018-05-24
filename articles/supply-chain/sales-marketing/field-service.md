---
title: Integrasjon med Microsoft Dynamics 365 for Field Service
description: Dette emnet gir en oversikt over integrasjonen med Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 03a932652cdd93b2a5917d0fca72809d1648b678
ms.openlocfilehash: b1acf0b64914a3199fcf44f8377e32b26f0af99e
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integrasjon med Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations gjør det mulig med synkronisering av forretningsprosesser mellom Finance and Operations og Microsoft Dynamics 365 for Field Service. Intregrasjonsscenarioene konfigureres ved hjelp av utvidbare Dataintegrator-maler og Common Data Service (CDS) for å gjøre det mulig med synkronisering av forretningsprosesser.

[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)

Den første fasen av integreringen mellom Field Service og Finance and Operations fokuserer på kunne la arbeidsordrer og avtaler i Field Service faktureres i Finance and Operations. Den støttede flyten starter i Field Service, der informasjonen fra arbeidsordrer synkroniseres til Finance and Operations som salgsordrer. Salgsordrene faktureres i Finance and Operations for å generere fakturadokumenter. I tillegg synkroniseres informasjonen fra avtalefakturaer i Field Service til Finance and Operations. Microsoft Dynamics 365 Data integrator synkroniserer data ved hjelp av prosjekter som kan tilpasses. Standardmaler kan brukes til å lage tilpassede integreringsprosjekter der flere standard og egendefinerte felt, og enheter, kan tilordnes for å justere integreringen og oppfylle spesifikke behov.

Den første fasen av integreringen mellom Field Service og Finance and Operations gjør det mulig med synkronisering av følgende elementer:

- [Produkter i Finance and Operations til produkter i Field Service som inneholder produkttypeinformasjon](field-service-product.md)
- [Arbeidsordrer i Field Service til salgsordrer i Finance and Operations](field-service-work-order.md)
- [Fakturaer i Field Service til fritekstfakturaer i Finance and Operations](field-service-invoice.md)

Hvis du vil se et eksempel på hvordan du kan synkronisere en arbeidsordre mellom Field Service og Finance og Operations, kan du se den korte YouTube videoen:

> [!Video https://www.youtube.com/embed/hAB4TDVMjxU]

[Synkronisere en arbeidsordre mellom Field Service og Finance and Operations (YouTube-video)](https://youtu.be/hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a>Systemkrav for Finance and Operations
Field Service-integrasjon støtter følgende versjoner:

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations versjon 8.0 (april 2018) eller senere

- Dynamics 365 for Finance and Operations versjon 8.0 (april 2018) ble utgitt i april 2018 og har programbuild-nummer 8.0.30.8020 med plattformoppdatering 15 (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>Systemkrav for Field Service
For å bruke Field Service-integrasjonsløsningen må du installere følgende komponenter:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 eller senere

- Dynamics 365 for Field Service versjon 1612 (9.0.1.733) (DB 9.0.1.733) online eller en senere versjon.
- Prospect to Cash (P2C)-løsningen for Dynamics 365, versjon 1.15.0.1 eller en nyere versjon. Løsningen er tilgjengelig for nedlasting fra [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Field Service-integrasjonsløsning for Dynamics 365, versjon 1.0.0.0 eller en nyere versjon. Løsningen er tilgjengelig for nedlasting fra [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).

