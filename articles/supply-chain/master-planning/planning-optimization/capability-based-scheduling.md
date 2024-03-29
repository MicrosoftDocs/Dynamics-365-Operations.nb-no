---
title: Planlegging med ressursvalg basert på kvalifikasjon
description: Denne artikkelen beskriver ressursvalg under ubegrenset kapasitetsplanlegging når du angir kvalifikasjoner som ressursbehov for en operasjon.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd, WrkCtrTable, WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 176f40ad8cd1aa1831bbe50c0ebd91ec0cc3bc89
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739905"
---
# <a name="scheduling-with-resource-selection-based-on-capability"></a>Planlegging med ressursvalg basert på kvalifikasjon

[!include [banner](../../includes/banner.md)]

Ved å angi ressursbehov for en operasjon av en produksjonsrute, definerer du hva som kreves for å utføre denne operasjonen. For eksempel kan en operasjon kreve en bestemt ressurs eller en ressursgruppe, eller en kombinasjon av kompetanse eller kvalifikasjoner. Denne artikkelen beskriver ressursvalg under ubegrenset kapasitetsplanlegging når du angir kvalifikasjoner som ressursbehov for en operasjon.

## <a name="turn-the-capability-based-scheduling-feature-on-or-off"></a>Aktiver eller deaktiver funksjon for kvalifikasjonsbasert kapasitetsplanlegging

For å bruke denne funksjonen må den være aktivert for systemet. Fra og med Supply Chain Management versjon 10.0.29 er funksjonen aktivert som standard. Administratorer kan aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Uendelig kapasitetsplanlegging for Planleggingsoptimalisering* i arbeidsområdet [Funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Hvis du vil ha mer informasjon om denne funksjonen, kan du se [Planlegging med ubegrenset kapasitet](infinite-capacity-planning.md).

## <a name="capability-based-scheduling"></a>Funksjonsbasert planlegging

En kvalifikasjon er muligheten for en operasjonsressurs til å utføre en bestemt aktivitet. Mer enn én kvalifikasjon kan tilordnes til en enkelt operasjonsressurs, og en enkelt kvalifikasjon kan tilordnes til mer enn én ressurs. Funksjoner som kan tilordnes til alle typer ressurser, for eksempel verktøy, leverandører, maskiner, lokasjoner, lokaler eller menneskelige ressurser.

Når du angir kvalifikasjoner som ressursbehov, kan du utsette ressurstildeling til ordrer blir planlagt. I stedet for å tilordne bestemte ressurser eller ressursgrupper til en ruteoperasjon, kan du definere hvilke kvalifikasjoner som kreves for hver ruteoperasjon. Under planleggingen samsvarer deretter systemet nødvendige kvalifikasjoner med kvalifikasjonene som er definert for ressursene. Systemet velger bare ressurser som oppfyller kravene.

Hvis du vil tilordne kvalifikasjoner til en operasjonsressurs, bruker du hurtigfanen **Funksjoner** på siden **Ressurser**. Hvis du vil tilordne ressurser til en kvalifikasjon, bruker du hurtigfanen **Ressurser** på siden **Ressurskvalifikasjoner**. Begge sidene er tilgjengelige under **Produksjonskontroll \> Oppsett \> Ressurser** på navigasjonsruten. Begge hurtigfanene inneholder et rutenett som viser ressurser som er knyttet til en valgt ressurs eller kvalifikasjon. Begge hurtigfanene inneholder også en verktøylinje som du kan bruke til å legge til, fjerne og redigere rader i rutenettet. Rutenettet inneholder følgende kolonner:

- **Ressurs** eller **Funksjon** – Velg ressursen eller kvalifikasjonen som blir tilordnet av raden.
- **Beskrivelse** – Legg inn en kort beskrivelse av ressursen eller kvalifikasjonen.
- **Effektiv** – Angi den første datoen da ressurs- eller kvalifikasjonstilordningen gjelder. Under planlegging vil ikke systemet bruke en ressurs eller kvalifikasjon som har en utløpt kvalifikasjonstilordning, selv om ressursen ellers oppfyller kravene.
- **Utløp** – Angi den siste datoen da ressurs- eller kvalifikasjonstilordningen gjelder. Under planlegging vil ikke systemet bruke en ressurs eller kvalifikasjon som har en utløpt kvalifikasjonstilordning, selv om ressursen ellers oppfyller kravene.
- **Nivå** – Angi kompetansenivået som ressursen må ha for kvalifikasjonen. Hvis du angir verdien **Nødvendig minimumsnivå** for ressurs- eller kvalifikasjonskravet, vil planleggingsmotoren vurdere graden av kompetanse under ressursvalg. Systemet velger bare ressurser som har den nødvendige kvalifikasjonen på et nivå som er lik eller overgår minimumsnivået som er angitt i ressursbehovet.
- **Prioritet** – Dette feltet støttes ennå ikke av Planleggingsoptimalisering. Hvis du imidlertid bruker den avskrevne hovedplanleggingsmotoren, kan du bruke **Prioritet**-feltet i ressurs- eller kvalifikasjonstilordningen til å definere ressursprioriteten. Hvis *Prioritet* deretter velges i feltet **Valg av primærressurs** på siden **Planleggingsparametere**, velger systemet først ressursen som har høyest prioritet (det vil si den laveste numeriske verdien i feltet **Prioritet**) under planlegging.

## <a name="example"></a>Eksempel

Dette eksemplet viser hvordan planleggingsmotoren velger ressurser basert på kvalifikasjon.

En produksjonsrute har fem operasjoner: *10*, *20*, *30*, *40* og *50*. Hver ruteoperasjon krever en ressurs som har ulike kvalifikasjoner. Ruteoperasjon *10* krever for eksempel en ressurs som har kvalifikasjon til å sette sammen en høyttaler (*0050 Høyttalermonter*), og kvalifikasjon til trearbeid (*1010 Trekvalifikasjon*). Ruteoperasjon *50* krever en ressurs som har kvalifikasjon til å pakke et produkt (*0070 Pakkingskvalifikasjon*).

![Kvalifikasjon brukt til planlegging.](media/capability-based-scheduling.png "Kvalifikasjon brukt til planlegging.")

Under planleggingen leter maskinen etter ressurser som oppfyller operasjonskravene. Planleggingsmotoren velger for eksempel ressurs *00101* til å utføre operasjon *10*, fordi denne ressursen er den første ressursen som blir funnet som har begge de nødvendige kvalifikasjonene. Planleggingsmotoren velger ressurs *00301* til å utføre operasjon *50*, fordi denne ressursen er den eneste ressursen som har pakkekvalifikasjonen.

Deretter bør du vurdere hvordan dette eksemplet blir påvirket når det brukes ferdighetsnivåer:

- Operasjon *10* krever et minimum kompetansenivå på *7* for *0059 Montering*-kvalifikasjonen.
- Ressurs *00101* har et kompetansenivå på *5* for *0059 Montering*-kvalifikasjonen.
- Ressurs *00102* har et kompetansenivå på *10* for *0059 Montering*-kvalifikasjonen.

I dette tilfellet, under ubegrenset kapasitetsplanlegging, vil planleggingsmotoren velge ressurs *00102* for å utføre operasjon *10*, fordi denne ressursen, i motsetning til ressurs *00101* har det nødvendige kompetansenivået for kvalifikasjonen.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
