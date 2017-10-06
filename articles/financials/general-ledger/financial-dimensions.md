---
title: Finansdimensjoner
description: Dette emnet beskriver de ulike typene finansdimensjoner og hvordan de er definert.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c4f5dae90c5fcaaa52a7087d7c20b2de343b7da0
ms.openlocfilehash: b5615a6d9003554593981ce65be0283a249a7d93
ms.contentlocale: nb-no
ms.lasthandoff: 08/01/2017

---

# <a name="financial-dimensions"></a>Finansdimensjoner

[!include[banner](../includes/banner.md)]

Dette emnet forklarer de ulike typene finansdimensjoner og hvordan de er definert.

Bruk **Finansdimensjoner**-siden til å opprette finansdimensjoner som du kan bruke som kontosegmenter for kontoplaner. Det finnes to typer finansdimensjoner: egendefinerte dimensjoner og enhetsstøttede dimensjoner. Egendefinerte dimensjoner deles på tvers av juridiske enheter, og verdiene angis og vedlikeholdes av brukerne. For enhetsstøttede dimensjoner er verdiene definert andre steder i systemet, for eksempel som kunde- eller butikkenheter. Noen enhetsstøttede dimensjoner deles på tvers av juridiske enheter, mens andre enhetsstøttede dimensjoner er firmaspesifikke. 

Når du har opprettet finansdimensjonene, bruker du **Finansdimensjonsverdier**-siden til å tilordne flere egenskaper til hver finansdimensjon. 

Du kan bruke finansdimensjoner til å representere juridiske enheter. Du trenger ikke å opprette de juridiske enhetene i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Finansdimensjoner er imidlertid ikke utviklet for å håndtere drifts- eller forretningbehovene til juridiske enheter. Funksjonen internenhetsregnskap i Finance and Operations er utviklet for bare å håndtere regnskapsoppføringene som opprettes av hver transaksjon. 

Før du setter opp finansdimensjoner som juridiske enheter, vurderer du forretningsprosessene i følgende områder for å se hvorvidt dette oppsettet fungerer for din organisasjon:

- Lager
- Kjøp og salg mellom finansdimensjoner og juridiske enheter
- Mva-beregning og rapportering
- Driftsrapportering

Her er noen av begrensningene:

- Du kan bare bruke mva-funksjonaliteten med juridiske enheter, ikke med finansdimensjoner.
- Noen av rapportene inneholder ikke finansdimensjoner. Derfor kan det hende du må endre rapportene for å rapportere etter finansdimensjon.

## <a name="custom-dimensions"></a>Egendefinerte dimensjoner

For å opprette en brukerdefinert finansdimensjon velger du **Egendefinerte dimensjoner** i feltet **&lt;Bruk verdier fra&gt;**. Du kan også angi en kontomaske for å begrense mengden og typen informasjon som du kan angi for dimensjonsverdier. Du kan angi tegn som forblir de samme for hver dimensjonsverdi, for eksempel bokstaver eller en bindestrek (-). Du kan også angi nummertegn (\#) og og-tegn (&) om plassholdere for bokstaver og tall som vil endres hver gang en dimensjonsverdi opprettes. Bruk et nummertegn (\#) som plassholder for et tall og et og-tegn (&) som plassholder for en bokstav. Feltet for formatmasken er bare tilgjengelig når du velger **&lt;Egendefinert dimensjon&gt;** i feltet **Bruk verdier fra**.

**Eksempel**

Hvis du vil begrense dimensjonsverdien til bokstavene «CC» og tre tall, kan du angi **CC-\#\#\#** som formatmaske.

## <a name="entity-backed-dimensions"></a>Enhetsstøttede dimensjoner

Hvis du vil opprette en enhetsstøttet finansdimensjon, velger du en systemdefinert enhet som basis for finansdimensjonen, i feltet **Bruk verdier fra**. Finansdimensjonsverdier opprettes deretter fra den enheten. Hvis du for eksempel vil opprette dimensjonsverdier for prosjekter, velger du **Prosjekter**. En dimensjonsverdi opprettes deretter for hvert prosjektnavn. Siden **Finansdimensjonsverdier** viser verdiene for enheten. Hvis disse verdiene er firmaspesifikke, viser siden også firmaet.

## <a name="activating-dimensions"></a>Aktivering av dimensjoner

Når du aktiverer en finansdimensjon, oppdateres tabellen slik at den inkluderer navnet på finansdimensjonen. Slettede dimensjoner fjernes. Du kan angi dimensjonsverdier før du aktiverer en finansdimensjon. En finansdimensjon ikke imidlertid ikke brukes hvor som helst før den er aktivert. Du kan for eksempel ikke legge til en finansdimensjon i en kontostruktur før finansdimensjonen er aktivert. Når du klikker **Aktiver**, oppdateres alle dimensjoner, og viser statusendringer. 

## <a name="translations"></a>Oversettelser

På siden  **Tekstoversettelse** kan du skrive inn tekst for den valgte finansdimensjonen i forskjellige språk. På siden  **Tekstoversettelse** kan du skrive inn tekst for hovedkontoen i forskjellige språk. 

## <a name="legal-entity-overrides"></a>Overstyringer for juridisk enhet

Alle dimensjonene er ikke gyldig for alle juridiske enheter. Dessuten kan noen dimensjoner bare være relevante i en bestemt periode. I disse tilfellene kan du bruke delen **Overstyringer for juridisk enhet** til å angi firmaene dimensjonen skal suspenderes for, eieren, og tidsperioden dimensjonen er aktiv.

## <a name="deleting-financial-dimensions"></a>Slette finansdimensjoner

For å opprettholde referanseintegriteten for dataene, kan finansdimensjoner sjelden slettes. Hvis du prøver å slette en finansdimensjon, evalueres følgende kriterier:

- Er finansdimensjonen brukt på posterte eller uposterte transaksjoner, eller en type dimensjonsverdikombinasjon?
- Er finansdimensjonen brukt i en aktiv kontostruktur, avansert regelstruktur eller i et finansdimensjonssett?
- Er finansdimensjonen en del et standardformat for finansdimensjonsintegrasjon?
- Er finansdimensjonen er satt opp som standarddimensjon?

Hvis ett av vilkårene er oppfylt, kan du ikke slette finansdimensjonen.


Hvis du vil ha mer informasjon, se følgende emner:
- [Definere finansdimensjoner](tasks/define-financial-dimensions.md)
- [Vedlikeholde standardmaler for finansdimensjon](tasks/maintain-financial-dimension-default-templates.md)
