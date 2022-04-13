---
title: Leverandørkode er ikke autorisert for et bestemt produkt og en bestemt dato
description: Når du prøver å autorisere en planlagt bestilling eller legge til en linje i en bestilling, får du en feilmelding som angir at leverandørkoden ikke har autorisasjon for et produkt og en dato.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 917526dfcefb36ce6e59af6f1f5bebc23ee6e53f
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/26/2022
ms.locfileid: "8489063"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a>Leverandørkode er ikke autorisert for et bestemt produkt og en bestemt dato

Feilkode: SYP4881415

## <a name="symptoms"></a>Symptomer

Når du prøver å autorisere en planlagt ordre eller legge til en linje i bestillingen, mottar du følgende feilmelding:

> Leverandørkoden %1 er ikke autorisert for %2 på %3.

## <a name="cause"></a>Årsak

Feilen oppstår fordi feltet **Godkjent leverandørkontrollmetode** er satt til *Bare advarsel* eller *Ikke tillatt* for det angitte produktet, og leverandøren har i øyeblikket ikke tillatelse til å levere dette produktet.

## <a name="resolution"></a>Løsning

Hvis du vil korrigere dette problemet, kan du enten deaktivere leverandørsjekken for det aktuelle produktet eller godkjenne leverandøren.

Følg denne fremgangsmåten for å deaktivere leverandørsjekken for et produkt.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Åpne det relevante produktet.
1. I hurtigfanen **Kjøp** setter du feltet **Godkjent leverandørkontrollmetode** til en annen verdi enn *Bare advarsel* eller *Ikke tillatt*.

Følg denne fremgangsmåten for å godkjenne en leverandør for et produkt.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Åpne det relevante elementet.
1. I handlingsruten i fanen **Kjøp** i gruppen **Godkjent leverandør** velger du **Oppsett**.
1. På listesiden **Godkjent leverandør** legger du til en rad i rutenettet, og angi deretter følgende verdier:

    - **Leverandør** – Velg leverandøren som skal godkjenne for gjeldende produkt.
    - **Ikrafttredelsesdato** – Velg den første datoen som leverandøren er godkjent for.
    - **Utløpsdato** – Velg den siste datoen som leverandøren er godkjent for.

Hvis du vil ha mer informasjon, kan du se [Godkjenne leverandører for spesifikke produkter](../../procurement/tasks/approve-vendors-specific-products.md).
