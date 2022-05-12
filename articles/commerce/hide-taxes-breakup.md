---
title: Skjul informasjon om avgiftsoppbrudd i ordresammendrag
description: Dette emnet beskriver hvordan du skjuler informasjon om avgiftsoppbrudd på sidene ordresammendrag i handlekurv, betaling, ordrebekreftelse og bestillingsdetaljer i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 04/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-03-28
ms.openlocfilehash: 9890b5cd92f8c07e6feabb26f4fdd076cb7a02bc
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645221"
---
# <a name="hide-tax-breakup-information-in-order-summaries"></a>Skjul informasjon om avgiftsoppbrudd i ordresammendrag

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emnet beskriver hvordan du skjuler informasjon om avgiftsoppbrudd på sidene ordresammendrag i handlekurv, betaling, ordrebekreftelse og bestillingsdetaljer i Microsoft Dynamics 365 Commerce.

Som standard viser Dynamics 365 Commerce informasjon om avgiftsoppbrudd på sidene ordresammendrag i handlekurv, betaling, ordrebekreftelse og bestillingsdetaljer. I Commerce, versjon 10.0.27-utgaven inneholder Commerce-områdebygger et alternativ som lar deg skjule informasjon om avgiftsoppbrudd i ordresammendrag.

Illustrasjonen nedenfor viser et eksempel på to ordresammendrag. Den første viser informasjon om avgiftsoppbrudd, og den andre skjuler den.

![Eksempler på handlekurver der informasjon om avgiftsoppbrudd vises og skjules.](media/prices-include-sales-tax-e-Commerce.png)

> [!NOTE]
> - Alternativet for å skjule informasjon om mavgiftsoppbrudd i ordresammendrag er bare tilgjengelig når alternativet **Priser inkluderer merverdiavgift** for netthandelskanalen er angitt til **Ja** i Commerce Headquarters under **Retail og Commerce \> Kanaler \> Butikker \> Alle butikker**. 
> - Som standard aktiveres alternativet **Vis avgiftsoppbrudd i ordresammendrag** i områdebyggeren.

## <a name="hide-tax-breakup-information-in-order-summaries"></a>Skjul informasjon om avgiftsoppbrudd i ordresammendrag

For å skjule informasjon om avgiftsoppbrudd i ordresammendrag følger du denne fremgangsmåten.

1. Gå til området du vil oppdatere, i Commerce-områdebygger.
1. Gå til **Områdeinnstillinger \> Tillegg**.
1. Fjern merket for **Vis avgiftsinnbrudd i ordresammendrag**.

Hvis du vil vise informasjon om avgiftsoppbrudd i ordresammendrag, merker du av for **Vis avgiftsoppbrudd for ordresammendrag**.  

Illustrasjonen nedenfor viser avmerkingsboksen **Vis avgiftsoppbrudd for ordresammendrag** merket og valgt i områdebyggeren.

![Vis avgiftsoppbrudd i ordresammendrag i områdebyggeren.](media/prices-include-sales-tax-e-Commerce-site-settings.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over merverdiavgift](/finance/general-ledger/indirect-taxes-overview)

[Konfigurere merverdiavgift for elektroniske ordrer](sales-tax-config.md)

[Feilsøk: Avgifter på elektroniske ordrer beregnes feil](troubleshoot/tax-miscalculated-online-order.md)
