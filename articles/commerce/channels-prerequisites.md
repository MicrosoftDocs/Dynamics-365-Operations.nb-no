---
title: Kanaloppsettsforutsetninger
description: Denne artikkelen viser en oversikt over forutsetninger for kanaloppsett i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 98ca2dc4691534853467c1680890199d08bc4e79
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282302"
---
# <a name="channel-setup-prerequisites"></a>Kanaloppsettsforutsetninger

[!include [banner](includes/banner.md)]

Denne artikkelen viser en oversikt over forutsetninger for kanaloppsett i Microsoft Dynamics 365 Commerce.

Før en Dynamics 365 Commerce-kanal kan opprettes, må du fullføre en rekke nødvendige oppgaver. Følgende lister over nødvendige oppgaver er ordnet etter kanaltype.

> [!NOTE]
> Det skrives fremdeles en del dokumentasjon, og koblingene blir oppdatert etter hvert som nytt innhold publiseres.

## <a name="initialization"></a>Initialisering

- [Initialisere utgangsverdidata](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Globale forutsetninger kreves for alle kanaltyper

- [Definere og konfigurere strukturen for juridisk enhet](channels-legal-entities.md) 
- [Konfigurere organisasjonshierarkiet](channels-org-hierarchies.md)
- [Definere et lager](channels-setup-warehouse.md)
- [Konfigurere merverdiavgift](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [Definere en profil for e-postvarsling](email-notification-profiles.md)
- [Definere nummerserier](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [Definere en standardkunde og adressebok](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Forutsetninger for detaljhandelskanal

- [Informasjonskoder og informasjonskodegrupper](info-codes-retail.md)
- [Definere en funksjonalitetsprofil for detaljhandel](retail-functionality-profile.md)
- [Konfigurere en adressebok for ansatt](new-address-book.md)
- [Definere et skjermoppsett](pos-screen-layouts.md)
- [Konfigurere en maskinvarestasjon](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a>Forutsetninger for telefonsenterkanal

- Telefonsenterparametere
- [Telefonsenterordrer og refusjonsbetalingsmåter](work-with-payments.md)
- [Leveringsmåter og tillegg for telefonsenter](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a>Forutsetninger for nettkanal

- [Opprette en nettbasert funksjonalitetsprofil](online-functionality-profile.md)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over kanaler](channels-overview.md)

[Oversikt over organisasjoner og organisasjonshierarkier](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Definere organisasjonshierarkier](channels-org-hierarchies.md)

[Opprett juridiske enheter](channels-legal-entities.md)

[Definere en detaljhandelskanal](channel-setup-retail.md)
    
[Definere en Internett-kanal](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
