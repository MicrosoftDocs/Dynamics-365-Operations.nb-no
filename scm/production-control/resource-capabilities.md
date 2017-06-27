---
title: Ressursfunksjoner
description: "Denne artikkelen inneholder informasjon ressursfunksjoner. En funksjon er muligheten for en operasjonsressurs til å utføre en bestemt aktivitet. Artikkelen forklarer hvordan funksjonene og relaterte konsepter, for eksempel ferdighetsnivå og prioritet, brukes til å velge riktige ressurser for en aktivitet."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WrkCtrCapability, WrkCtrTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 29961
ms.assetid: 30e38233-2a64-4070-911f-8ffd78dd8281
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f6b4ccf4d7f9727819831b07221d859e3c5cdd39
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="resource-capabilities"></a>Ressursfunksjoner

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder informasjon ressursfunksjoner. En funksjon er muligheten for en operasjonsressurs til å utføre en bestemt aktivitet. Artikkelen forklarer hvordan funksjonene og relaterte konsepter, for eksempel ferdighetsnivå og prioritet, brukes til å velge riktige ressurser for en aktivitet.

En funksjon er muligheten for en operasjonsressurs til å utføre en bestemt aktivitet. En operasjonsressurs kan ha flere funksjoner tilordnet, og en funksjon kan tilordnes til mer enn én ressurs. Du kan tilordne funksjoner til ressurser midlertidig ved å definere en startdato og utløpsdato for funksjonstilordningen. Når funksjonen for en ressurs utløper, kan ikke ressursen planlegges for et prosjekt eller en produksjon som krever denne funksjonen. En funksjon som er utløpt, kan fornyes. Du kan slette funksjoner, forutsatt at de ikke er på en ruterelasjon eller på en del av en produksjonsrute for en aktiv produksjonsordre. Vær vanligvis forsiktig når du sletter funksjoner. I stedet bør du vurdere å justere utløpsdatoen for ressursene som har funksjonen. Funksjoner som kan tilordnes til alle typer ressurser: Verktøy, leverandør, maskin, lokasjon, lokaler eller Personale.

## <a name="level"></a>Nivå
Flere ressurser har ofte samme funksjonelle kapasitet, men på forskjellige ferdighetsnivåer (for eksempel styrke, behandlingshastighet eller nøyaktighet). Når du tilordner en funksjon til en ressurs, kan du derfor angi en **nivå** verdi. Nivået er en enkelt numerisk verdi. Hvis du angir at en funksjon er et ressursbehov for en produksjonsrute, kan du også angi en verdi for **Nødvendig minimumsnivå** for denne funksjonen. Planleggingsmotoren velger deretter bare ressurser som har den nødvendige kapasiteten på et nivå som er lik eller overgår minimumsnivået som er angitt i ressursbehovet.

## <a name="priority"></a>Prioritet
Operasjonsressurser som har samme funksjoner, kan tilordnes en prioritet. Hvis flere ressurser har funksjoner som tilfredsstiller kravene til planlegging på det nødvendige nivået, og har ledig kapasitet, kan deretter planleggingsmotoren velge blant disse ressursene. Hvis **Prioritet** er valgt i feltet **Valg av primærressurs** på siden **Planleggingsparametere**, velges ressursen som har høyest prioritet (den laveste numeriske verdien i feltet **Prioritet**) først under planlegging.

## <a name="resource-requirements"></a>Ressursbehov
Når du definerer ressursbehov for en produksjonsrute, kan du angi én eller flere funksjoner som behov. Under produksjonsplanlegging sammenlignes funksjonene som er definert i ressursbehovene på ruteoperasjonen, med funksjonene som er definert for ressursene. Ressurser som har funksjoner som tilfredsstiller kravene velges. Hvis flere ressurser har samme funksjonelle kapasitet, men forskjellige ferdigheter (for eksempel styrke, behandlingshastighet eller nøyaktighet), kan du definere flere funksjoner eller bruke funksjonsnivået for å kvalifisere funksjonen for ressursen. Her er et eksempel:

-   I en rute settes drillingsbehandlingstiden til 10 enheter per time, men selve behovet defineres som Drilling.
-   Du har to drille maskiner, M1 og M2.
-   Drillingsfunksjonen er tilordnet til begge ressurser, M1 maskinen og M2 maskinen.
-   Maskinen M1 kan drille to enheter per time, og maskinen M2 kan drille 11 enheter per time.

Begge maskiner kan velges som planleggingsmotoren, fordi begge tilfredsstiller kravet til grunnleggende funksjonalitet (Drilling), i dette eksemplet. Maskinen M1 kan imidlertid kun drille to enheter per time. Fordi denne satsen er mye mindre enn 10 enheter per time som er angitt i ruten, vil maskinen M1 forårsake produksjonsproblemer hvis den er valgt. Det finnes to måter å løse dette problemet på og sikre at maskinen M2 blir valgt i stedet:

-   Opprett to separate funksjoner: lav hastighet drilling og høy hastighet drilling. Definer lav hastighet drilling som drilling som har en behandlingstid på én til ni enheter per time. Definer høy hastighet drilling som drilling som har en drillingsbehandlingstid på 10 til 19 enheter per time. Tilordne deretter M1 maskinen funksjonen for lav hastighet drilling, og tilordne M2 maskinen funksjonen for rask drilling. Til slutt endre ressursbehovskravet i ruten til rask drilling. Planleggingsmotoren velger deretter den riktige maskinen (M2).
-   Bruk funksjonsnivået til å kvalifisere Drilling funksjonen som tilordnes til drilling maskiner. Angi at M1 maskinen har Drilling funksjonen på nivået 2,0 og at M2 maskinen har Drilling funksjonen på nivået 11,0. Angi deretter at 10,0 er minimumsnivået som kreves for funksjonsbehovet for Drilling på ruten. Planleggingsmotoren fastslår deretter at bare M2 maskinen oppfyller ressursbehovene.

## <a name="competencies-for-human-resources"></a>Kompetanser for Personale
Når du har operasjonsressurser av typen **Personale** som er knyttet til arbeidere i Personale, du kan også dra nytte av kompetansetypene for arbeidere når du definerer hvilke ressurser som kreves for en produksjonsrute. Med andre ord, kan du også angi krav for en bestemte ferdigheter, kurs, sertifikater eller titler. Planleggingsmotoren kan deretter velge ressurser som er knyttet til arbeidere, og valget vil baseres på kompetansetypene for disse arbeiderne. Kompetansetypene defineres i Personale, ikke på siden **Ressursfunksjoner**. Når du definerer ferdigheter, kurs, sertifikater eller titler som ressursbehov, må du bruke Personale-funksjonaliteten og koble hver ressurs av typen **Personale** til en tilhørende arbeider. Hvis du ikke bruker Personale-funksjonaliteten, kan du definere funksjoner på siden **Ressursfunksjoner** som ligner på eller dupliserer kompetansetypene fra Personale. Siden **Ressursfunksjoner** inneholder imidlertid ikke funksjonaliteten som kreves for å opprettholde ferdigheter, kurs, sertifisering eller titler.




