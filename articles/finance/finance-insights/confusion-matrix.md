---
title: Resultat av maskinlæringsmodeller (forhåndsversjon)
description: Dette emnet beskriver forvirringsmatriser, klassifiseringsproblemer og nøyaktighet i modeller for maskinlæring (ML). Hensikten er å forbedre forståelsen din av nøyaktighet i ML-prediksjonsresultater.
author: ShivamPandey-msft
ms.date: 06/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-14
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: a9642bd21ffc0770be61677220e0e72986586047
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6028209"
---
# <a name="results-of-machine-learning-models-preview"></a>Resultat av maskinlæringsmodeller (forhåndsversjon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet beskriver forvirringsmatriser, klassifiseringsproblemer og nøyaktighet i modeller for maskinlæring (ML). Hensikten er å forbedre forståelsen din av nøyaktighet i ML-prediksjonsresultater. Målgruppen omfatter teknikere, analytikere og ledere som ønsker å utvikle kunnskapen og ferdighetene innenfor datavitenskap.

## <a name="confusion-matrix"></a>Forvirringsmatrise
Etter at et overvåket ML-problem er opplært basert på et sett med historiske data, testes det ved hjelp av data som holdes tilbake fra opplæringsprosessen. På denne måten kan du sammenligne prediksjonene fra den opplærte modellen med de faktiske verdiene. Forvirringsmatrisen gir en metode for å evaluere hvor vellykket et klassifiseringsproblem er, og hvor det gjør feil (det vil si hvor det blir «forvirret»).

La oss si at målet er å forutsi om et kjæledyr er en hund eller katt, basert på noen fysiske attributter og atferdsattributter. Hvis du har et testdatasett som inneholder 30 hunder og 20 katter, kan det hende at forvirringsmatrisen ligner på følgende illustrasjon.

![Eksempel på artsprediksjon](media/species-prediction-matrix.png)

Tallene i de grønne cellene representerer riktige prediksjoner. Som du kan se, forutsier modellen en høyere prosent av de faktiske kattene riktig. Den generelle nøyaktigheten til modellen er enkel å beregne. I dette tilfellet er den 42 ÷ 50 eller 0,84.

### <a name="multi-class-classifiers-in-a-confusion-matrix"></a>Klassifiserere med flere klasser i en forvirringsmatrise

De fleste diskusjoner om forvirringsmatrisen fokuserer på binære klassifiserere, som i det foregående eksemplet. Dette tilfellet er et spesialtilfelle der andre måledata kan vurderes, for eksempel følsomhet og tilbakekalling.

Nå skal vi vurdere et klassifiseringsproblem for et finansscenario med tre tilstander. Modellen forutsier om en kundefaktura kommer til å bli betalt til planlagt tid, for sent eller svært sent. La oss si at av 100 testfakturaer blir 50 betalt til planlagt tid, 35 betalt for sent og 15 betalt svært sent. I dette tilfellet kan en modell produsere en forvirringsmatrise som ligner på den følgende illustrasjonen.

![Modell 1](media/payment-prediction-matrix.png)]

En forvirringsmatrise gir betydelig mer informasjon enn en enkel måleverdi for nøyaktighet. Den er likevel relativt lett å forstå. En forvirringsmatrise forteller deg om du har et balansert datasett der utdataklassene har lignende antall. Når det gjelder scenarioet med flere klasser, forteller det deg hvor unøyaktig en prediksjon kan bli når utdataklassene er ordenstall, som i det foregående eksemplet med kundebetalinger.

## <a name="model-accuracy"></a>Modellnøyaktighet 
Ulike nøyaktighetsmåledata har fordelen av å kvantifisere modellkvaliteten. 

Siden nøyaktighet er en enkel måling å forstå, er det et godt utgangspunkt for å forklare en modell til andre personer, særlig til brukere av modellen som ikke er dataforskere. Du trenger ikke å forstå statistikk for å kunne forstå nøyaktigheten til modellen. Når en forvirringsmatrise er tilgjengelig, gir den ytterligere innsikt i modellens ytelse.

Hvis du vil ha en grundigere forståelse, må du imidlertid være oppmerksom på flere utfordringer knyttet til nøyaktighet. Hvor nyttig målingen er, avhenger av konteksten til problemet. Et spørsmål som ofte stilles i forhold til modellytelse, er «Hvor god er modellen?» Det er imidlertid ikke nødvendigvis et enkelt svar på dette spørsmålet. La oss se på den følgende forvirringsmatrisen (modell 2).

