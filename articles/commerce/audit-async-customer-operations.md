---
title: Revisjonssynkronisering av kundeoperasjoner i headquarters
description: Denne artikkelen beskriver hvordan du kan utføre revisjonssynkronisering av kundeoperasjoner i Microsoft Dynamics 365 Commerce headquarters for å rette eventuelle brukerproblemer.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-28
ms.openlocfilehash: c615b0b436e01a1423b5611a72f0056b5b14f8e8
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691091"
---
# <a name="audit-synchronization-of-customer-operations-in-headquarters"></a>Revisjonssynkronisering av kundeoperasjoner i headquarters

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Denne artikkelen beskriver hvordan du kan utføre revisjonssynkronisering av kundeoperasjoner i Microsoft Dynamics 365 Commerce headquarters for å rette eventuelle brukerproblemer.

Når organisasjoner begynner å bruke muligheten til å opprette og redigere kunder asynkront, må områdeadministratorer bruke en måte å vise og feilsøke operasjoner på, basert på brukerforespørsler eller mislykkede behandlingsforsøk. I disse scenariene skal områdeadministratorer kunne kontrollere at kunder kan opprette og redigere operasjoner, og korrigere eventuelle feil ved hjelp av en selvbetjeningsmodell.

## <a name="customer-synchronization-status"></a>Kundesynkroniseringsstatus

Når du velger asynkron modus for kundebehandling og den tilsvarende funksjonen, må Commerce headquarters-administratorer opprette og planlegge en gjentakende satsvis jobb for **P-jobben**, jobben **Synkroniser kunder og forretningspartnere fra asynkront modus** og jobben **1010**, slik at alle asynkrone kunder konverteres til synkrone kunder i Commerce headquarters. Synkronisering av kundestyringsoperasjoner skjer hver gang disse jobbene kjøres. Hvis du vil ha mer informasjon, kan du se [Asynkron kundeopprettingsmodus](async-customer-mode.md).

Som bedriftseier kan du utføre følgende operasjoner:

- Vis alle opprette-/redigeringsoperasjoner for områdebrukere. Detaljene inkluderer status og tidsangivelse.
- Filtrer operasjoner ved å bruke et av kundetabellfeltene og -verdiene til å begrense revisjonsloggen.
- Vis korte beskrivelser av endringer sammen med statusdetaljene for å forstå operasjoner på et høyt nivå.
- For feil kan du redigere og korrigere problematiske felt, og deretter lagre og synkronisere bestemte kundeoperasjoner.

### <a name="elements-on-the-customer-synchronization-status-page"></a>Elementer på statussiden for kundesynkronisering

Hvis du vil vise en liste over alle synkroniseringsoperasjoner, går du til Commerce headquarters og **Commerce and Retail \> Kunder \> Kundesynkroniseringsstatus**. Illustrasjonen nedenfor viser et eksempel på siden **Kundesynkroniseringsstatus**.

![Kundesynkroniseringsstatusside i Commerce Headquarters.](media/D365-Commerce-Customer-Mgmt-Audi-Async-Operations.png)

Som standard inkluderer listen over kundesynkroniseringsoperasjoner på venstre side av siden for **Kundesynkroniseringsstatus** følgende kolonner:

- Kanalnavn
- Kundekonto
- Asynkron kundekonto
- Operasjonstidsstempel
- Kundesynkroniseringsstatus

Øverst til høyre på siden vises kundekontodetaljer, for eksempel verdiene **Kundekonto**, **Retail Async-operasjon**, **Kundesynkroniseringsstatus** og **Siste kjente feil**.

Delen **Endringsbeskrivelse** inneholder en beskrivelse av typen kundestyringsoperasjon som kjørte (for eksempel kundeopprettelse, kontooppdatering eller synkroniseringsfeil med detaljer).

**Kundeattributter**-delen inneholder et rutenett som viser alle kundeattributter, sammen med gamle og nye verdier. Du kan redigere denne delen hvis du vil endre kundeattributtverdiene for å korrigere feil, og deretter synkronisere på nytt.
