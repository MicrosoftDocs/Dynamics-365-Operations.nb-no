---
title: Velg bort samling for nettaktivitetshendelse
description: I denne artikkelen finner du informasjon om hvordan du kan la besøkende på nettstedet velge bort en samling for webaktivitetshendelse i Microsoft Dynamics 365 Commerce.
author: aamiral
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 78d3f795820eb36d1a81fb28875456e7471f8971
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878405"
---
# <a name="opt-out-of-web-activity-event-collection"></a>Velg bort samling for nettaktivitetshendelse
[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du kan la kundene velge bort samling for webaktivitetshendelse i Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce lar områdeadministratorer analysere webaktiviteten til brukere av sine områder for e-handel. På denne måten kan de bedre forstå hvordan områdene brukes, og de kan optimalisere områdene for å gi en forbedret brukeropplevelse og oppfylle forretningsmålene.


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>Metoder administratorer kan bruke til å implementere mulighet for brukere å velge bort ting

Administratorer kan implementere mulighet for brukere å velge bort ting på tre måter.

### <a name="opt-out-on-behalf-of-users"></a>Velge bort på vegne av brukeren

I Kontobehandling i Commerce Headquarters (HQ) kan administratorer velge bort på vegne av brukeren.

1. I HQ-klienten søker du etter og velger en kunde på siden **Alle kunder**.
1. På siden for kundedetaljer setter du alternativet **Ikke spor webaktivitet** til **Ja** i delen **Personvern** i hurtigkategorien **Detaljhandel**.

    ![Personverninnstillinger.](media/Disablepersonalizationpart2.png)

1. Velg **Lagre**, og lukk deretter siden.

### <a name="module-based-opt-out-experience"></a>Modulbasert bortvalgsopplevelse

Administratorer kan la godkjente brukere velge bort samling for webaktivitshendelse selv. Hvis du vil gi denne bortvalgsopplevelsen, legger du til en bortvalgsmodul for brukerne på profilsidene for kundekontoer.

### <a name="custom-extensions"></a>Egendefinerte tillegg

Administratorer kan opprette egne tillegg for å administrere bortvalgsopplevelsen for brukere. Hvis du vil ha mer informasjon, kan du se [Kalle API-er for Retail Server](e-commerce-extensibility/call-retail-server-apis.md) og [Utvidelsesmulighet for Internett-kanal](e-commerce-extensibility/overview.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
