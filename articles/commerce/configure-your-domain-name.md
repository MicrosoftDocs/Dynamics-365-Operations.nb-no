---
title: Konfigurer domenenavnet
description: Denne artikkelen beskriver hvordan du konfigurerer et domenenavn for et e-handelsområde for Microsoft Dynamics 365.
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
ms.openlocfilehash: 00c75581ba08979dfbc784f949c30b9bf78d44c9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892137"
---
# <a name="configure-your-domain-name"></a>Konfigurer domenenavnet


[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer et domenenavn for et e-handelsområde for Microsoft Dynamics 365. 

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