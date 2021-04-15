---
title: Opprette organisasonsmodellhierarkier for B2B-organisasjoner
description: Dette emnet beskriver hvordan du oppretter organisasjonsmodellhierarkier for bedrift-til-bedrift-organisasjoner (B2B).
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 487af939f92ece8bc3e543b3beeffa239baa1863
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799835"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a>Opprette organisasonsmodellhierarkier for B2B-organisasjoner

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du oppretter organisasjonsmodellhierarkier for bedrift-til-bedrift-organisasjoner (B2B) i Microsoft Dynamics 365 Commerce.

I Commerce Headquarters representeres forretningspartnerorganisasjoner av kunde- og kundehierarkienheter. Forretningspartnerorganisasjonen og dens brukere representeres som kunder, og kundehierarkier brukes til å knytte disse kundene til hverandre.

Når en forretningspartnerforespørsel om å delta i et B2B-e-handelsområde godkjennes, utføres følgende handlinger:

- To nye kundeposter opprettes i systemet: en **Type Organisasjon**-kundepost for forretningspartnerorganisasjonen og en kundepost av typen **Type Person** for anmoderen (det vil si forretningspartnerbrukeren som sendte forespørselen).
- Det opprettes en ny kundehierarkipost under **Kunde \> Kundehierarki**. Denne posten har følgende hodeegenskaper:

    - **Kundehierarki-ID** – En unik ID for kundehierarkiet. Denne IDen bruker nummerserien som er definert i Delte handelsparametere i Commerce Headquarters.
    - **Navn** – Organisasjonsnavnet til forretningspartneren, som angitt i forespørselen om pålasting.
    - **Formål** – Denne egenskapen er satt til den forhåndsdefinerte verdien **B2B-organisasjon**.
    - **Organisasjon** – Kunde-IDen til forretningspartneren.

Her er detaljene i kundehierarkiposten:

- Kundeposten til anmoderen er knyttet til kundehierarkiet.
- Administratorrollen er knyttet til anmoderen.

Når administratoren legger til flere brukere i forretningspartnerorganisasjonen på et B2B-område, opprettes det en ny kundepost for hver bruker i Commerce Headquarters. Denne kundeposten legges også til i den relevante kundehierarkiposten for forretningspartneren og har rollen "bruker".

> [!NOTE]
> I de fleste tilfeller bør tilsvarende egenskapsverdier for alle kundeposter i et hierarki samsvare. Fordi alle forretningspartnerbrukere for eksempel skal få like priser for produkter, bør prisgruppen og tilknyttede konfigurasjoner samsvare. Systemet iverksetter imidlertid ikke denne konsistensen. Derfor er de relevante Commerce Headquarters-brukerne ansvarlige for å sikre at egenskapsverdiene og konfigurasjonene samsvarer for alle kunder i et gitt hierarki.

Commerce Headquarters-brukere kan se på egenskapsverdiene for alle kundeposter i hierarkiet i side-ved-side-visning. Velg de relevante kundepostegenskapene ved å velge kategorinavnene på rullegardinmenyen. Brukere kan vise og redigere egenskapsverdiene direkte fra denne visningen. Hvis du vil bruke alle verdiene fra administratorkundeposten på alle brukerkundepostene, kan du velge **Overstyr** i kundehierarkidetaljene.

## <a name="additional-resources"></a>Tilleggsressurser

[Definere et B2B-e-handelsområde](set-up-b2b-site.md)

[Administrere forretningspartnerbrukere på B2B-e-handelsområder](manage-b2b-users.md)

[Konfigurere kundekontobetalingsmetode for B2B-e-handelsområder](payment-method.md)

[Angi produktantallsgrenser for B2B-e-handelsområder](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]