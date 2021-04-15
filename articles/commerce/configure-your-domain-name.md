---
title: Konfigurere domenenavnet
description: Dette emnet beskriver hvordan du konfigurerer et domenenavn for et e-handelsområde for Microsoft Dynamics 365.
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d41168da44100a09c58b8c05367ab45bbd62a30
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796057"
---
# <a name="configure-your-domain-name"></a>Konfigurere domenenavnet


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer et domenenavn for et e-handelsområde for Microsoft Dynamics 365. 

## <a name="add-domains-during-e-commerce-initialization"></a>Legge til domener under initialisering av e-handel

Hvis du vil knytte domener til Dynamics 365 Commerce-e-handelsmiljøet, kan du initialisere e-handel som beskrevet i [Distribuere en ny e-handelsleier](deploy-ecommerce-site.md). Under initialiseringen blir du bedt om å oppgi informasjon som skal brukes til å klargjøre ditt e-handelsmiljø. Legg til alle domenene du planlegger å bruke med dette miljøet, i feltet **Støttede vertsnavn**. Flere domener må skilles med semikolon. På denne måten konfigureres domenene i alle de nødvendige Commerce-komponentene, og de er klare til bruk når du bytter trafikk fra innholdsleveringsnettverket (CDN) eller nettserveren og peker den til e-handel-frontene.

## <a name="add-domains-after-e-commerce-initialization"></a>Legge til domener etter initialisering av e-handel

Hvis du vil knytte nye domener til e-handelsmiljøet etter at e-handel initialiseres, må du sende en serviceforespørsel.

## <a name="additional-resources"></a>Tilleggsressurser

[Distribuere en ny e-handelsleier](deploy-ecommerce-site.md)

[Opprette et e-handelsområde](create-ecommerce-site.md)

[Knytte et Dynamics 365 Commerce-nettsted til en nettkanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Laste opp masseomdirigeringer for URL-adresse](upload-bulk-redirects.md)

[Konfigurere en B2C-leier i Commerce](set-up-B2C-tenant.md)

[Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md)

[Konfigurere flere B2C-leiere i et Commerce-miljø](configure-multi-B2C-tenants.md)

[Legge til støtte for et innholdsleveringsnettverk (CDN)](add-cdn-support.md)

[Aktivere stedsbasert butikkregistrering](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]