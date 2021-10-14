---
title: Lagerparametere for bølgebehandling
description: Dette emnet beskriver hvordan du setter opp lagerparametere for bølgebehandling. Du kan bruke bølgebehandling til å gruppere plukkarbeidet for flere arbeidsordrer til en enkelt bølge.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: cd7961ae8f4237bcee7ae4c53365d24ab03c5aa9
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572224"
---
# <a name="warehouse-parameters-for-wave-processing"></a>Lagerparametere for bølgebehandling

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du setter opp lagerparametere for bølgebehandling. Du kan bruke bølgebehandling til å gruppere plukkarbeidet for flere arbeidsordrer til en enkelt bølge.

Hvis du vil bruke bølgebehandling, angir du følgende på siden **Lagerstyringsparametere**:

- Om du kan behandle bølger ved hjelp av en satsvis jobb.
- Om du samler inn informasjon i en loggfil når bølger behandles.

## <a name="set-up-warehouse-management-parameters-for-wave-processing"></a>Konfigurere lagerstyringsparametere for bølgebehandling

Hvis du vil konfigurere lagerstyringparametere for bølgebehandling, gjør du følgende:

1. Gå til **Lagerstyring** \> **Oppsett** \> **Lagerstyringsparametere**.

1. Foreta følgende innstillinger på hurtigfanen **Bølgebehandling**:

    - **Satsvis gruppe for bølgebehandling** – Velg den satsvise gruppen som skal brukes når du behandler bølger ved hjelp av satsvise jobber. Den satsvise gruppen angir serveren den satsvise jobber kjøres på.
    - **Behandle bølger satsvis** – Velg om du vil at bølger skal behandles automatisk av en satsvis jobb. Du må sette dette til *Ja* for å bruke parallell behandling. Du definerer den satsvise jobben på **Behandle bølger**-siden. (Se også merknaden nederst i denne listen.)
    - **Opprett bølgefremdriftslogg** – Velg om systemet skal generere en loggpost hver gang tildelingen for en vare og dens dimensjoner begynner og slutter. Du bør bare aktivere denne loggen når du trenger den, for eksempel i den innledende testingen eller i forbindelse med feilsøking. For mer informasjon, se [Bølgetildeling](wave-allocation-method.md).
    - **Opprett historikklogg for bølgebehandling** – Velg om du automatisk vil lagre informasjon om en bølge i en loggfil etter at bølgen er behandlet, inkludert under parallell behandling av uavsluttede tildelinger. Vanligvis bør du bare aktivere dette under feilsøking fordi det legger til ekstra administrasjonskostnader. Hvis du vil vise loggen, kan du gå til **Lagerstyring \> Utgående bølger \> Historikklogg for bølgebehandling**. Hvis du vil ha mer informasjon kan du se [Bølgeoppretting og -behandling](wave-processing.md).
    - **Opprett historikklogg for containerbruk** – Velg om du automatisk vil lagre informasjon om containerisering for en bølge i en loggfil etter at bølgen er behandlet. Du kan vise loggen ved å gå til **Lagerstyring \> Pakking og containerbruk \> Containerbruklogg**.
    - **Vent på lås (ms)** – Angi tiden, i millisekunder, som et tildelingstrinn skal vente på en systemressurs som er låst av et annet tildelingstrinn. Når denne tiden overskrides, behandles ikke på bølgen, og det vises en feilmelding.

1. På hurtigfanen **Frigi til lager** angir du følgende innstilling:

    - **Feil ved mislykket satsvis jobb** – Velg om det skal genereres en feil når en frigivelse til den satsvise jobben for lager mislykkes. Hvis dette er aktivert, vil mislykkede jobber avsluttes med statusen *Feil*. Hvis dette er deaktivert, vil mislykkede jobber avsluttes med statusen *Avsluttet*.

> [!NOTE]
> I bølgemalen som brukes til å behandle bølgen, kan du angi innstillingene som automatiserer bølgebehandlingen. Hvis du konfigurerer en tidsplan for den satsvise jobben, bør du koordinere tiden med innstillingene for automatisering i bølgemalen. Hvis du vil ha mer informasjon, kan du se [Opprette en bølgemal](wave-templates.md).
>
> Hvis du bruker *Transportstyring* og *Avansert lagerstyring*, kan du angi om du vil konsolidere laster når du behandler en bølge. Dette er for eksempel nyttig når flere små laster kan sendes samtidig. Hvis du vil konsolidere laster når du behandler en bølge, går du til **Laster**-fanen og merker av for **Konsolider laster under bølgebehandling**.</P>

## <a name="set-up-full-or-partial-reservation-for-production-waves"></a>Angi fullstendig eller delvis reservasjon for produksjonsbølger

Når det gjelder salgsordrer og Kanban-bestillinger, må beholdning reserveres før ordren frigis til lageret. Hvis ikke, varer eller tildelingslinjer kan ikke behandles i en Bølge. Produksjonsordrer er imidlertid litt mer fleksible. Når det gjelder produksjonsordrer, kan du angi følgende:

- Tillat at produksjonsordrer frigis til lageret, selv om ikke alle materialer kan reserveres. Hvis du velger dette alternativet, må du gjenta prosessen med frigivelse til lager manuelt når tilleggsmaterialene flere blir tilgjengelige. Dette er for eksempel nyttig hvis du har materialene du trenger for å starte en produksjon, og du kan vente til tilleggsmaterialene bli tilgjengelige.
- Krev at alle materialer reserveres før en ordre kan frigis til lageret.

Hvis du vil kreve fullstendig reservering eller godta delvis reservasjon, gjør du følgende:

1. Gå til **Produksjonskontroll** \> **Oppsett** \> **Parametere for produksjonskontroll**.
1. på **Generelt**-fanen, i feltet **Frigi til lager**, velger du standardinnstillingen.
