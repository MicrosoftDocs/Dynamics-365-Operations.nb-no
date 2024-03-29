---
title: Begrense tilgang til en butikkfasade under testing eller utvikling
description: Denne artikkelen beskriver hvordan du begrenser tilgang til en Microsoft Dynamics 365 Commerce-butikkfasade når det skjer intern testing eller utvikling.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: e382f01f82b368ad89f7abf122bf806dca4f0340
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292034"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a>Begrense tilgang til en butikkfasade under testing eller utvikling

[!include [banner](../../includes/banner.md)]

Denne artikkelen beskriver hvordan du begrenser tilgang til en Microsoft Dynamics 365 Commerce-butikkfasade når det skjer intern testing eller utvikling.

## <a name="description"></a>beskrivelse

Under intern testing eller aktiv utvikling kan det hende at du vil begrense tilgangen til området for å hindre at eksterne brukere får tilgang til de publiserte butikkområdesidene.

## <a name="resolution"></a>Oppløsning

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a>Konfigurere Azure AD B2C ved hjelp av standard brukerflyter

Hvis du vil ha mer informasjon om hvordan du konfigurerer Azure Active Directory B2C (Azure AD B2C) for e-handelsområdet, kan du se [Definere en B2C-leier i Commerce](../set-up-b2c-tenant.md).

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a>Begrense brukertilgang til butikksider og blokkere oppretting av nye brukere

Følg denne fremgangsmåten for å begrense brukertilgang til butikksider i Commerce-områdebyggeren.

1. Gå til området ditt.
1. Velg **Sider**, og velg deretter siden du vil begrense brukertilgang for.
1. Velg modul- eller fragmentsporet, og velg deretter **Rediger**.
1. Velg **Krever pålogging?** i egenskapsruten, og velg deretter **Fullfør redigering**.
1. Velg **Publiser**.

Følg denne fremgangsmåten for å blokkere opprettingen av nye Azure AD-brukere.

1. Gå til [Azure-portalen](https://portal.azure.com/).
1. Velg Azure AD B2C-programmet du opprettet for områdetilgang.
1. Velg **Brukerflyter** til venstre.
1. Øverst på siden **Brukerflyter** velger du **Ny brukerflyt**.
1. Velg **Forhåndsvisning** på siden **Velg en brukerflyttype**.
1. På midten av siden velger du **Logg på v2**. Følg deretter trinnene i [Konfigurere en B2C-leier i Commerce](../set-up-b2c-tenant.md) for å konfigurere flyten som områdets standard brukerflyt for Azure AD B2C under testing eller utvikling.

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere en B2C-leier i Commerce](../set-up-b2c-tenant.md)

[Definere egendefinerte sider for brukerpålogginger](../custom-pages-user-logins.md)
