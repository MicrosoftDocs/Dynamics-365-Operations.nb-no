---
title: Finansdimensjoner
description: Dette emnet beskriver de ulike typene finansdimensjoner og hvordan de er definert.
author: aprilolson
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ems.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: af93f115dca3f26a984c53e044659f4eac9986f1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249369"
---
# <a name="financial-dimensions"></a>Finansdimensjoner

[!include [banner](../includes/banner.md)]

Dette emnet forklarer de ulike typene finansdimensjoner og hvordan de er definert.

Bruk **Finansdimensjoner**-siden til å opprette finansdimensjoner som du kan bruke som kontosegmenter for kontoplaner. Det finnes to typer finansdimensjoner: egendefinerte dimensjoner og enhetsstøttede dimensjoner. Egendefinerte dimensjoner deles på tvers av juridiske enheter, og verdiene angis og vedlikeholdes av brukerne. For enhetsstøttede dimensjoner er verdiene definert andre steder i systemet, for eksempel som kunde- eller butikkenheter. Noen enhetsstøttede dimensjoner deles på tvers av juridiske enheter, mens andre enhetsstøttede dimensjoner er firmaspesifikke.

Når du har opprettet finansdimensjonene, bruker du **Finansdimensjonsverdier**-siden til å tilordne flere egenskaper til hver finansdimensjon.

Du kan bruke finansdimensjoner til å representere juridiske enheter. Du trenger ikke å opprette de juridiske enhetene i Dynamics 365 Finance. Finansdimensjoner er imidlertid ikke utviklet for å håndtere drifts- eller forretningbehovene til juridiske enheter. Funksjonen internenhetsregnskap i Finance er utviklet for bare å håndtere regnskapsoppføringene som opprettes av hver transaksjon.

Før du setter opp finansdimensjoner som juridiske enheter, vurderer du forretningsprosessene i følgende områder for å se hvorvidt dette oppsettet fungerer for din organisasjon:

- Lager
- Kjøp og salg mellom finansdimensjoner og juridiske enheter
- Mva-beregning og rapportering
- Driftsrapportering

Her er noen av begrensningene:

- Du kan bare bruke mva-funksjonaliteten med juridiske enheter, ikke med finansdimensjoner.
- Noen av rapportene inneholder ikke finansdimensjoner. Derfor kan det hende du må endre rapportene for å rapportere etter finansdimensjon.

## <a name="custom-dimensions"></a>Egendefinerte dimensjoner

For å opprette en brukerdefinert finansdimensjon velger du **Egendefinert dimensjon** i feltet **Bruk verdier fra**.

