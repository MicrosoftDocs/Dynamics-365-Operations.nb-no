---
title: Oppsett for elektronisk fakturering
description: Denne artikkelen gir en oversikt over prosessen for oppsett og konfigurasjon av elektronisk fakturering.
author: gionoder
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: de94843c1e98a8788375bd41def587a64baea07d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272187"
---
# <a name="electronic-invoicing-setup"></a>Oppsett for elektronisk fakturering

[!include [banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over prosessen for oppsett og konfigurasjon av elektronisk fakturering. Du må fullføre trinnene i oppsettet i rekkefølgen som er angitt her. Hvis du hopper over et obligatorisk trinn, fungerer ikke funksjonaliteten som den skal, og det oppstår flere feil i de påfølgende trinnene eller når du bruker funksjonaliteten. 

Før du begynner, må du kontrollere at alle hovedkomponentene er riktig konfigurert, at du har registrert deg for Regulatory Configuration Service (RCS) og har en forekomst av RCS, og at tilleggsprogrammet for elektronisk fakturering er installert for Microsoft Dynamics 365 Finance- eller Dynamics 365 Supply Chain Management-miljøet. Hvis du vil ha mer informasjon, kan du se [Registrer og installer elektronisk fakturering](e-invoicing-install-add-in-microservices-lcs.md).

Deretter konfigurerer du Azure-ressurser som elektronisk fakturering trenger for å fungere. Du finner mer informasjon under [Konfigurere Azure-ressurser for elektronisk fakturering](e-invoicing-set-up-azure-resources.md).

Etter at hovedkomponentene er konfigurert, kan du arbeide med RCS for å konfigurere de logiske hovedkomponentene for elektronisk fakturering. Først definerer du antall tjenestemiljøer du vil vedlikeholde. Dermed definerer du de logiske dataene og konfigurasjonspartisjoneringen for å sikre at du har en grense mellom et utviklings- eller testmiljø og produksjonsmiljøene. Hvis du vil konfigurere utviklingsprosessen på en fleksibel måte, må du kanskje ha flere atskilte utviklings- og testmiljøer. I tillegg til å definere tjenestemiljøer oppretter du en kobling til forretningsprogrammene, for eksempel Finance eller Supply Chain Management, direkte fra RCS for å konfigurere parameterne som kreves for at dette skal fungere riktig med elektronisk fakturering. Hvis du vil ha mer informasjon om miljøene, kan du se [Tjenestemiljøer](e-invoicing-service-environments.md).

Etter at alt er konfigurert, kan du opprette dine egne globaliseringsfunksjoner som definerer ulike scenarioer for behandling av elektroniske dokumenter og transformering av data, eller for å importere dokumentene fra det globale repositoriet. Hvis du vil ha mer informasjon om hvordan du arbeider med globaliseringsfunksjoner, kan du se [Arbeid med globaliseringsfunksjoner](e-invoicing-working-globalization-features.md).

Hvis scenarioene krever integrering med e-post eller SharePoint for å behandle innkommende elektroniske dokumenter, kan du se [Behandling av innkommende elektroniske dokumenter](e-invoicing-process-incoming-electronic-documents.md) for å få informasjon om hvordan du konfigurerer og bruker disse kanalene.
