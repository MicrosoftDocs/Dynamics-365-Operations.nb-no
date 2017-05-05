---
title: Kostnadsanalyse for produksjonsordrer
description: "Denne artikkelen inneholder informasjon om kostnadsanalysen som du kan utføre for fullførte og gjeldende produksjonsordrer. Du kan analysere de estimerte kostnadene og faktiske kostnadene ved hjelp av siden Prisberegning eller rapporten Kostnadsestimater og etterkalkuleringer. Du kan vise informasjon om de estimerte og faktiske kostnadene (og antallene) for hver komponentvare, rutingoperasjon og indirekte kostnad."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-04-11 13 - 25 - 42
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79634
ms.assetid: ded5da04-f787-49f7-b5e5-75c2a2b92930
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f931432f6dc919d448ed690a1deae3d64bebe455
ms.lasthandoff: 03/29/2017


---

# <a name="production-order-cost-analysis"></a>Kostnadsanalyse for produksjonsordrer

Denne artikkelen inneholder informasjon om kostnadsanalysen som du kan utføre for fullførte og gjeldende produksjonsordrer. Du kan analysere de estimerte kostnadene og faktiske kostnadene ved hjelp av siden Prisberegning eller rapporten Kostnadsestimater og etterkalkuleringer. Du kan vise informasjon om de estimerte og faktiske kostnadene (og antallene) for hver komponentvare, rutingoperasjon og indirekte kostnad.

De faktiske kostnadene for en produksjonsordre er basert på det rapporterte forbruket av materialer og rutingoperasjoner. Du kan få tilgang til detaljerte transaksjoner om rapportert forbruk av materialer, rutingoperasjoner og indirekte kostnader for en produksjonsordre på siden **Produksjonspostering**.

## <a name="variance-analysis-for-a-completed-production-order"></a>Avviksanalyse for en fullført produksjonsordre
Avvikene gjenspeiler en sammenligning av de rapporterte produksjonsaktivitetene og beregningen av standardkoster for produksjonsvaren. Avvikene gjenspeiler ikke en sammenligning med produksjonsordrens estimerte kostnader. De rapporterte produksjonsaktivitetene inkluderer materialforbruk og ruteoperasjoner, sammen med tilknyttede indirekte kostnader, og det ferdigmeldte antallet. Følgende fire avvikstyper beregnes:

-   Partistørrelsesavvik
-   Avvik for produksjonsantall
-   Avvik i produksjonspris
-   Erstatningsavvik for produksjon

Diagrammet nedenfor viser de fire avvikene som utgjør differansen mellom en produksjonsordres faktiske kostnader og de beregnede kostnadene i varens kostnadspost når produksjonsordren avsluttes. ![Avvik som tar hensyn til forskjeller i en fullført produksjonsordre](./media/control.jpg) Du kan analysere produksjonsavvikene ved hjelp av **Avvik**-siden eller **Produksjonsavvik**-rapporten. Bruk visningsalternativene til å vise detaljer om avvik etter vare og operasjonsressurs eller etter kostnadsgruppe. Policyen for nedbryting av kostnader i lagerparameterne bestemmer om avvikene spores etter kostgruppe. Du kan også bruke visningsalternativene **enkelt**, **flere** og **totalt** til å vise summerte avvik. Informasjonen om detaljerte avvik kan hkelpe deg med å forstå hva som er kilden til de enkelte avvikene. For å forutsi avvik før du avslutter en produksjonsordre, kan du analysere den detaljerte informasjonen i rapporten **Kostnadsestimater og etterkalkuleringer**.

## <a name="cost-analysis-for-current-production-orders"></a>Kostnadsanalyse for gjeldende produksjonsordrer
Egne rapporter inneholder informasjon om hver transaksjonstype. Bruk disse rapportene til å analysere kostnadene for rapporterte produksjonsaktiviteter. Det vises bare informasjon om gjeldende produksjonsordrer med statusen **Startet** eller** Ferdigmeldt**.

-   **Materialer i prosess **− Denne rapporten viser plukklistetransaksjoner som er rapportert mot gjeldende produksjonsordrer per en angitt transaksjonsdato. Rapporten viser mengden av en komponent som er tatt ut av lageret, og kostprisen for hver transaksjon. Bruk utvalgskriteriene på én enkelt komponentvare. Du kan for eksempel skrive ut informasjon om avgangsantallet mot gjeldende produksjonsordrer. Det utstedte antallet oppdateres ikke med antallet som er ferdigmeldt for den overordnede varen. Det faktiske antallet råvarer i prosess kan derfor være overvurdert.
-   **Arbeid pågår **− Denne rapporten viser rutetransaksjoner (eller jobbtransaksjoner) som er rapportert mot gjeldende produksjonsordrer per en angitt transaksjonsdato. Rapporten viser timer, beløp og antall (både antall korrekte og antall feil) som er rapportert for hver transaksjon. Det inneholder også informasjon som operasjonsnummer, operasjons-ID og operasjonsressurs. I tillegg viser rapporten samlet tid og beløp for alle transaksjoner mot produksjonsordren, samt ferdigmeldt antall.
-   **Indirekte kostnader i prosess **− Denne rapporten viser de indirekte kostnadene som har påløpt mot produksjonsordrer. Disse dataene er basert på rapportert forbruk av rutingoperasjoner og komponenter per en angitt transaksjonsdato. Rapporten viser typen indirekte kostnader (tillegg eller satser), kostarkkoden for den indirekte kostnaden og kostnadsbeløpet for hver transaksjon. Rapporten inneholder ikke informasjon om rutingkort- eller plukklistetransaksjonen som genererte den indirekte kostnaden.
-   **Etterkalkulering av produksjon i arbeid **− Denne rapporten viser det samlede forbruket av materialer, rutingoperasjoner og indirekte kostnader mot produksjonsordrer per en angitt transaksjonsdato.
-   **Ferdigvarer i arbeid **− Denne rapporten viser gjeldende produksjonsordrer og ferdigmeldingstransaksjonene per en angitt transaksjonsdato.


<a name="see-also"></a>Se også
--------

[Vanlige kilder til produksjonsavvik](common-sources-of-production-variances.md)

