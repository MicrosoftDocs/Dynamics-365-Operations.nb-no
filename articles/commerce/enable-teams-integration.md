---
title: Aktiver Dynamics 365 Commerce- og Microsoft Teams-integrering
description: Dette emnet beskriver hvordan du aktiverer Microsoft Dynamics 365 Commerce- og Microsoft Teams-integrering.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c4d596f27ffe15a97dc04e2ce7e85d21f8e7161f
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908401"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Aktiver Dynamics 365 Commerce- og Microsoft Teams-integrering

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du aktiverer Microsoft Dynamics 365 Commerce- og Microsoft Teams-integrering.

Hvis du vil klargjøre Teams med informasjon fra Dynamics 365 Commerce og synkronisere oppgavebehandlingsfunksjonene mellom Teams og POS-programmet (salgsstedet), må du aktivere integreringsfunksjonene i Commerce Headquarters.

> [!NOTE]
> Når du aktiverer Teams-integrering, godtar du å dele dataene dine med Teams. Data som deles med Teams, kan ligge i et annet land enn Commerce-dataene, og de kan være underlagt andre samsvarsstandarder. Hvis du vil ha mer informasjon om disse endringene, kan du se [Microsoft Trust Center](https://www.microsoft.com/trust-center). Hvis du vil ha informasjon om Microsofts personvernerklæringer, kan du se [Microsofts personvernerklæring](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>Aktiver Teams-integrering

Før du kan aktivere Microsoft Teams-integrering med Commerce, må du registrere Teams-programmet med leieren i Azure-portalen.

Følg denne fremgangsmåten for å registrere Teams-programmet med leieren i Azure-portalen.

1. følg trinnene i [Hurtigstart: Registrer en app i Microsoft-identitetsplattformen](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) for å registrere Teams-appen med leieren i Azure-portalen.
1. Kopier verdien for **App-ID (klient)** fra **Oversikt**-siden for den registrerte appen. Du bruker denne verdien for å aktivere Teams-integrering i Commerce Headquarters.
1. Kopier sertifikatverdien som ble angitt da du [la til et sertifikat](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) i trinn 1. Sertifikatet kalles også offentlig nøkkel eller programnøkkel. Du bruker denne verdien for å aktivere Teams-integrering i Commerce Headquarters.

Følg denne fremgangsmåten for å aktivere Teams-integrering i Commerce Headquarters.

1. Gå til **Retail og Commerce \> Kanaloppsett \> Konfigurasjon av Microsoft Teams-integrering**.
1. I handlingsruten velger du **Rediger**.
1. Sett alternativet **Aktiver Microsoft Teams-integrering** til **Ja**.
1. I feltene **App-ID** og **Appnøkkel** angir du verdiene du fikk da du registrerte Teams-appen i Azure-portalen.
1. Velg **Lagre** i handlingsruten.

Illustrasjonen nedenfor viser et eksempel på konfigurasjonen av Teams-integrering i Commerce Headquarters.

![Konfigurasjon av Teams-integrering i Commerce Headquarters](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>Deaktiver Teams-integrering

Følg denne fremgangsmåten for å deaktivere Microsoft Teams-integrering i Commerce Headquarters.

1. Gå til **Retail og Commerce \> Kanaloppsett \> Konfigurasjon av Microsoft Teams-integrering**.
1. I handlingsruten velger du **Rediger**.
3. Sett alternativet **Aktiver Microsoft Teams-integrering** til **Nei**.
4. Fjern verdiene fra feltene **App-ID** og **Appnøkkel**.
1. Velg **Lagre** i handlingsruten.

> [!NOTE]
> Når du har deaktivert Teams-integrering med Commerce, vil ikke POS-terminaler lenger vise oppgaver som er publisert fra Teams-appen.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over Dynamics 365 Commerce- og Microsoft Teams-integrering](commerce-teams-integration.md)

[Klargjøring av Microsoft Teams fra Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Synkroniser oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Behandle brukerroller i Microsoft Teams](manage-user-roles-teams.md)

[Tilordne butikker og grupper hvis det finnes eksisterende grupper i Microsoft Teams](map-stores-existing-teams.md)

[Vanlige spørsmål om Dynamics 365 Commerce- og Microsoft Teams-integrering](teams-integration-faq.md)
