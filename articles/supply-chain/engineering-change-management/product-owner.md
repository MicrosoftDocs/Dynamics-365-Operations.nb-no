---
title: Produkteiere
description: Denne artikkelen inneholder informasjon om produkteiere. En produkteier er en gruppe brukere som har ansvaret for bestemte produkter. Bare medlemmer av gruppen kan frigi disse produktene. Produkteieren kan også brukes i godkjenningsarbeidsflyten.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5e09fdbbe14aa5a5ffbc5f07ae90b5d307a9e155
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907529"
---
# <a name="product-owners"></a>Produkteiere

[!include [banner](../includes/banner.md)]

Produkteieren er en gruppe brukere som har ansvaret for bestemte produkter. Når en produkteiergruppe tilordnes til et produkt, kan bare medlemmene av denne gruppen frigi produktet. Produkteieren kan også brukes i godkjenningsarbeidsflyten i behandling av teknisk endring.

Produkteiere er globale innstillinger. De er derfor tilgjengelige for alle juridiske enheter.

## <a name="create-a-product-owner-group"></a>Opprett en produkteiergruppe

Følg denne fremgangsmåten for å opprette en produkteiergruppe og legge til medlemmer i den:

1. Gå til **Behandling av teknisk endring \> Oppsett \> Produkteiere**.
2. Velg **Ny** i handlingsruten.
3. I **Produkteier**-feltet angir du et navn på gruppen.
4. I **Navn**-feltet skriver du inn en beskrivelse av gruppen.
5. På hurtigfanen **Medlemmer** legger du til arbeiderne som skal være medlemmer av gruppen.

## <a name="assign-a-product-owner-to-a-product"></a>Tilordne en produkteier til et produkt

Hvis du vil tilordne en produkteier til et produkt, gjør du følgende.

1. Åpne siden **Produktdetaljer** for det relevante produkt eller produktstandarden.
1. I hurtigfanen **Generelt** setter du **Produkteier**-feltet til navnet på den aktuelle produkteiergruppen.

Mens en produkteier er tilordnet et produkt, kan bare medlemmene av produkteiergruppen redigere **Produkteier**-innstillingen.

Produkteieren vises også på siden **Frigitte produkter**.

## <a name="product-owners-and-product-releases"></a>Produkteiere og produktfrigivelser

Bare brukere fra et produkts produkteiergruppe kan frigi produktet. Det er imidlertid et unntak når produktet er en underordnet vare, og det overordnede frigis av eieren av det overordnede. Med andre ord, hvis produktet er en del av stykklisten til et annet produkt, sjekker ikke systemet produkteieren av hver vare i stykklisten. Den kontrollerer bare produkteieren av den overordnede varen.

Produkt X er for eksempel tilordnet til produkteiergruppen *Designkabinetter*. Produkt X er også en del av stykklisten for produkt Y, som er tilordnet til produkteiergruppen *Designhøyttalere*. Hvis en bruker fra produkteiergruppen *Designhøyttalere* frigir produkt Y og stykklisten, blir produkt X frigitt sammen med produkt Y.

## <a name="product-owners-and-approvals"></a>Produkteiere og godkjenninger

Fordi produkteiere vet om bestemte tekniske endringer som vil dra nytte av produktene deres, er det ofte fornuftig å ta dem med som en del av godkjenningsprosessen under behandling av teknisk endring. Du kan implementere denne fremgangsmåten ved å definere produkteierne som deltakerleverandører i arbeidsflytene som brukes til behandling av teknisk endring. Systemet vil deretter tilordne godkjenningsoppgaver i arbeidsflytene, basert på produktene som er i forespørsler og ordrer om teknisk endring. Hvis du vil ha mer informasjon, kan du se [Behandle endringer i tekniske produkter](engineering-change-management.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]