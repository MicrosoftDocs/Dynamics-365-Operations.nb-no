---
title: Registrere deg for og installere tjenesten for elektronisk fakturering
description: Denne artikkelen gir informasjon om hvordan du registrerer deg for og installerer tjenesten for elektronisk fakturering.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 57314058883e60599bc51d91a65b0daeae724bb7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865533"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>Registrere deg for og installere tjenesten for elektronisk fakturering

[!include [banner](../includes/banner.md)]

Denne artikkelen gir informasjon om hvordan du registrerer deg for og installerer tjenesten for elektronisk fakturering. Denne prosessen består av fire trinn. Trinn 1 til og med 3 er nødvendig, og trinn 4 er valgfritt.

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>Trinn 1: Registrer deg for Regulatory Configuration Service

Regulatory Configuration Service (RCS) gir deg konfigurasjonen og utformingen som brukes til å konfigurere elektronisk fakturering. Ressurser som miljøer og funksjoner for elektroniske fakturering opprettes, vedlikeholdes og administreres i RCS. Når ressursene er klare, publiseres de i tjenesten for elektronisk fakturering.

Hvis du vil ha mer informasjon om RCS, kan du se [Regulatory Configuration Services (RCS) – globaliseringsfunksjoner](rcs-globalization-feature.md).

Du kan registrere deg for RCS på siden [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>Trinn 2: Installer tilleggsprogrammet for mikrotjenester i Microsoft Dynamics Lifecycle Services

Tjenesten for elektronisk fakturering er et sett med mikrotjenester som driftes i Microsofts datasentre. Kunder av Dynamics 365 Finance og Dynamics 365 Supply Chain Management har som standard ikke tilgang til tjenesten for elektronisk fakturering. Du må installere den som et tilleggsprogram i Microsoft Dynamics Lifecycle Services (LCS). Når du installerer tilleggsprogrammet, registreres Finance- eller Supply Chain Management-miljøet i registeret for programmer som har tillatelse til å koble seg til tjenesten for elektronisk fakturering.

For å fullføre dette trinnet ser du [Installer tilleggsprogrammet for mikrotjenester i Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md).

### <a name="step-3-set-up-rcs"></a>Trinn 3: Konfigurer RCS

Du må konfigurere integreringen mellom RCS og tjenesten for elektronisk fakturering. Du må også konfigurere hovedkomponentene.

For å fullføre dette oppsettet ser du [Konfigurere Regulatory Configuration Service (RCS)](e-invoicing-set-up-rcs.md).

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>Trinn 4: Administratorreferanse for Microsoft Power Platform-programtillegg

Noen scenarioer krever integrering med Dataverse innenfor Microsoft Power Platform.

Dette oppsettet er for øyeblikket obligatorisk hvis du skal bruke løsninger for elektronisk fakturering i scenarioer med indonesisk elektronisk fakturering. Det er imidlertid valgfritt for scenarioer med saudiarabisk elektronisk fakturering. Hvis du vil ha mer informasjon, kan du se [Tilgjengelighet av funksjoner for elektronisk fakturering etter land eller område](e-invoicing-country-specific-availability.md).

Du kan fullføre dette trinnet ved å se i [Administratorreferanse for Microsoft Power Platform-programtillegg](e-invoicing-power-platform-plug-in.md).
