---
title: Proaktive nettpratparametere for Commerce-nettpratmodulen
description: Denne artikkelen beskriver de proaktive nettpratparameterne for Commerce-nettpratmoduler i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: f3cff89a25ff84414e7fdd32cbb26404c2080187
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691075"
---
# <a name="commerce-chat-module-proactive-chat-parameters"></a>Proaktive nettpratparametere for Commerce-nettpratmodulen

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver de proaktive nettpratparameterne for Commerce-nettprat med Omnikanal for Customer Service og Commerce-nettprat med Power Virtual Agents-nettpratmoduler i Microsoft Dynamics 365 Commerce.

## <a name="proactive-chat-properties"></a>Proaktive nettprategenskaper

De proaktive nettprategenskapene ligger i egenskapsruten i Commerce-nettprat med Omnikanal for Customer Service og Commerce-nettprat med Power Virtual Agents-moduler i Commerce-områdebygger.

> [!NOTE]
> Alle de proaktive nettprategenskapene som er oppført her, er tomme som standard. Vi anbefaler at du lærer mer om disse egenskapene og bare definerer dem etter behov. Denne fremgangsmåten vil bidra til å redusere feilaktig proaktiv nettprat fra å bli utløst.

### <a name="proactive-chat"></a>Proaktiv nettprat

| Egendefinert navn | Beskrivelse | Standardverdi |
|---------------|-------------|---------------|
| Aktivert | En proaktiv aktivitet med kunder basert på ulike utløsere. | Deaktivert |
| Nettprathilsener | Hilsningsmeldingen som brukes når en proaktiv nettprat er utløst. | Blank |

### <a name="wait-time-proactive-chat"></a>Ventetid (proaktiv nettprat)

| Egendefinert navn | Beskrivelse |
|---------------|-------------|
| Ventetid (sek) | Tiden (i sekunder) som områdebrukere bruker på en områdeside før det utløses en proaktiv nettprat. |
| Nettprathilsener | Hilsningsmeldingen som brukes når en proaktiv nettprat er utløst. |

### <a name="number-of-page-visits-proactive-chat"></a>Antall sidebesøk (proaktiv nettprat)

| Egendefinert navn | Beskrivelse |
|---------------|-------------|
| Antall sidebesøk | Antall sidebesøk før en proaktiv nettprat utløses. Stedsbrukere må først godta ledeteksten i personvernerklæringen for informasjonskapsler. |
| Nettprathilsener | Hilsningsmeldingen som brukes når en proaktiv nettprat er utløst. |

### <a name="specific-pages-proactive-chat"></a>Bestemte sider (Proaktiv nettprat)

| Egendefinert navn | Beskrivelse |
|---------------|-------------|
| Side(r) | En liste over sidene som utløser en proaktiv nettprat når de blir besøkt. |
| Nettprathilsener | Hilsningsmeldingen som brukes når en proaktiv nettprat er utløst. |

### <a name="from-specific-pages-proactive-chat"></a>Fra bestemte sider (Proaktiv nettprat)

| Egendefinert navn | Beskrivelse |
|---------------|-------------|
| Side(r) | En liste over sidene som utløser en proaktiv nettprat når brukere navigerer bort fra dem. |
| Nettprathilsener | Hilsningsmeldingen som brukes når en proaktiv nettprat er utløst. |

### <a name="specific-countryregion-proactive-chat"></a>Bestemt land/område (proaktiv nettprat)

| Egendefinert navn | Beskrivelse |
|---------------|-------------|
| Landkode | Brukere som besøker fra bestemte land eller regioner, vil utløse en proaktiv nettprat. Land-/regionkoder må ha to bokstaver med stor forbokstav (for eksempel **US**). |
| Nettprathilsener | Hilsningsmeldingen som brukes når en proaktiv nettprat er utløst. |

### <a name="date-range-proactive-chat"></a>Datoområde (proaktiv nettprat)

| Egendefinert navn | Beskrivelse |
|---------------|-------------|
| Startdato (dd/mm/ååå) | Datoen som en proaktiv nettprat vil bli utløst etter. |
| Sluttdato (dd/mm/ååå) | Gjeldende dato eller datoen før en proaktiv nettprat vil bli utløst. |
| Nettprathilsener | Hilsningsmeldingen som brukes når en proaktiv nettprat er utløst. |

### <a name="total-amount-in-cart-proactive-chat"></a>Totalbeløp i handlekurv (proaktiv nettprat)

| Egendefinert navn | Beskrivelse |
|---------------|-------------|
| Minimum | Minimumsbeløpet (inklusiv) i handlekurven som vil utløse en proaktiv nettprat når brukere går til handlekurvsiden. |
| Maksimum | Maksimumsbeløpet (inklusiv) i handlekurven som vil utløse en proaktiv nettprat når brukere går til handlekurvsiden. |
|Nettprathilsener | Hilsningsmeldingen som brukes når en proaktiv nettprat er utløst. |

### <a name="total-number-of-items-in-cart-proactive-chat"></a>Totalt antall varer i handlekurven (proaktiv nettprat)

| Egendefinert navn | Beskrivelse |
|---------------|-------------|
| Minimum | Minimumsantallet elementer (inklusiv) i handlekurven som vil utløse en proaktiv nettprat når brukere går til handlekurvsiden. |
| Maksimum | Maksimum elementer (inklusiv) i handlekurven som vil utløse en proaktiv nettprat når brukere går til handlekurvsiden. |
| Nettprathilsener | Hilsningsmeldingen som brukes når en proaktiv nettprat er utløst. |

### <a name="specific-products-in-cart-proactive-chat"></a>Bestemte produkter i handlekurv (proaktiv nettprat)

| Egendefinert navn | Beskrivelse |
|---------------|-------------|
| Produkt(er) ID/SKU | En liste over IDer/SKUer-produktnumrene som vil utløse en proaktiv nettprat når brukere besøker handlekurvsiden. |
| Nettprathilsener | Hilsningsmeldingen som brukes når en proaktiv nettprat er utløst. |

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over Commerce-nettpratfunksjoner](commerce-chat-overview.md)

[Commerce-nettprat med Omnikanal for Customer Service-modul](commerce-chat-module.md)

[Commerce-nettprat med Power Virtual Agents-modul](chat-module-pva.md)
