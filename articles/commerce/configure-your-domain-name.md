---
title: Konfigurere domenenavnet
description: Dette emnet beskriver hvordan du konfigurerer et domenenavn for et e-handelsområde for Microsoft Dynamics 365.
author: psimolin
manager: AnnBe
ms.date: 03/02/2020
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
ms.openlocfilehash: 2ad9ca3aee21301ef6d830d7b29982a45cd53f60
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096826"
---
# <a name="configure-your-domain-name"></a>Konfigurere domenenavnet


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer et domenenavn for et e-handelsområde for Microsoft Dynamics 365. 

## <a name="add-domains-during-e-commerce-initialization"></a>Legge til domener under initialisering av e-handel

Hvis du vil knytte domener til ditt e-handelsmiljø, kan du initialisere e-handel som beskrevet i [Distribuere et nytt e-handelsområde](deploy-ecommerce-site.md). Under initialiseringen blir du bedt om å oppgi informasjon som skal brukes til å klargjøre ditt e-handelsmiljø. Legg til alle domenene du planlegger å bruke med dette miljøet, i feltet **Støttede vertsnavn**. Flere domener må skilles med semikolon. På denne måten konfigureres domenene i alle de nødvendige komponentene for e-handel, og de er klare til bruk når du bytter trafikk fra innholdsleveringsnettverket (CDN) eller webserveren og peker den til e-handel-frontene.

## <a name="add-domains-after-e-commerce-initialization"></a>Legge til domener etter initialisering av e-handel

Hvis du vil knytte nye domener til e-handelsmiljøet etter at e-handel initialiseres, må du sende en serviceforespørsel.

## <a name="additional-resources"></a>Tilleggsressurser

[Distribuere et nytt e-handelsområde](deploy-ecommerce-site.md)

[Definere en kanal for nettbutikk](online-stores.md)

[Opprette et e-handelsområde](create-ecommerce-site.md)

[Knytte et nettområde til en kanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Laste opp URL-adresser for omadressering samtidig](upload-bulk-redirects.md)

[Konfigurere en B2C-leier i Commerce](set-up-B2C-tenant.md)

[Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md)

[Konfigurere flere B2C-leiere i et Commerce-miljø](configure-multi-B2C-tenants.md)

[Legge til støtte for et innholdsleveringsnettverk (CDN)](add-cdn-support.md)

[Aktivere stedsbasert butikkregistrering](enable-store-detection.md)
