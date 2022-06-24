---
title: Koble til et eksperiment og redigere variasjoner
description: Denne artikkelen beskriver hvordan du kobler et eksperiment i en tredjepartstjeneste til Dynamics 365 Commerce, og hvordan du redigerer variasjoner for eksperimentet.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: dcdbd61976402ddd719ece184a86692fbc7c628d
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942828"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Koble til et eksperiment og redigere variasjoner

Denne artikkelen beskriver hvordan du kobler til eksperimentet i Commerce og gjør endringer i variasjonene slik at de justeres med hypotesen. 

Diagrammet nedenfor viser alle trinnene for å konfigurere og kjøre et eksperiment på et nettsted for e-handel i Dynamics 365 Commerce. Flere trinn er beskrevet i separate artikler.

[ ![Brukerreise for eksperimentering – koble til og redigere.](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Når du har [konfigurert eksperimentet](experimentation-setup.md) i en tredjepartstjeneste, kobler du eksperimentet til i Dynamics 365 Commerce og redigerer eksperimentvariasjonene.

## <a name="connect-your-experiment"></a>Koble til eksperimentet
Hvis du vil koble til eksperimentet, starter du veiviser **Koble til eksperiment**. Veiviseren leder deg gjennom trinnene som kreves for å koble til eksperimentet. Når du fullfører veiviseren, er eksperimentet ditt tilkoblet, og variasjonene er opprettet og klare til redigering.

Følg denne fremgangsmåten for å komme i gang med å koble til eksperimentet i Commerce-områdebyggeren:

1. Hvis du vil starte veiviseren **Koble til eksperiment**, velger du **Eksperimenter** i den venstre navigasjonsruten, og deretter velger du **Koble til**. Alternativt kan du få tilgang til veiviseren fra en side eller et fragmentredigeringsprogram ved å redigere den og velge **Koble til eksperiment** på kommandolinjen.

    > [!NOTE]
    > - En side kan bare kobles til ett eksperiment om gangen. Hvis du vil koble en side til et annet eksperiment, må du først slette eksperimentet som siden for øyeblikket er koblet til.
    > - Du kan bare eksperimentere på sider med et egendefinert oppsett. Hvis siden har et forhåndsdefinert oppsett, må du konvertere det til et egendefinert oppsett først. Du kan gjøre dette ved å gå til siden og velge **Konverter til egendefinert oppsett** på kommandolinjen. Hvis du vil ha mer informasjon om oppsett, kan du se [Forhåndsinnstilte og egendefinerte oppsett](templates-layouts-overview.md#preset-and-custom-layouts). 

1. Hvis du kobler deg til et eksperiment **Eksperimenter**-fanen i den venstre navigasjonsruten, velger du eksperimentnavnet fra listen som vises.
1. Velg siden eller fragmentet du vil kjøre eksperimentet på.
1. Velg **Generer varianter og avslutt veiviser** i det siste trinnet i veiviseren. Variasjoner blir opprettet for eksperimentet. 

> [!NOTE]
> Hvis du vil planlegge når eksperimentet publiseres til ditt eget område, må du passe på at innholdet du vil knytte til eksperimentet, er tilgjengelig i en publiseringsgruppe *før* du kobler til eksperimentet. Hvis du vil ha mer informasjon om publiseringsgrupper, kan du se [Arbeide med publiseringsgrupper](publish-groups.md).

## <a name="edit-your-variations"></a>Redigere variasjonene

Når du avslutter veiviseren **Koble til eksperiment**, blir det opprettet variasjoner for deg. Følg trinnene nedenfor for å redigere variasjonene slik at de gjenspeiler valgene du må kontrollere i hypotesen for eksperimentet.

1. I redigeringsvisning bruker du rullegardinmenyen for variasjoner nedenfor kommandolinjen til å redigere hver variant basert på den opprinnelige hypotesen. Du kan også opprette en kontroll eller basisvariasjon ved å la én av variasjonene være uendret.
1. Velg modulen det skal eksperimenteres på, Velg ellipsen (...), og velg deretter **Legg til eksperiment**.

> [!NOTE]
> Du kan også vurdere å opprette en kontroll eller basisvariasjon ved å la én av variasjonene være uendret.

## <a name="previous-step"></a>Forrige trinn
[Definer et eksperiment](experimentation-setup.md) 


## <a name="next-step"></a>Neste trinn
[Forhåndsvise og publisere et eksperiment](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
