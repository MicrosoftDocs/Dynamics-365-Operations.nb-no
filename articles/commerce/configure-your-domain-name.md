---
title: Konfigurere domenenavnet
description: Dette emnet beskriver hvordan du konfigurerer et domenenavn for et e-handelsområde for Microsoft Dynamics 365.
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f73c034563fb1cc6b05091b4c47e2a788d1a8b6
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945542"
---
# <a name="configure-your-domain-name"></a>Konfigurere domenenavnet

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer et domenenavn for et e-handelsområde for Microsoft Dynamics 365. 

## <a name="add-domains-during-e-commerce-initialization"></a>Legge til domener under initialisering av e-handel

Hvis du vil knytte domener til ditt e-handelsmiljø, kan du initialisere e-handel som beskrevet i [Distribuere et nytt e-handelsområde](deploy-ecommerce-site.md). Under initialiseringen blir du bedt om å oppgi informasjon som skal brukes til å klargjøre ditt e-handelsmiljø. Legg til alle domenene du planlegger å bruke med dette miljøet, i feltet **Støttede vertsnavn**. Flere domener må skilles med semikolon. På denne måten konfigureres domenene i alle de nødvendige komponentene for e-handel, og de er klare til bruk når du bytter trafikk fra innholdsleveringsnettverket (CDN) eller webserveren og peker den til e-handel-frontene.

## <a name="add-domains-after-e-commerce-initialization"></a>Legge til domener etter initialisering av e-handel

Hvis du vil knytte nye domener til e-handelsmiljøet etter at e-handel initialiseres, må du sende en serviceforespørsel.

## <a name="additional-resources"></a>Tilleggsressurser

[Distribuere et nytt e-handelsområde](deploy-ecommerce-site.md)

[Opprette et e-handelsområde](create-ecommerce-site.md)

[Knytte et nettområde til en kanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md)

[Legge til støtte for et innholdsleveringsnettverk (CDN)](add-cdn-support.md)

[Aktivere stedsbasert butikkregistrering](enable-store-detection.md)
