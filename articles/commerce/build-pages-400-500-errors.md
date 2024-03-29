---
title: Bygg egendefinerte svarsider for 4xx/5xx-statuskodefeil
description: Denne artikkelen beskriver hvordan du bygger egendefinerte svarsider for 4xx- og 5xx-statuskodefeil ved hjelp av redigeringsverktøyene i Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4a3b1762cebc74c1b77f9ca60925608bc966e306
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276407"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>Bygg egendefinerte svarsider for 4xx/5xx-statuskodefeil

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du bygger egendefinerte svarsider for 4xx- og 5xx-statuskodefeil ved hjelp av redigeringsverktøyene i Microsoft Dynamics 365 Commerce.

Hvis en forespørsel ikke lykkes, utsteder serveren svar på HTTP-statuskodefeil. Statuskoden 404 registreres og returneres hvis en side ikke blir funnet, og 500 statuskoden fanges opp og returneres hvis det oppstår en serverfeil. I Dynamics 365 Commerce kan programbrukere bygge egendefinerte svarsider for statuskodefeil som vises for brukere for disse statuskodefeilsvarene.

## <a name="build-a-status-code-error-response-page"></a>Bygge en svarside for statuskodefeil

Følg denne fremgangsmåten for å begynne å bygge en svarside for statuskodefeil.

1. I den foretrukne webleseren logger du på Dynamics 365 Commerce. 
1. Velg området du vil bygge en svarside for 4xx/5xx-statuskodefeil for.

### <a name="build-the-template"></a>Bygge malen

Følg denne fremgangsmåten for å bygge malen for svarsiden for statuskodefeil.

1. Gå til **Maler**.
1. Velg **Ny** for å opprette en sidemal.
1. I dialogboksen **Ny mal**, under **Malnavn**, angir du et navn for den nye malen, og velger deretter **OK**.
1. Bygg malen på grunnlag av strukturen du vil at svarsiden for statuskodefeil skal ha.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den. 

### <a name="build-the-status-code-error-response-page"></a>Bygge svarsiden for statuskodefeil

Følg denne fremgangsmåten for å bygge svarsiden for statuskodefeil.

1. Gå til **Sider**.
1. Velg **Ny** for å opprette en side.
1. Velg en mal i dialogboksen **Velg en mal**, og skriv deretter inn et navn for svarsiden for statuskodefeil under **Sidenavn**. La feltet **URL-adresse for side** være tomt.
1. Bygg siden.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

> [!NOTE]
> Du kan opprette separate svarsider for statuskodefeil for 4xx- og 5xx-statuskodefeil. Du kan også bruke den samme generelle svarsiden statuskodefeil for begge feilkategorier.

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a>Definere en omadressering for svarsiden for statuskodefeil

Følg denne fremgangsmåten for å opprette en omadressering for svarsiden for statuskodefeil.

1. Gå til **URL-adresser \> Ny \> Nytt alias**, og velg svarsiden for statuskodefil som du bygde tidligere.
1. I feltet **Alias** angir du **default-4xx** eller **default-5xx**, avhengig av hvilken svarside for statuskodefeil du definerer en omadressering for. Disse aliasene må publiseres. Hvis ikke fungerer ikke omadresseringen.
1. Velg **OK** for å aktivere koblingen.

> [!NOTE]
> Hvis du bruker én svarside for statuskodefeil for begge feilkategoriene, gjentar du denne fremgangsmåten for å koble et alias for den andre feilkategorien til den samme siden.

## <a name="additional-resources"></a>Tilleggsressurser

[Arbeide med maler](work-with-templates.md)

[Legg til en ny områdeside](add-new-page.md)

[Opprette en URL-adresse for side](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
