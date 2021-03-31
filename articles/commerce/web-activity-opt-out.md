---
title: Velge bort samling for webaktivitetshendelse
description: I dette emnet finner du informasjon om hvordan du kan la besøkende på nettstedet velge bort en samling for webaktivitetshendelse i Microsoft Dynamics 365 Commerce.
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 244d612fa01529df4fff250df50a06526632fcf1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210929"
---
# <a name="opt-out-of-web-activity-event-collection"></a>Velge bort samling for webaktivitetshendelse
[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du kan la kundene velge bort samling for webaktivitetshendelse i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Dynamics 365 Commerce lar områdeadministratorer analysere webaktiviteten til brukere av sine områder for e-handel. På denne måten kan de bedre forstå hvordan områdene brukes, og de kan optimalisere områdene for å gi en forbedret brukeropplevelse og oppfylle forretningsmålene.


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>Metoder administratorer kan bruke til å implementere mulighet for brukere å velge bort ting

Administratorer kan implementere mulighet for brukere å velge bort ting på tre måter.

### <a name="opt-out-on-behalf-of-users"></a>Velge bort på vegne av brukeren

I Kontobehandling i Commerce Headquarters (HQ) kan administratorer velge bort på vegne av brukeren.

1. I HQ-klienten søker du etter og velger en kunde på siden **Alle kunder**.
1. På siden for kundedetaljer setter du alternativet **Ikke spor webaktivitet** til **Ja** i delen **Personvern** i hurtigkategorien **Detaljhandel**.

    ![Personverninnstillinger](media/Disablepersonalizationpart2.png)

1. Velg **Lagre**, og lukk deretter siden.

### <a name="module-based-opt-out-experience"></a>Modulbasert bortvalgsopplevelse

Administratorer kan la godkjente brukere velge bort samling for webaktivitshendelse selv. Hvis du vil gi denne bortvalgsopplevelsen, legger du til en bortvalgsmodul for brukerne på profilsidene for kundekontoer.

### <a name="custom-extensions"></a>Egendefinerte tillegg

Administratorer kan opprette egne tillegg for å administrere bortvalgsopplevelsen for brukere. Hvis du vil ha mer informasjon, kan du se [Kalle API-er for Retail Server](e-commerce-extensibility/call-retail-server-apis.md) og [Utvidelsesmulighet for Internett-kanal](e-commerce-extensibility/overview.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]