---
title: Velkomst-e-post sendes ikke når nye kunder opprettes
description: Dette emnet gir feilsøkingsveiledning som kan være til hjelp hvis en velkomst-e-postvarsling ikke sendes når en ny kunde opprettes i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 1a4faf6cd189f69232e7f9ab8d0e79b320cfe2d9
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349960"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Velkomst-e-post sendes ikke når nye kunder opprettes

[!include [banner](../../includes/banner.md)]

Dette emnet gir feilsøkingsveiledning som kan være til hjelp hvis en velkomst-e-postvarsling ikke sendes når en ny kunde opprettes i Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Beskrivelse

Når en ny kunde opprettes i Commerce Headquarters, sendes det ikke en velkomst-e-post til kunden, selv om det er konfigurert en e-postvarsling for e-postvarslingstypen **Kunden er opprettet**.

## <a name="resolution"></a>Oppløsning

### <a name="set-the-correct-email-id-value-for-the-customer-created-email-notification-type"></a>Angi riktig verdi for E-post-ID for e-postvarslingstypen Kunden er opprettet

Følg denne fremgangsmåten for å angi riktig verdi for **E-post-ID** for e-postvarslingstypen **Kunden er opprettet** i Headquarters.

1. Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Handelsprofil for e-postvarsling**.
1. Velg profilen for e-postvarsling i den venstre navigasjonsruten.
1. Angi **NewCust** i feltet **E-post-ID** for e-postvarslingstypen **Kunden er opprettet** under **Varslingsinnstillinger for detaljhandelshendelse**.

## <a name="additional-resources"></a>Tilleggsressurser

[Definere en profil for e-postvarsling](../email-notification-profiles.md)
