---
title: Integrasjon med Microsoft Dynamics 365 for Field Service
description: Dette emnet gir en oversikt over integrasjonen med Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 08/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 95031534c43dc0578e258bc3e5376c429d72b0ab
ms.openlocfilehash: 673ab2a101cee1a3dbbb1249f582d959cecc7f7f
ms.contentlocale: nb-no
ms.lasthandoff: 12/23/2018

---

# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integrasjon med Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations gjør det mulig med synkronisering av forretningsprosesser mellom Finance and Operations og Microsoft Dynamics 365 for Field Service. Intregrasjonsscenarioene konfigureres ved hjelp av utvidbare Dataintegrator-maler og Common Data Service (CDS) for å gjøre det mulig med synkronisering av forretningsprosesser.
Standardmaler kan brukes til å lage tilpassede integreringsprosjekter der flere standard og egendefinerte felt, og enheter, kan tilordnes for å justere integreringen og oppfylle spesifikke forretningsbehov. 

Field Service-integreringen bygger på eksisterende kundeemne til kontanter-funksjonalitet.

![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/field-service-integration.png)

Den første fasen av integreringen mellom Field Service og Finance and Operations fokuserer på kunne la arbeidsordrer og avtaler i Field Service faktureres i Finance and Operations. Den støttede flyten starter i Field Service, der informasjonen fra arbeidsordrer synkroniseres til Finance and Operations som salgsordrer. Salgsordrene faktureres i Finance and Operations for å generere fakturadokumenter. I tillegg synkroniseres informasjonen fra avtalefakturaer i Field Service til Finance and Operations. Microsoft Dynamics 365 Data integrator synkroniserer data ved hjelp av prosjekter som kan tilpasses. Standardmaler kan brukes til å lage tilpassede integreringsprosjekter der flere standard og egendefinerte felt, og enheter, kan tilordnes for å justere integreringen og oppfylle spesifikke behov.

Den første fasen av integreringen mellom Field Service og Finance and Operations gjør det mulig med synkronisering av følgende elementer:

- [Produkter i Finance and Operations til produkter i Field Service som inneholder produkttypeinformasjon](field-service-product.md)
- [Arbeidsordrer i Field Service til salgsordrer i Finance and Operations](field-service-work-order.md)
- [Fakturaer i Field Service til fritekstfakturaer i Finance and Operations](field-service-invoice.md)

Hvis du vil se et eksempel på hvordan du kan synkronisere en arbeidsordre mellom Field Service og Finance and Operations, se den korte YouTube-videoen [Synkronisere en arbeidsordre med Microsoft Dynamics 365-integrering](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="system-requirements-for-finance-and-operations"></a>Systemkrav for Finance and Operations
Field Service-integrasjon støtter følgende versjoner:

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations versjon 8.0 (april 2018) eller senere

- Dynamics 365 for Finance and Operations versjon 8.0 (april 2018) ble utgitt i april 2018 og har programbuild-nummer 8.0.30.8020 med plattformoppdatering 15 (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>Systemkrav for Field Service
For å bruke Field Service-integrasjonsløsningen må du installere følgende komponenter:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 eller senere

- Dynamics 365 for Field Service versjon 1612 (9.0.1.733) (DB 9.0.1.733) online eller en senere versjon.
- Prospect to Cash (P2C)-løsningen for Dynamics 365, versjon 1.15.0.1 eller en nyere versjon. Løsningen er tilgjengelig for nedlasting fra [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Field Service-integrasjonsløsning for Dynamics 365, versjon 1.0.0.0 eller en nyere versjon. Løsningen er tilgjengelig for nedlasting fra [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegration).

# <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>Integrasjon med Microsoft Dynamics 365 for Field Service, inkludert informasjon om lager og prosjekt

Den ekstra funksjonaliteten i andre fase fokuserer på å gi teknikere innsikt i lagerinformasjon fra Finance and Operations slik at de kan oppdatere lagernivåer og overføre materiell. I tillegg vil firmaer som installerer eller vedlikeholder solgte varer, dra nytte av bedre styring og synlighet i hele salgs- og serviceprosessen med integrering fra prosjekter.

### <a name="functionality-includes-integration-of"></a>Funksjonalitet inkluderer integrering av:
- Lagerinformasjon
- Informasjon om lagerbeholdning
- Lageroverføringer
- Lagerjusteringer
- Dynamics 365 for Finance and Operations-prosjekter koblet til Dynamics 365 for Field Service-arbeidsordrer
- Dynamics 365 for Field Service-arbeidsordrer med kobling til Dynamics 365 for Finance and Operations-prosjekter bruker dette prosjektnummeret i Dynamics 365 for Finance and Operations-salgsordren for å tillate fakturering fra prosjektet. 

![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>Den andre fasen av integreringen mellom Field Service og Finance and Operations gjør det mulig med synkronisering med følgende maler:
- Lagre (Fin and Ops til Field Service) - Lagre fra Finance and Operations til Field Service [Avansert spørring] 
- Produktlager (Fin and Ops til Field Service) - Lagernivåinformasjon fra Finance and Operations til Field Service [Avansert spørring] 
- Lagerjustering (Field Service til Fin and Ops) - Lagerjusteringer fra Field Service til Finance and Operations [Avansert spørring] 
- Lageroverføringer (Field Service til Fin and Ops) - Lageroverføringer fra Field Service til Finance and Operations [Avansert spørring] 
- Prosjekter (Fin and Ops til Field Service) - Prosjektliste fra Finance and Operations til Field Service 
- Arbeidsordrer med prosjekt (Field Service til Fin and Ops) - Arbeidsordrer i Field Service til salgsordrer i Finance and Operations, med støtte for prosjekt [Avansert spørring] 
- Field Service-produkter med lagerenhet (Fin and Ops til Sales) - Salgbare frigitte produkter i Finance and Operations til Sales-produkter for Field Service, inkludert lagerenhet 

## <a name="system-requirements-for-finance-and-operations"></a>Systemkrav for Finance and Operations
Field Service-integrasjon støtter følgende versjoner:

- Dynamics 365 for Finance and Operations versjon 8.1.2 (desember 2019) ble utgitt i desember 2019 og har programbuild-nummer 8.1.195 med plattformoppdatering 22 (7.0.5095). 

## <a name="system-requirements-for-field-service"></a>Systemkrav for Field Service
For å bruke Field Service-integrasjonsløsningen må du installere følgende komponenter:

- Field Service for Dynamics 365 (versjon 8.2.0.286) eller en nyere versjon på Dynamics 365 9.1.x - utgitt november 2018
- Prospect to Cash (P2C)-løsningen for Dynamics 365, versjon 1.15.0.1 eller en nyere versjon. Løsningen er tilgjengelig for nedlasting fra [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Field Service Integration, Project and Inventory-løsningen for Dynamics 365, versjon 2.0.0.0 eller en nyere versjon. Løsningen er tilgjengelig for nedlasting fra [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).

