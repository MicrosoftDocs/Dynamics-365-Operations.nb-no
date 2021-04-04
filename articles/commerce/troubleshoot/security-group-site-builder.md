---
title: Kan ikke konfigurere en sikkerhetsgruppe for Commerce-områdebygger under første distribusjon
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når sikkerhetsgruppen for Commerce-områdebyggeren for Microsoft Azure Active Directory (Azure AD) ikke vises som et alternativ når du oppretter e-handelskomponenter i Microsoft Dynamics Lifecycle Services (LCS) under første distribusjon av en ny e-handelsleier.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36ea43e19f395e3914d3eda1a9b8f5487b0926c5
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585468"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>Kan ikke konfigurere en sikkerhetsgruppe for Commerce-områdebygger under første distribusjon

[!include [banner](../../includes/banner.md)]

Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når sikkerhetsgruppen for Commerce-områdebyggeren for Microsoft Azure Active Directory (Azure AD) ikke vises som et alternativ når du oppretter e-handelskomponenter i Microsoft Dynamics Lifecycle Services (LCS) under første distribusjon av en ny e-handelsleier.

## <a name="description"></a>beskrivelse

Når du oppretter e-handelskomponentene som en del av prosessen med å distribuere en ny e-handel-leietaker som inneholder komponenten for commerce site builder, vises ikke sikkerhetsgruppen i Azure AD som et alternativ i dialogboksen.

## <a name="resolution"></a>Oppløsning

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>Klargjøre e-handelsområdet med en bruker i riktig leietaker

1. Gå til [Azure-portalen](https://portal.azure.com/).
1. Følg instruksjonene i [Opprett en grunnleggende gruppe og legg til medlemmer ved hjelp av Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal) under den leietakeren som LCS-prosjektet for e-handel er klargjort for.
1. Gå til [LCS](https://lcs.dynamics.com/), og logg på med en konto som deler samme leietaker som sikkerhetsgruppen for Azure AD du akkurat opprettet. Kontoen må ha tilgang til å vise sikkerhetsgruppen for Azure AD.
1. Fullfør trinnene i oppsettet for å konfigurere e-handelsområdet. Når du klargjør e-handelskomponentene, skal sikkerhetsgruppen nå vises som et alternativ i dialogboksen.

> [!NOTE]
> Hvis du vil være sikker på at feltet i dialogboksen er fylt ut med listen med sikkerhetsgrupper, må du velge **Angi** etter at du har angitt navnet på sikkerhetsgruppen for Azure AD du opprettet. Søkeresultatene viser alle sikkerhetsgruppene for Azure AD som starter med søketeksten, og som brukeren har tilgang til. Du kan bruke en kortere søketerm for å tillate bredere søkeresultater.

## <a name="additional-resources"></a>Tilleggsressurser

[Opprette en grunnleggende gruppe og legge til medlemmer ved hjelp av Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[Distribuere en ny e-handelsleier](../deploy-ecommerce-site.md)