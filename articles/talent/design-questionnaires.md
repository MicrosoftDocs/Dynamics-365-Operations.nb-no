---
title: "Utforme et spørreskjema"
description: "Dette emnet beskriver fremgangsmåten for å opprette et spørreskjema. Det første trinnet er å utforme spørreskjemaet. Når du utformer et spørreskjema, skriver du ikke bare spørsmålene og svarene, men du oppretter også strukturen som gjør at svar kan registreres og ordnes i tabellform."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e406be47f33f388ad8088524700c4f3e331998c8
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="design-a-questionnaire"></a>Utforme et spørreskjema

[!include[banner](includes/banner.md)]

Dette emnet beskriver fremgangsmåten for å opprette et spørreskjema. Det første trinnet er å utforme spørreskjemaet. Når du utformer et spørreskjema, skriver du ikke bare spørsmålene og svarene, men du oppretter også strukturen som gjør at svar kan registreres og ordnes i tabellform. 

Et nøye utformet spørreskjema kan være med på å øke kvaliteten på dataene du samler inn. Gjennom nøye utforming kan du bedre velge de riktige alternativene til rett tid for et spørreskjema. Følgende punkt kan gjøre det enklere å planlegge et effektivt spørreskjema:

-   Definer formålet med spørreskjemaet klart og tydelig for å bidra til å garantere at spørsmålene understøtter formålet.
-   Avgjør hvilken person eller gruppe som skal fylle ut spørreskjemaet.
-   Skriv spørsmål som skal vises i spørreskjemaet, og ta eventuelt med svaralternativer.
-   Pass på at spørreskjemaet har en logisk flyt, slik at respondenter holdes engasjert.
-   Ordne spørsmål og svar i rekkefølgen de skal vises til respondentene.
-   Angi eventuelt hvordan resultatene skal evalueres.
-   Avgjør om du trenger flere funksjoner. Avgjør for eksempel om og hvordan resultatene skal kategoriseres, om det kreves en tidsfrist, eller om alle spørsmålene skal være obligatoriske.

Utformingsfasen inneholder fire kategorier med oppgaver du må fullføre i denne rekkefølgen:

1.  Definer forutsetninger etter behov.
2.  Definer om nødvendig svargrupper og svar.
3.  Definer spørsmål og tilknytningen deres til svargruppen.
4.  Definer selve spørreskjemaet, og knytt spørsmål til det.

## <a name="prerequisites"></a>Nødvendig programvare
Enkelte forutsetninger er nødvendige før du kan opprette spørreskjemaer, spørsmål og svar. Men ikke alle forutsetninger nødvendige for å utnytte all funksjonalitet.

### <a name="required"></a>Obligatorisk

| Forutsetning        | Beskrivelse                |
|---------------------|----------------------------|
| Spørreskjematyper | Kategoriser spørreskjemaer. |
| Spørsmålstyper      | Kategoriser spørsmål.      |

### <a name="optional"></a>Valgfri

| Forutsetning             | Beskrivelse                                                    |
|--------------------------|----------------------------------------------------------------|
| Spørreskjemaparametere | Endre grunnleggende kontroller og standardinnstillinger for spørreskjemaer. |

### <a name="questionnaire-types"></a>Spørreskjematyper

Spørreskjematyper er obligatoriske og må tilordnes når du oppretter et spørreskjema. Spørreskjematyper gjør det enklere å administrere og klassifisere spørreskjemaer. Bruk spørreskjematyper til å klassifisere spørreskjemaer og skille dem fra hverandre. Hvis du for eksempel har flere spørreskjemaer for å velge mellom, kan du filtrere dem etter type for å gjøre det enklere å finne et bestemt spørreskjema. Her er noen eksempler på spørreskjematyper:

-   Personaleutvikling
-   Kundeundersøkelser
-   Gå gjennom prosess

### <a name="question-types"></a>Spørsmålstyper

Spørsmålstyper er obligatoriske og må tilordnes når du lager et spørsmål. 

Bruk spørsmålstyper til å kategorisere spørsmål for rapportering. Spørsmålstyper gjør det også enklere å finne spørsmål, fordi du kan bruke typer som filtre på **Spørsmål**-siden. Her er noen eksempler på spørsmålstyper:

