---
title: Rabattbehandlingsparametere
description: Dette emnet beskriver siden Rabattbehandlingsparametere. Denne siden inneholder innstillinger som påvirker postering, statusoppdateringer, nummerserier og annen virkemåte.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0665ce41233308c814a514fccf3b73e20de64098
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576694"
---
# <a name="rebate-management-parameters"></a>Rabattbehandlingsparametere

[!include [banner](../includes/banner.md)]

Siden **Rabattbehandlingsparametere** brukes til å definere innstillinger som gjelder i hele **Rabattbehandling**-modulen. Disse innstillingene påvirker postering, statusoppdateringer, nummerserier og annen virkemåte. Oppsettet på denne siden deles på tvers av juridiske enheter og kan endres av brukere som har riktige sikkerhetstillatelser.

Du åpner siden **Rabattbehandlingsparametere** ved å gå til **Rabattbehandling \> Oppsett \> Rabattbehandlingsparametere**. Deretter angir du feltene som beskrevet i følgende underdeler.

## <a name="rebate-management-tab"></a>Rabattbehandling-fanen

Følgende tabell beskriver feltene som er tilgjengelige på fanen **Rabattbehandling** på siden **Rabattbehandlingsparametere**.

| Felt | beskrivelse |
|---|---|
| Standardstatus | Velg standardstatus for alle nye avtaler. Hvis du vil definere settet med statusverdier som kan velges, kan du bruke [siden **Rabattstatuser**](rebate-statuses.md). |
| Behandle etter dimensjon | Velg om avsetnings-, rabatt- og avskrivingstransaksjoner skal behandles etter finansdimensjon. Når dette alternativet er aktivert, bruker systemet finansdimensjoner fra kildetransaksjonene i måltransaksjonene. |
| Kontroller om tidligere postert | <p>Velg systemvirkemåten hvis uposterte rabattransaksjoner behandles mer enn én gang for samme periode:</p><ul><li>**Advarsel** – Systemet tillater at brukere overstyrer de opprinnelige transaksjonslinjene, men det vises en advarsel.</li><li>**Feil** – Systemet hindrer brukere i å overstyre de opprinnelige transaksjonslinjene, og det vises en feilmelding. |
| Poster journaler automatisk | Velg om systemet automatisk skal postere foreslåtte journaler. Disse journalene inkluderer daglige journaler som brukes til avsetning og kundefradrag, og også fakturajournaler for leverandøravgifter. |
| Poster fritekstfakturaer automatisk | Velg om systemet automatisk skal postere fritekstfakturaer. Dette alternativet gjelder bare fritekstfakturaer der betalingstypen er angitt til *Kundefradrag for avgiftsfaktura*. |
| Ordrereferanse for rabattvare | Velg rabattreferansen som skal brukes på salgsordrer og bestillinger som genereres fra rabattprosessen (*Ingen*, *Rabattbehandlingsavtale*, *Rabattbehandlingsnummer*, *Rabattransaksjonsnummer* eller *Dokumentmerknader*). |
| Bruk kravprosess | <p>Sett dette alternativet til *Ja* for å bruke en kravprosess. På denne måten kan du merke transaksjoner som Rabattbehandling oppretter, som enten gjort krav på eller ikke er gjort krav på, og deretter bare postere de innkrevde transaksjonene.</p><p>Du kan for eksempel beregne rabatter for en måned med transaksjoner, men kunden har to dager det ikke er gjort krav på. I dette tilfellet opprettes transaksjonene det ikke er gjort krav på, på nytt neste gang du kjører *Behandle*-funksjonen for neste periode.</p><p>Hvis du setter dette alternativet til *Nei*, posteres alle kravtransaksjoner.</p> |
| Inkluder ordretypejournal | For avtaler eller avtalelinjer der transaksjonstypen er satt til *Ordre*, kontrollerer dette alternativet om en salgsordre av *Journal*-typen skal inkluderes. Den gir fleksibilitet hvis disse ordretypene brukes i scenarier der en rabatt ikke skal gjelde ennå. |

## <a name="number-sequences-tab"></a>Fanen Nummerserier

Bruk fanen **Nummerserier** på siden **Rabattbehandlingsparametere** til å tilordne nummerseriekoder til de ulike nummerseriene som Rabattbehandling bruker. I tabellen nedenfor beskrives formålet med hver av disse nummerseriene. Hvis du vil ha mer informasjon om nummerserier, kan du se [Oversikt over nummerserier](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md) og relaterte emner.

| Referanse | beskrivelse |
|---|---|
| Rabattbehandlingsavtale | Nummerserien tilordner en unik nøkkelverdi til hver rabattavtale. Denne nøkkelen brukes når det opprettes avtaler. |
| Rabattbehandlingsnummer | Nummerserien tilordner en unik nøkkelverdi til hver rabatt. Denne nøkkelen brukes til å identifisere rabattrelasjoner. |
| Rabattransaksjonsnummer | Nummerserien tilordner en unik nøkkelverdi til hver rabattransaksjon. Denne nøkkelen brukes til å identifisere rabattransaksjoner. |
| Mva-faktura | Nummerserien tilordner en unik nøkkelverdi til hver rabattfaktura. Denne nøkkelen brukes når rabattjournaler posteres automatisk. |

## <a name="feature-visibility-tab"></a>Fanen Funksjonssynlighet

Rabattbehandling tilfører funksjonalitet (felt og funksjoner) til flere ofte brukte sider i Microsoft Dynamics 365 Supply Chain Management. Disse sidene omfatter sider som er relatert til salgsordrer og salgsavtaler. Hvis du bruker Rabattbehandling, må du gjøre disse funksjonene synlige overalt før du kan dra nytte av dem. Hvis du ikke bruker Rabattbehandling, kan du skjule funksjonene slik at de holdes utenfor.

I fanen **Funksjonssynlighet** på siden **Rabattbehandlingsparametere** setter du alternativet **Aktiver** til *Ja* for å gjøre funksjonene for Rabattbehandling synlige der de er tilgjengelige. Sett det til *Nei* for å skjule funksjonene på vanlige sider utenfor modulen **Rabattbehandling**. Selv om alternativet er angitt til *Nei*, vil imidlertid selve modulen, inkludert siden **Rabattbehandlingsparametere**, være tilgjengelig for brukere som har de riktige tillatelsene til å få tilgang til den.