![Eksempel på betalingsprediksjon med et større utvalg](media/payment-prediction-matrix-2.png)

En rask beregning viser at denne modellens nøyaktighet er (70 + 10 + 3) ÷ 100 eller 0,83. Dette resultatet er tilsynelatende bedre enn resultatet for den forrige modellen med flere klasser (modell 1), som har en nøyaktighet på 0,73. Men er den bedre?

Du kan begynne å svare på dette spørsmålet ved å vurdere nøyaktigheten til en naiv gjetning. For et klassifiseringsproblem vil en enkel gjetning alltid forutsi den vanligste klassen. I modell 1 vil denne gjetningen være «til planlagt tid», og det gir en nøyaktighet på 0,50. Gjetningen i modell 2 blir også «til planlagt tid», og det gir en nøyaktighet på 0,80. Siden modell 1 forbedrer den naive gjetningen med 0,73 – 0,50 = 0,23, mens modell 2 forbedrer den naive gjetningen med 0,83 – 0,80 = 0,03, er modell 1 en bedre modell, selv om den har lavere nøyaktighet. Beregningen viser at effektiv vurdering av en modells kvalitet krever mer kontekst enn nøyaktighetsverdien.

Et annet aspekt er også verdt å merke seg. Tenk deg et scenario der en medisinsk test brukes til å oppdage en sykdom i en pasient. Dette problemet er av typen binær klassifisering, der et positivt resultat angir at pasienten har sykdommen. I dette scenarioet må du tenke på virkningen av følgende feil:

- Falske positive, der testen angir at en pasient har sykdommen, men vedkommende egentlig ikke har den.
- Falske negative, der testen angir at en pasient ikke har sykdommen, men vedkommende egentlig har den.

Begge typer feil er selvsagt uønsket, men hvilken er verst? Det kommer igjen an på konteksten. Hvis det er snakk om en livstruende sykdom som må behandles raskt, prioriteres minimering av falske negative (forhåpentlig etterfulgt av flere tester). I andre mindre kritiske situasjoner kan de som laget modellen, kanskje fokusere på å minimere falske positive i stedet. En rimelig konklusjon er i alle fall at for å kunne effektivt fastsette kvaliteten til en modell, må du har mer informasjon enn det en nøyaktige måleverdi gir.

### <a name="recommendations"></a>Anbefalinger

Nøyaktighet er et viktig verktøy for kommunikasjon med domeneeksperter som ikke vet mye om statistikk. For å gjøre informasjonen nyttig er det imidlertid avgjørende at ytterligere kontekst gis sammen med nøyaktighetsverdien.

Når det gjelder scenarioet med betalingsprediksjon, kan du angi et mål for ML-modellen som omfatter faktorer i ulike betalingsatferder. Målet er at modellen skal forbedre en naiv gjetning ved å redusere antallet feilaktige svar med minst 50 prosent. Du vil med andre ord ha en målnøyaktighet som er et kompromiss mellom nøyaktigheten til en naiv gjetning og 100 prosent.

Tabellen nedenfor inneholder et sammendrag av dette prinsippet for forvirringsmatrisene i dette emnet.

| Modell   | Naiv gjetning | Mål | Modellnøyaktighet | Er målet oppnådd?                                          |
|---------|-------------|--------|----------------|-----------------------------------------------------------|
| Modell 1 | 0.50        | 0.75   | 0.73           | Nesten. Denne modellen er betydelig bedre enn gjetningen. |
| Modell 2 | 0.80        | 0.90   | 0.83           | Nr. Forbedring er nødvendig.                              |

## <a name="classification-f1-accuracy"></a>F1-nøyaktighet for klassifisering

Det siste vi skal se på i dette emnet, er et mer avansert mål på ytelsen til klassifiserings-ML som kalles F1-nøyaktighet.

Før F1-nøyaktighet kan defineres, må to andre måleverdier introduseres: presisjon og tilbakekalling. Presisjon angir hvor mange av totalt antall prediksjoner som er angitt som positive, er riktig tilordnet. Denne måleverdien kalles også den positive forutsigende verdien. Tilbakekalling er det totale antallet av de faktiske positive tilfellene som ble riktig forutsagt. Denne måleverdien kalles også følsomhet.

