---
title: Forutsetninger for kanaloppsett
description: Dette emnet viser en oversikt over forutsetninger for kanaloppsett i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002295"
---
# <a name="channel-setup-prerequisites"></a>Forutsetninger for kanaloppsett


[!include [banner](includes/banner.md)]

Dette emnet viser en oversikt over forutsetninger for kanaloppsett i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Før en Dynamics 365 Commerce-kanal kan opprettes, må du fullføre en rekke nødvendige oppgaver. Følgende lister over nødvendige oppgaver er ordnet etter kanaltype.

> [!NOTE]
> Det skrives fremdeles en del dokumentasjon, og koblingene blir oppdatert etter hvert som nytt innhold publiseres.

## <a name="initialization"></a>Initialisering

- [Initialisere utgangsverdidata](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Globale forutsetninger kreves for alle kanaltyper

- [Definere og konfigurere strukturen for juridisk enhet](channels-legal-entities.md) 
- [Konfigurere organisasjonshierarkiet](channels-org-hierarchies.md)
- [Definere et lager](channels-setup-warehouse.md)
- [Konfigurere merverdiavgift](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [Definere en profil for e-postvarsling](email-notification-profiles.md)
- [Definere nummerserier](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [Definere en standardkunde og adressebok](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Forutsetninger for detaljhandelskanal

- [Informasjonskoder og informasjonskodegrupper](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [Definere en funksjonalitetsprofil for detaljhandel](retail-functionality-profile.md)
- [Konfigurere en adressebok for ansatt](new-address-book.md)
- [Definere et skjermoppsett](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [Konfigurere en maskinvarestasjon](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a>Forutsetninger for telefonsenterkanal

- Telefonsenterparametere
- Refunderingsmetoder for telefonsenter
- Utleietyper
- Betalingstjenester
- Ordresperrekoder

## <a name="online-channel-prerequisites"></a>Forutsetninger for Internett-kanal

- [Opprett en Internett-funksjonalitetsprofil](online-functionality-profile.md)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over kanaler](channels-overview.md)

[Oversikt over organisasjoner og organisasjonshierarkier](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Definere organisasjonshierarkier](channels-org-hierarchies.md)

[Opprett juridiske enheter](channels-legal-entities.md)

[Definere en detaljhandelskanal](channel-setup-retail.md)
    
[Definere en Internett-kanal](channel-setup-online.md)
