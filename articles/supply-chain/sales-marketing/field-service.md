---
title: Oversikt over integrering med Microsoft Dynamics 365 Field Service
description: Dette emnet inneholder en oversikt over integreringen med Microsoft Dynamics 365 Field Service.
author: Henrikan
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 23661bca91ccd7b7a04c763e60cfca9a99d62bfa
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566461"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a>Oversikt over integrering med Microsoft Dynamics 365 Field Service

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Supply Chain Management gjør det mulig å synkronisere forretningsprosesser mellom Dynamics 365 Supply Chain Management og Dynamics 365 Field Service. Intregrasjonsscenarioene konfigureres ved hjelp av utvidbare Dataintegrator-maler og Microsoft Dataverse for å gjøre det mulig med synkronisering av forretningsprosesser.
Standardmaler kan brukes til å lage tilpassede integreringsprosjekter der flere standard og egendefinerte kolonner og tabeller kan tilordnes for å justere integreringen og oppfylle spesifikke forretningsbehov. 

Field Service-integreringen bygger på eksisterende kundeemne til kontanter-funksjonalitet.

![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service.](./media/field-service-integration.png)

Den første fasen av integreringen mellom Field Service og Supply Chain Management fokuserer på kunne la arbeidsordrer og avtaler i Field Service faktureres i Supply Chain Management. Den støttede flyten starter i Field Service, der informasjonen fra arbeidsordrer synkroniseres til Supply Chain Management som salgsordrer. I Supply Chain Management faktureres salgsordrene for å generere fakturadokumenter. I tillegg synkroniseres informasjonen fra avtalefakturaer i Field Service til Supply Chain Management. Microsoft Dynamics 365 Data integrator synkroniserer data ved hjelp av prosjekter som kan tilpasses. Standardmaler kan brukes til å lage tilpassede integreringsprosjekter der flere standard og egendefinerte kolonner og tabeller kan tilordnes for å justere integreringen og oppfylle spesifikke behov.

Den første fasen av integreringen mellom Field Service og Supply Chain Management gjør det mulig med synkronisering av følgende elementer:

- [Synkronisere produkter i Supply Chain Management til produkter i Field Service](field-service-product.md)
- [Synkronisere arbeidsordrer i Field Service til salgsordrer i Supply Chain Management](field-service-work-order.md)
- [Synkronisere avtalefakturaer i Field Service til fritekstfakturaer i Supply Chain Management](field-service-invoice.md)

Hvis du vil se et eksempel på hvordan du kan synkronisere en arbeidsordre mellom Field Service og Supply Chain Management, se den korte YouTube-videoen [Synkronisere en arbeidsordre med Microsoft Dynamics 365-integrering](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-field-service-including-inventory-and-project-information"></a>Integrasjon med Field Service, inkludert informasjon om lager og prosjekt

Den ekstra funksjonaliteten i andre fase fokuserer på å gi teknikere innsikt i lagerinformasjon fra Supply Chain Management slik at de kan oppdatere lagernivåer og overføre materiell. I tillegg vil firmaer som installerer eller vedlikeholder solgte varer, dra nytte av bedre styring og synlighet i hele salgs- og serviceprosessen med integrering fra prosjekter.

### <a name="functionality-includes-integration-of"></a>Funksjonalitet inkluderer integrering av:
- Lagerinformasjon
- Informasjon om lagerbeholdning
- Lageroverføringer
- Lagerjusteringer
- Supply Chain Management-prosjekter koblet til Dynamics 365 Field Service-arbeidsordrer
- Dynamics 365 Field Service-arbeidsordrer med kobling til Supply Chain Management-prosjekter bruker dette prosjektnummeret i salgsordren for å tillate fakturering fra prosjektet. 

![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service, inkludert lager- og prosjektinformasjon.](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a>Den andre fasen av integreringen mellom Field Service og Supply Chain Management gjør det mulig med synkronisering med følgende maler:
- Lagre (Supply Chain Management til Field Service) – Lagre fra Supply Chain Management til Field Service [Avansert spørring] 
- Produktbeholdning (Supply Chain Management til Field Service) – Lagernivåinformasjon fra Supply Chain Management til Field Service [Avansert spørring] 
- Lagerjustering (Field Service til Supply Chain Management) – Lagerjusteringer fra Field Service til Supply Chain Management [Avansert spørring] 
- Lageroverføringer (Field Service til Supply Chain Management) – Lageroverføringer fra Field Service til Supply Chain Management [Avansert spørring] 
- Prosjekter (Supply Chain Management til Field Service) – Prosjektliste fra Supply Chain Management til Field Service 
- Arbeidsordrer med prosjekt (Field Service til Supply Chain Management) – Arbeidsordrer i Field Service til salgsordrer i Supply Chain Management, med støtte for prosjekt [Avansert spørring] 
- Field Service-produkter med lagerenhet (Supply Chain Management til Sales) – Salgbare frigitte produkter i Supply Chain Management til Sales-produkter for Field Service, inkludert lagerenhet 

## <a name="system-requirements"></a>Systemkrav

### <a name="system-requirements-for-supply-chain-management"></a>Systemkrav for Supply Chain Management
Field Service-integrasjon støtter følgende versjoner:

- Dynamics 365 for Finance and Operations versjon 8.1.2 (desember 2018) ble utgitt i desember 2018 og har programbyggnummer 8.1.195 med Platform update 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>Systemkrav for Field Service
For å bruke Field Service-integrasjonsløsningen må du installere følgende komponenter:

- Field Service (versjon 8.2.0.286) eller en nyere versjon på Dynamics 365 9.1.x – utgitt november 2018
- Prospect to Cash (P2C)-løsningen for Dynamics 365, versjon 1.15.0.1 eller en nyere versjon. Løsningen er tilgjengelig for nedlasting fra [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Field Service Integration, Project and Inventory-løsningen for Dynamics 365, versjon 2.0.0.0 eller en nyere versjon. Løsningen er tilgjengelig for nedlasting fra [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]