Du kan også angi en kontomaske for å begrense mengden og typen informasjon som kan angis for dimensjonsverdier. Du kan angi tegn som forblir de samme for hver dimensjonsverdi, for eksempel bokstaver eller en bindestrek (-). Du kan også angi nummertegn (\#) og og-tegn (&) om plassholdere for tegn som vil endres hver gang en dimensjonsverdi opprettes. Bruk et nummertegn (\#) som plassholder for et tall og et og-tegn (&) som plassholder for en bokstav. Feltet for formatmasken er bare tilgjengelig når du velger **Egendefinert dimensjon** i feltet **Bruk verdier fra**.

**Eksempel**

Hvis du vil begrense dimensjonsverdien til bokstavene «CC» og tre tall, kan du angi **CC-\#\#\#** som formatmaske.

## <a name="entity-backed-dimensions"></a>Enhetsstøttede dimensjoner

Hvis du vil opprette en enhetsstøttet finansdimensjon, velger du en systemdefinert enhet som basis for finansdimensjonen, i feltet **Bruk verdier fra**. Finansdimensjonsverdier opprettes deretter fra den enheten. Hvis du for eksempel vil opprette dimensjonsverdier for prosjekter, velger du **Prosjekter**. En dimensjonsverdi opprettes deretter for hvert prosjektnavn. Siden **Finansdimensjonsverdier** viser verdiene for enheten. Hvis disse verdiene er firmaspesifikke, viser siden også firmaet.

## <a name="activating-dimensions"></a>Aktivering av dimensjoner

Når du aktiverer en finansdimensjon, oppdateres tabellen slik at den inkluderer navnet på finansdimensjonen. Slettede dimensjoner fjernes. Du kan angi dimensjonsverdier før du aktiverer en finansdimensjon. En finansdimensjon ikke imidlertid ikke brukes hvor som helst før den er aktivert. Du kan for eksempel ikke legge til en finansdimensjon i en kontostruktur før finansdimensjonen er aktivert. Når du velger **Aktiver**, oppdateres alle dimensjoner, og viser statusendringer.

## <a name="translations"></a>Oversettelser

På siden  **Tekstoversettelse** kan du skrive inn tekst for den valgte finansdimensjonen i forskjellige språk. På siden  **Tekstoversettelse** kan du skrive inn tekst for hovedkontoen i forskjellige språk. 

## <a name="legal-entity-overrides"></a>Overstyringer for juridisk enhet

Alle dimensjonene er ikke gyldig for alle juridiske enheter. Dessuten kan noen dimensjoner bare være relevante i en bestemt periode. I disse tilfellene kan du bruke delen **Overstyringer for juridisk enhet** til å angi firmaene dimensjonen skal suspenderes for, eieren, og tidsperioden dimensjonen er aktiv.

## <a name="deleting-financial-dimensions"></a>Slette finansdimensjoner

For å opprettholde referanseintegriteten for dataene, kan finansdimensjoner sjelden slettes. Hvis du prøver å slette en finansdimensjon, evalueres følgende kriterier:

- Er finansdimensjonen brukt på posterte eller uposterte transaksjoner, eller i en type dimensjonsverdikombinasjon?
- Er finansdimensjonen brukt i en aktiv kontostruktur, avansert regelstruktur eller i et finansdimensjonssett?
- Er finansdimensjonen en del et standardformat for finansdimensjonsintegrasjon?
- Er finansdimensjonen er satt opp som standarddimensjon?

Hvis ett av vilkårene er oppfylt, kan du ikke slette finansdimensjonen.

## <a name="default-dimension-values"></a>Standard dimensjonsverdier

Du kan bruke verdier fra overordnede oppføringer, for eksempel kunder og leverandører, som standardverdier i nye dimensjoner. Når nye dimensjoner opprettes, er overordnet post-ID angitt i dimensjonsverdier for disse hovedoppføringene. Når du for eksempel oppretter en ny kunde, angis kunde-ID-en i kundedimensjonen. Når du oppretter salgsordrer, fakturaer eller andre dokumenter som krever en kunde-ID, brukes de eksisterende standardreglene, og kunde-ID-en legges til i dokumentet.

Denne funksjonen styres av en innstilling i dimensjonen. Denne innstillingen kalles **Kopier verdier til denne dimensjonen i hver nye DimensionName som er opprettet**, der **DimensionName** er navnet på dimensjonen. Funksjonen er deaktivert som standard. Men den kan aktiveres når som helst.

Hvis det allerede finnes poster for dimensjonen, oppdateres de overordnede postene når du aktiverer funksjonen. Imidlertid oppdateres ikke eksisterende dokumenter og transaksjoner.

Hvis du bruker en mal til å opprette en hovedoppføring, må du kontrollere at malverdien for hoveddimensjonen er tom. Hvis du for eksempel oppretter kunder fra en mal, må du kontrollere at kundedimensjonen i malen er tom. Kundedimensjonsverdien hentes som standard fra det nye kundenummeret når du oppretter den nye kunden.  

## <a name="derived-dimensions"></a>Avledede dimensjoner

Du kan konfigurere en dimensjon slik at informasjonen for andre dimensjoner angis automatisk når du angir denne dimensjonen i et dokument. Hvis du angir kostsenter 10, kan verdien **20** angis automatisk i avdelingsdimensjonen.

Du kan definere avledede verdier på dimensjonssiden.

1. Velg en dimensjon, og velg deretter **Avledede dimensjoner**.

    Siden **Avledede dimensjoner** inneholder et rutenett. Det valgte dimensjonssegmentet er den første kolonnen i rutenettet.

2. Legg til segmentene som skal avledes. Hvert segment vises som en kolonne.

Angi dimensjonskombinasjonene som skal avledes fra dimensjonsfeltene, i den første kolonnen. Hvis du for eksempel vil bruke kostsenteret som dimensjonenen som avdelingen og lokasjonen er avledet fra, angir du kostsenter 10, avdeling 20 og lokasjon 30. Deretter, når du angir kostsenter 10 i en hovedoppføring eller på en transaksjonsside, angis avdeling 20 og lokasjon 30 som standard.

### <a name="overriding-existing-values-with-derived-dimensions"></a>Overstyre eksisterende verdier med avledede dimensjoner
 
Den avledede dimensjonsprosessen overstyrer som standard ikke eksisterende verdier for avledede dimensjoner. Hvis du angir kostsenter 10, og ingen andre dimensjoner er angitt, blir for eksempel avdeling 20 og lokasjon 30 angitt som standard. Men hvis du endrer kostsenteret, endres ikke verdiene som allerede er opprettet. Derfor kan du opprette standarddimensjoner på hovedoppføringer, og disse dimensjonene endres ikke etter avledede dimensjoner.

Du kan endre virkemåten til avledede dimensjoner for å overstyre eksisterende verdier, ved å merke av for **Erstatt eksisterende dimensjonsverdier med avledede verdier** på siden **Avledede dimensjoner**. Hvis dette feltet er valgt, kan du angi en dimensjon med avledede dimensjonsverdier, så vil de avledede dimensjonsverdiene overskrive verdier som allerede finnes. Hvis vi bruker det forrige eksemplet: Hvis du angir kostsenter 10, og ingen andre dimensjoner er angitt, blir for eksempel avdeling 20 og lokasjon 30 angitt som standard. Hvis verdiene imidlertid allerede var avdeling 50 og lokasjon 60, endres verdiene nå til avdeling 20 og lokasjon 30.
 
Avledede dimensjoner med denne innstillingen erstatter ikke automatisk de eksisterende standard dimensjonsverdiene når dimensjonsverdier angis som standard. Dimensjonsverdier vil bare bli overskrevet når du angir en ny dimensjonsverdi på en side, og det finnes eksisterende avledede verdier for denne dimensjonen på siden.

### <a name="preventing-changes-with-derived-dimensions"></a>Hindre endringer ved hjelp av avledede dimensjoner
 
Når du bruker **Legg til segment** på siden **Avledede dimensjoner** for å legge til et segment som en avledet dimensjon, angis et alternativ nederst på siden **Legg til segment** der du kan unngå endringer i dimensjonen når den hentes inn på en side. Standardinnstillingen er deaktivert, så den hindrer ikke de avledede dimensjonsverdiene fra å bli endret. Endre innstillingen til **Ja** hvis du vil hindre at dimensjonen blir endret etter at den er avledet. Hvis for eksempel verdien for avdelingsdimensjonen er avledet fra verdien for kostsenterdimensjonen, kan ikke avdelingsverdien endres hvis innstillingen **Hindre endringer** er **Ja**. 
 
Innstillingen hindrer ikke endringer hvis dimensjonsverdien er gyldig, men den er ikke oppført i listen over avledede dimensjoner. For eksempel hvis Avdeling 20 er avledet fra Kostsenter 10, og du angir Kostsenter 10, kan du ikke redigere Avdeling 20. Hvis du imidlertid angir Kostsenter 20, og det ikke er i listen over avledede dimensjoner for Kostsenter, kan du redigere avdelingsverdien. 
 
I alle tilfeller blir kontoverdien og alle dimensjonsverdiene likevel validert mot kontostrukturene etter at de avledede dimensjonsverdier er brukt. Hvis du bruker avledede dimensjoner, og valideringen mislykkes når de brukes på en side, må du endre de avledede dimensjonsverdiene på siden for avledede dimensjoner før du kan bruke dem i transaksjoner. 
 
Når du endrer dimensjoner i hurtigfanen **Finansdimensjoner**, vil ikke dimensjonen som er merket for å hindre endringer, kunne redigeres. Hvis du angir en konto og dimensjoner i den segmenterte angivelseskontrollen på en side, er dimensjonene redigerbare. Men når du flytter markeringen fra den segmenterte angivelseskontrollen og flytter til et annet felt eller iverksetter en handling, vil kontoen og dimensjonene bli validert mot den avledede dimensjonslisten og kontostrukturene for å sikre at du har angitt riktige verdier. 

### <a name="derived-dimensions-and-entities"></a>Avledede dimensjoner og enheter

Du kan definere avledede dimensjonssegmenter og -verdier ved hjelp av enheter.

- Den avledede dimensjonsenheten angir de drivende dimensjonene og segmentene som skal brukes for disse dimensjonene.
- Avledede dimensjonsverdier-enheten lar deg importere verdiene som skal avledes for hver drivende dimensjon.

Når du bruker en enhet til å importere data, hvis denne enheten importerer dimensjoner, brukes reglene for avledet dimensjon under importen, med mindre enheten spesifikt overstyrer disse dimensjonene.

Hvis du vil ha mer informasjon, se følgende emner:

- [Definere finansdimensjoner](tasks/define-financial-dimensions.md)
- [Vedlikeholde standardmaler for finansdimensjon](tasks/maintain-financial-dimension-default-templates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]