-   Personale
-   Forretningsadministrasjon
-   Kursevaluering

### <a name="questionnaire-parameters"></a>Spørreskjemaparametere

Spørreskjemaparametere er valgfrie. Du trenger ikke å bruke dem, avhengig av firmaets behov. 

Spørreskjemaparametere definerer anonymitet, nummerseriekoder og referansetyper i et spørreskjema. Når en organisasjon distribuerer et spørreskjema, kan alternativet for å la respondenter være anonyme være av betydning. 

Nummerseriekodene brukes til å organisere spørsmål og svar. Basert på disse nummerseriekodene tilordnes verdier automatisk til elementer. 

Du bør definere alle parametere før du begynner å opprette dataene. Du kan endre innstillingene for spørreskjemaparametere når som helst.

## <a name="questionnaire-components"></a>Spørreskjemakomponenter
Spørreskjemaer omfatter tre hovedelementer: svargrupper som inneholder svarene på spørsmål med flere valg, spørsmål og selve spørreskjemaet. Du kan også eventuelt gruppere spørsmålene i et spørreskjema i resultatgrupper. Resultatgrupper gjør at du kan kategorisere spørsmål og gi ytterligere analyse i spørreskjemaet. 

[![Spørreskjemakomponenter](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)

### <a name="answer-groups-and-answers"></a>Svargrupper og svar

Respondenter kan svare på spørsmål på to måter, avhengig av spørsmålets emne:

-   Åpne spørsmål krever ikke svar i et bestemt format. Respondenter kan skrive inn svaret i form av tekst, et tall, en dato eller et klokkeslett. Disse spørsmålene krever som regel at respondentene gir subjektiv informasjon i sine svar, for eksempel en oppfatning, en beskrivelse, en vurdering eller et estimat.
-   Lukkede spørsmål krever at respondenten velger et svar i en liste over mulige riktige svar.

Hvis du vil bruke en liste over mulige svar for lukkede spørsmål, kan du lage svarene på **Svargrupper**-siden. 

Svargrupper og svar er komponenter som utgjør hoveddelen av informasjon som spørsmål lages fra. Etter at du har opprettet en svargruppe, kan du tilordne svargruppen til et spørsmål i **Svargruppe**-feltet på **Spørsmål**-siden. 

En svargruppe kan brukes til flere spørsmål i det samme spørreskjemaet og kan også brukes i flere spørreskjemaer. 

**Obs!** Hvis du endrer svarteksten i svargrupper som allerede er brukt i fullførte spørreskjemaer, kan data bli vanskelige å evaluere, og spørreskjemaresultater slutter kanskje å være gyldige. Hvis du må endre en svargruppe, bør du vurdere å opprette en ny svargruppe i stedet for å endre en eksisterende. Du kan ikke slette svargrupper som er knyttet til et spørsmål eller svar, eller som er besvart.

### <a name="questions"></a>Spørsmål

Et spørreskjema må inneholde spørsmål. Spørsmål kan enten være åpne eller lukkede.

-   Svarene på åpne spørsmål kontrolleres ikke, og respondentene kan skrive inn svarene sine.
-   Lukkede spørsmål krever en liste over forhåndsdefinerte svaralternativer, og spørsmålene kan struktureres slik at en respondent kan velge flere svar. Spørsmål bør utformes slik at respondenten gir spesifikk informasjon, og de må kobles til en svargruppe som gir svaralternativene for hvert lukkede spørsmål. 
     -  **Obs!** Før du kan definere lukkede spørsmål, må du opprette svargrupper og svar.

Spørsmål kan ordnes i et hierarki for betingede spørsmål, slik at sekundære spørsmål avhenger av svaret respondenten valgte for det forrige spørsmålet. Du kan skrive spørsmålene først og deretter ordne dem i et hierarki senere.

## <a name="setting-up-questionnaires"></a>Definere spørreskjemaer
**Obs!** Før du kan opprette et spørreskjema, må du definere svar, spørsmål og forutsetninger. 

For hvert spørreskjema kan du angi følgende informasjon:

-   Samlet tid eller tidsfristen for å svare på obligatoriske spørsmål
-   Om alle spørsmålene er obligatoriske
-   Om poeng skal beregnes i et spørreskjema
-   Hvordan resultatene skal kategoriseres
-   Om spørreskjemaet skal være tilgjengelig for et begrenset sett med respondenter
-   Om en skjemamal skal vises som bakgrunn bak hver side i spørreskjemaet
-   Om ytterligere notater er nødvendige for å forklare hensikten med spørreskjemaet til respondentene
-   Om spørsmål skal vises i en fast rekkefølge eller velges i tilfeldig rekkefølge fra et utvalg
-   Om spørsmål bare skal stilles hvis bestemte svar gis for tidligere svar.

### <a name="set-up-a-questionnaire"></a>Definere et spørreskjema

Den primære siden du bruker til å definere et spørreskjema, er **Spørreskjemaer**-siden. Fullfør følgende oppgaver i angitt rekkefølge for å definere et spørreskjema:

1.  Opprett et spørreskjema.
2.  Følg ett av disse trinnene for å knytte spørsmål til spørreskjemaet:
    -   Hvis du bruker resultatgrupper, kan du knytte spørsmål til et spørreskjema ved hjelp av resultatgrupper. Først definerer du resultatgruppene for spørreskjemaet, og deretter legger du til spørsmål i resultatgruppene.
    -   Hvis du ikke bruker resultatgrupper, kan du knytte spørsmål direkte til spørreskjemaet.

3.  Definer om nødvendig et hierarki for betingede spørsmål.
4.  Test spørreskjemaet.

Klikk **Valider** på **Spørreskjemaer**-siden for å teste om spørreskjemaet er riktig satt sammen. Det er imidlertid også en god idé å fylle ut spørreskjemaet og teste det selv før du distribuerer det.

### <a name="modify-a-questionnaire"></a>Endre et spørreskjema

Du kan fullføre følgende oppgaver på **Spørreskjemaer**-siden:

-   Endre informasjonen i spørreskjemaet, for eksempel resultatgrupper og spørsmål
-   Slette og legge til spørsmål
-   Gjøre endringer i resultatgruppene og serienummeret 

**Forsiktig!** Vær forsiktig når endrer spørreskjemaer som allerede er besvart. Endringer kan redusere nøyaktigheten til statistikk og derfor gjøre statistikken til et dårlig evalueringsgrunnlag. Vurder å lage et nytt spørsmål i stedet for å endre et spørsmål som allerede er besvart.

Du kan ikke slette følgende typer spørsmål i et spørreskjema:

-   Spørsmål som er knyttet til et spørreskjema
-   Spørsmål som allerede er besvart og derfor vises i dialogboksen **Svar**

### <a name="result-groups"></a>Resultatgrupper

Resultatgrupper er valgfrie når du knytter spørsmål til et spørreskjema. 

En resultatgruppe brukes til å beregne poeng og kategorisere resultatene i et spørreskjema. Hvis du bruker resultatgrupper, kan du utføre følgende oppgaver:

-   Evaluere spørreskjemaresultater basert på poengstatistikk.
-   Evaluere en respondents poengsum for hver resultatgruppe du definerer.
-   Generere statistikk for hver resultatgruppe for å hjelpe deg med å analysere resultatene.
-   Skrive ut en rapport som viser resultatene for hver resultatgruppe, samt valgfrie poeng/tekster som er basert på poeng som fås i hver resultatgruppe.

**Obs!** Før du kan definere resultatgruppene, må du fullføre følgende oppgaver:

-   Definer lukkede spørsmål. Når det gjelder lukkede spørsmål, må inndatatypen på **Spørsmål**-siden være **Avmerkingsboks**, **Alternativknapp** eller **Kombinasjonsboks**.
-   Definer poeng for svar i svargruppene som er tilordnet hvert spørsmål.
-   Definer et spørreskjema.

Hvis du vil knytte spørsmål til et spørreskjema ved hjelp av resultatgrupper, definerer du først resultatgruppene for spørreskjemaet, og deretter legger du til spørsmål i resultatgruppene. Hvis du ikke bruker resultatgrupper, kan du knytte spørsmål direkte til et spørreskjema. 

Du kan definere flere resultatgrupper for å evaluere poengene en respondent får i hver kategori. Når et spørreskjema er fullført, kan du vise poengene som er oppnådd for hver resultatgruppe. 

**Tips!** Hvis du vil evaluere et spørreskjema ved å bruke poeng, men ikke separate kategorier, kan du legge til alle spørsmål i én resultatgruppe. 

For hver resultatgruppe kan du også definere én eller flere poengbaserte meldinger som respondenter får når de har fullført et spørreskjema. Teksten som vises, kan variere avhengig av poengsummen en respondent får i en resultatgruppe. Hvis du vil bruke poengbaserte meldinger, må du definere du poengintervaller og en beskrivelse av hvert intervall. Når en respondent oppnår en poengsum i et bestemt intervall, tas teksten for dette intervallet med i resultatrapporten. 

Siden en resultatgruppe er knyttet til poengene som er knyttet til bestemte sett med spørsmål i et spørreskjema, kan du bare bruke en bestemt resultatgruppe for et spørreskjema.

#### <a name="example-pointstexts-for-result-group-3"></a>Eksempel: Poeng/tekster for resultatgruppe 3

Du bruker et spørreskjema i en ledertest med 15 spørsmål i tre kategorier. Du oppretter tre resultatgrupper og legger til fem spørsmål i hver resultatgruppe. Poeng legges deretter sammen i de tre gruppene. De tre resultatgruppene er som følger:

-   Kreative ferdigheter
-   Lederegenskaper
-   Tekniske ferdigheter

Hvis du vil bruke poengbaserte meldinger, definerer du tekstintervaller for hver resultatgruppe. Hvert spørsmål tilordnes to poeng. Derfor er den største mulige poengsummen i hver resultatgruppe 10. 

Tabellen nedenfor viser poengbaserte meldinger som du definerer for resultatgruppen "lederegenskaper".

| Poengintervall | Tekst                                       |
|----------------|--------------------------------------------|
| 1 til 3         | Du har gjennomsnittlige lederegenskaper.     |
| 4 til 7         | Du har gode lederegenskaper.        |
| 8 til 10        | Du har fremragende lederegenskaper. |

Du kan definere poengintervaller og tekster for hver resultatgruppe i et spørreskjema. Tekster som svarer til hver enkelt respondents poengsum, vises for hver resultatgruppe. 

**Obs!** Du kan endre intervaller og tekster. Vær likevel oppmerksom på at hvis et spørreskjema er ferdig utfylt, kan endringer føre til forskjeller mellom tidligere og nye resultatrapporter.

### <a name="conditional-question-hierarchies"></a>Hierarkier for betingede spørsmål

Hierarkier for betingede spørsmål er valgfrie når du definerer et spørreskjema. 

**Obs!** Før du kan opprette et hierarki for betingede spørsmål, må du knytte spørsmål som har tilordnede svargrupper, til spørreskjemaet. 

Hvis du vil bruke betingede spørsmål til å opprette et spørsmålshierarki i et spørreskjema, kan du gjøre rekkefølgen som spørsmålene stilles i, avhengig av svaret en respondent velger for hvert spørsmål. Når du baserer spørsmålsrekkefølgen på svaret til en respondent, kan du endre spørreskjemaet mens respondenten fyller det ut.

#### <a name="examples"></a>Eksempler

En juridisk enhet tilbyr både varer og tjenester til kunder. Som vanlig i slike tilfeller kjøper enkelte kunder bare varer, noen bare tjenester og andre både varer og tjenester. Når den juridiske enheten distribuerer en undersøkelse om kundetilfredshet, bruker den en betinget struktur på spørreskjemaet, slik at kunder som bare kjøper tjenester, ikke trenger å svare på spørsmål om varer. 

Alternativt kan du definere du et spørreskjema slik at hvis en respondent velger svar A på spørsmål 1, er spørsmål 2 det neste spørsmålsrekkefølgen. Hvis respondenten i stedet velger svar B på spørsmål 1, er spørsmål 5 det neste spørsmålet.

<a name="see-also"></a>Se også
--------

[Bruke spørreskjemaer](questionnaires.md)

[Distribuere og fylle ut spørreskjemaer](distribute-questionnaires.md)

[Vise og evaluere resultatene i spørreskjemaer](evaluate-questionnaire-results.md)


