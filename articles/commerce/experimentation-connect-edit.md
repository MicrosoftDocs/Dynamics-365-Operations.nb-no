---
title: Koble til et eksperiment og redigere variasjoner
description: Dette emnet beskriver hvordan du kobler et eksperiment i en tredjepartstjeneste til Dynamics 365 Commerce, og hvordan du redigerer variasjoner for eksperimentet.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2a33897d01dd98d446c2fb49e417abd9db9f403a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010030"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Koble til et eksperiment og redigere variasjoner

Dette emnet beskriver hvordan du kobler til eksperimentet i Commerce og gjør endringer i variasjonene slik at de justeres med hypotesen. 

Diagrammet nedenfor viser alle trinnene for å konfigurere og kjøre et eksperiment på et nettsted for e-handel i Dynamics 365 Commerce. Flere trinn er beskrevet i separate emner.

[ ![Brukerreise for eksperimentering – koble til og redigere](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Når du har [konfigurert eksperimentet](experimentation-setup.md) i en tredjepartstjeneste, kobler du eksperimentet til i Dynamics 365 Commerce og redigerer eksperimentvariasjonene.

## <a name="planning-considerations"></a>Planleggingshensyn

Før du kobler til eksperimentet i Commerce, må du ta noen beslutninger som påvirker hvordan innholdet administreres i Commerce.

### <a name="determine-the-scope-of-your-experiment"></a>Bestemme omfanget av eksperimentet ditt
Når du kobler til et eksperiment, blir du bedt om å definere omfanget av eksperimentet. Eksperimenter er definert som omfanget **delvis** eller **hele**
- Velg **delvis** hvis du vil utføre et eksperiment på en bestemt del av en side. Hvis du velger dette alternativet, må du identifisere hvilke moduler som er inkludert i eksperimentet. Endringer som gjøres i deler av standardsiden eller -fragmentet som ikke er relatert til eksperimentet, synkroniseres automatisk på tvers av variasjoner.
- Velg **hele** hvis du vil utføre et eksperiment på en hel side eller et helt fragment. Det opprettes separate kopier av standardsiden eller -fragmentet. Du trenger ikke velge hvilke moduler som skal tas med i eksperimentet, fordi hele redigeringsflaten kan endres. Du kan legge til, slette og ordne modulene på nytt etter behov. Hvis det imidlertid gjøres endringer i standardsiden eller -fragmentet som eksperimentet er tilknyttet, må disse endringene synkroniseres manuelt på tvers av alle variasjoner.

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> Hvis du knytter eksperimentet til en side som bruker et oppsett, kan du bare angi omfanget **hele** for eksperimentet.

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a>Bestem om du vil planlegge når eksperimentet publiseres
Hvis du vil planlegge når eksperimentet publiseres til ditt eget område, må du passe på at innholdet du vil knytte til eksperimentet, er tilgjengelig i en publiseringsgruppe *før* du kobler til eksperimentet. 

Hvis du vil ha mer informasjon om publiseringsgrupper, kan du se [Arbeide med publiseringsgrupper](publish-groups.md).


## <a name="connect-your-experiment"></a>Koble til eksperimentet
Hvis du vil koble til eksperimentet, starter du veiviser **Koble til eksperiment**. Veiviseren leder deg gjennom trinnene som kreves for å koble til eksperimentet. Når du fullfører veiviseren, er eksperimentet ditt tilkoblet, og variasjonene er opprettet og klare til redigering.

Følg denne fremgangsmåten for å komme i gang med å koble til eksperimentet i Commerce-områdebyggeren:

1. Hvis du vil starte veiviseren **Koble til eksperiment**, velger du **Eksperimenter** i den venstre navigasjonsruten, og deretter velger du **Koble til**. Alternativt kan du få tilgang til veiviseren fra en side eller et fragmentredigeringsprogram ved å redigere den og velge **Koble til eksperiment** på kommandolinjen.

    > [!NOTE]
    > En side kan bare kobles til ett eksperiment om gangen. Hvis du vil koble en side til et annet eksperiment, må du først slette eksperimentet som siden for øyeblikket er koblet til.

1. Velg siden eller fragmentet du vil kjøre eksperimentet på.
1. Angi eksperimentomfanget til **delvis** eller **hele**, basert på valget ditt i delen [Bestemme omfanget av eksperimentet ditt](#determine-the-scope-of-your-experiment) ovenfor.
    > [!NOTE]
    > Funksjonsflaggene for **Eksperimenter på sider eller fragmenter** må være aktivert hvis du vil eksperimentere på en hel side eller et helt fragment. Hvis du vil ha mer informasjon, kan du se emnet [Eksperimentering i Dynamics 365 Commerce](experimentation-overview.md).
    
1. Velg **Generer varianter og avslutt veiviser** i det siste trinnet i veiviseren. Variasjoner blir opprettet for eksperimentet. 

## <a name="edit-your-variations"></a>Redigere variasjonene
Når du avslutter veiviseren, blir det opprettet variasjoner for deg. 

Deretter skal du redigere variasjonene slik at de gjenspeiler valgene du må kontrollere i hypotesen for eksperimentet. Velg én av følgende fremgangsmåter som tilsvarer omfanget du velger for eksperimentet, i [Bestemme omfanget av eksperimentet ditt](#determine-the-scope-of-your-experiment) ovenfor.

### <a name="edit-variations-for-experiments-with-partial-scope"></a>Redigere variasjoner for eksperiment med omfanget delvis
Følg disse trinnene hvis du har definert omfanget for eksperimentet som **delvis** i veiviseren **Koble til eksperiment**.

1. I redigeringsvisning bruker du rullegardinmenyen for variasjoner nedenfor kommandolinjen til å redigere hver variant basert på den opprinnelige hypotesen. Du kan også opprette en kontroll eller basisvariasjon ved å la én av variasjonene være uendret.
1. Velg modulen det skal eksperimenteres på, Velg ellipsen (...), og velg deretter **Legg til eksperiment**.

### <a name="edit-variations-for-experiments-with-entire-scope"></a>Redigere variasjoner for eksperiment med omfanget hele
Hvis du har definert omfanget av eksperimentet som **hele** i veiviseren **Koble til eksperiment**, kan du i redigeringsvisning bruke rullegardinmenyen for variasjoner under kommandolinjen til å redigere hver variant basert på den opprinnelige hypotesen. 

> [!NOTE]
> I begge tilfeller kan du også opprette en kontroll eller basisvariasjon ved å la én av variasjonene være uendret.

## <a name="previous-step"></a>Forrige trinn
[Definer et eksperiment](experimentation-setup.md) 


## <a name="next-step"></a>Neste trinn
[Forhåndsvise og publisere et eksperiment](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]