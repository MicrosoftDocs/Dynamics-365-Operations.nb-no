---
title: Aktivere stedsbasert butikkregistrering
description: Dette emnet beskriver hvordan du aktiverer stedsbasert butikkregistrering for Dynamics 365 Commerce-området.
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a542d6987280451910b4ff3bcfb3a109a0e028c6
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697618"
---
# <a name="enable-location-based-store-detection"></a>Aktivere stedsbasert butikkregistrering

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du aktiverer stedsbasert butikkregistrering for Dynamics 365 Commerce-området.

## <a name="overview"></a>Oversikt

Med stedsbasert butikkregistrering i Commerce kan du gi relevant områdeinnhold til kunder basert på lokasjonen. Når stedsbasert butikkregistrering er aktivert, bruker Commerce-gjengivelsestjenesten lands-/områdeinformasjonen fra IP-adressen til kundens webleser til å dirigere kunden til den beste geografiske områdekonfigurasjonen som er tilgjengelig.

## <a name="privacy-notice"></a>Personvernerklæring

Hvis du aktiverer den stedsbaserte butikkregistreringsfunksjonen, sendes informasjon fra kundens webleser til en Microsoft-stedstjeneste. Denne informasjonen brukes deretter til å angi kundeinnholdet som er relevant for hans eller hennes lokasjon. Både informasjon som sendes fra kundens webleser, og den stedsbaserte informasjonen som returneres til kunden, er underlagt retningslinjer for personvern og informasjonskapsler.

## <a name="turn-on-location-based-store-detection"></a>Aktivere stedsbasert butikkregistrering

Følg denne fremgangsmåten for å aktivere stedsbasert butikkregistrering i Commerce.

1. Gå til området ditt i redigeringsverktøyet.
1. Velg **Områdebehandling** i navigasjonsruten til venstre.
1. Velg **Områdeinnstillinger**.
1. Sett **Aktiver registrering av plasseringsbasert butikk** til **På**.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over nettbutikk](online-store-overview.md)

[Opprette et e-handelsområde](create-ecommerce-site.md)

[Distribuere et nytt e-handelsområde](deploy-ecommerce-site.md)

[Knytte et nettområde til en kanal](associate-site-online-store.md)

[Konfigurere domenenavnet](configure-your-domain-name.md)

[Legge til støtte for et innholdsleveringsnettverk (CDN)](add-cdn-support.md)

[Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md)