[![Sanne kontra usanne resultater](./media/tn-fn.png)](./media/tn-fn.png)

I forvirringsmatrisen i den foregående illustrasjonen beregnes disse måleverdiene på følgende måte:

- Presisjon = TP ÷ (TP + RP)
- Tilbakekalling = TP ÷ (TP + FN)

F1-målingen kombinerer presisjon og tilbakekalling. Resultatet er den harmoniske middelverdien av de to verdiene. Den beregnes på følgende måte:

- F1 = 2 × (presisjon × tilbakekalling) ÷ (presisjon + tilbakekalling)

La oss se på et konkret eksempel. Tidligere i dette emnet var det et eksempel på en modell som forutsa om et dyr var en hund eller en katt. Illustrasjonen gjentas her.

[![Eksempel på artsprediksjon (gjentatt)](./media/species-prediction-matrix.png)](./media/species-prediction-matrix.png)

Her er resultatet hvis «Hund» brukes som det positive svaret.

- Presisjon = 24 ÷ (24 + 2) = 0,9231
- Tilbakekalling = 24 ÷ (24 + 6) = 0,8
- F1 = 2 × (0,9231 × 0,8) ÷ (0,9231 + 0,8) = 0,8572

Som du kan se, er verdien for F1 mellom verdiene for presisjon og tilbakekalling.

Selv om det ikke er like lett å forstå F1-nøyaktighet, tilføyer det nyanse til det grunnleggende nøyaktighetstallet. Det kan også være til hjelp i ubalanserte datasett, som den følgende diskusjonen viser.

Delen [Modellnøyaktighet](#model-accuracy) i dette emnet sammenlignet de to følgende forvirringsmatrisene. Selv om den første modellen hadde lavere nøyaktighet, ble den regnet for å være en nyttigere modell fordi den hadde større forbedring enn standardgjetningen for en betaling i tide.

![Eksempel på betalingsprediksjon kontra faktiske tilfeller](media/payment-prediction-matrix.png)

![Eksempel på betalingsprediksjon med et større utvalg (gjentatt)](media/payment-prediction-matrix-2.png)

La oss sammenligne disse to modellene når F1-poengsummen brukes. F1-poengsummen tar hensyn til presisjon og tilbakekalling for hver tilstand, og F1-makroberegningen beregner deretter gjennomsnittet av F1-poengsummen på tvers av tilstandene for å beregne en samlet F1-poengsum. Det finnes andre F1-varianter, men det er mer interessant å vurdere makroversjonen, gitt at det tas like stort hensyn til alle tre tilstandene.

For å forenkle beregningene ble det bygd eksempelmatriser for å sammenligne de faktiske og forutsagte verdiene. Disse matrisene brukte sklearns målingsbibliotek i Python til å beregne verdiene. Her er resultatet.

| Modell   | Naiv gjetning | Presisjon | F1-makro |
|---------|-------------|----------|----------|
| Modell 1 | 0.5         | 0.73     | 0.67     |
| Modell 2 | 0.80        | 0.83     | 0.66     |

Hvis du vil ha mer informasjon om hvordan denne beregningen fungerer, har du her klassifiseringsrapporten sklearn.metrics for modell 1. De tre tilstandene Til planlagt tid, For sent og Svært sent representeres av radene som er merket med henholdsvis 1, 2 og 3. Makrogjennomsnittet er bare gjennomsnittet av kolonnen for F1-poengsum.

|           | presisjon | tilbakekalling   | f1-poengsum |
|-----------|-----------|----------|----------|
| **1**     | 0.83      | 0.80     | 0.82     |
| **2**     | 0.68      | 0.71     | 0.69     |
| **3**     | 0.50      | 0.50     | 0.50     |

Som disse resultatene viser har de to modellene nesten identiske poengsummer for F1-makronøyaktighet. I dette og mange andre tilfeller er F1-nøyaktighet en bedre indikator på hvor god en modell er. Som for nøyaktighet krever tolkningen av resultatene at du forstår hva som er det viktigste å ta hensyn til i modellen.

#### <a name="privacy-notice"></a>Personvernerklæring
Forhåndsversjoner (1) kan ha redusert personvern og færre sikkerhetstiltak enn Dynamics 365 Finance and Operations-tjenesten, (2) er ikke inkludert i serviceavtalen (SLA) for denne tjenesten, (3) må ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) har begrenset støtte.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]