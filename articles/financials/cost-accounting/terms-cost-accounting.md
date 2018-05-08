---
title: Terminologi for kostnadsregnskap
description: Dette emnet beskriver de viktigste begrepene som brukes i Kostnadsregnskap.
author: YuyuScheller
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostAccountingLedger
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 1ec2f4a407c705fb37681f5593d0f7ea31f4cf0f
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="cost-accounting-terminology"></a>Terminologi for kostnadsregnskap

[!include [banner](../includes/banner.md)]

Dette emnet beskriver de viktigste begrepene som brukes i Kostnadsregnskap.

**Tildelingsgrunnlag**

Tildelingsgrunnlag brukes til å måle og kvantifisere aktiviteter, for eksempel maskintimer som brukes, kilowatt-timer som forbrukes eller kvadratfot som er opptatt. Den brukes som grunnlag for allokering av kostnader til en eller flere kostnadsobjekter

**Kostnadsregnskap**

Med Kostnadsregnskap kan du samle inn data fra forskjellige kilder, for eksempel i økonomimodulen, underfinans, budsjetter og statistisk informasjon. Deretter kan du analysere, summere og evaluere kostnadsdata, slik at ledelsen kan gjøre best mulig avgjørelsene for prisoppdateringer, budsjetter, kostnadskontroll og så videre. Kildedataene som brukes til å foreta kostnadsanalyser, behandles uavhengig av hverandre i Kostnadsregnskap. Oppdateringer i Kostnadsregnskap påvirker derfor ikke kildedataene. Når du samler inn kostnadsdata fra forskjellige kilder, og særlig når du importerer hovedkontoene fra Microsoft Dynamics 365 for Finance and Operations som kostnadselementer, er det imidlertid overflødige data, fordi de samme dataene finnes i både Finans og Kostnadsregnskap. Denne overflødigheten er nødvendig, fordi du kan bruke Økonomistyring for ekstern rapportering og Kostnadsregnskap for intern rapportering.

**Kostnadsregnskapsfinans**

Definert etter kalender-, valuta- og kostnadselementdimensjon, styrer den prosesser og retningslinjer for måling av kostnader. 

**Kostnadsoppføring**

Kostposter er et resultat av en overføring via data koblinger fra finansposter, kostnadsfordelinger og bokførte kostposter i kostkladder.

**Kostnadsobjekt**

Enhver type objekt som er valgt for kostnadskontroll. Kostnader eller inntekter er enten direkte postet på eller allokert til kostnadsobjekter. Noen typiske kostnadsobjekter er:

-  Produkter
-  Prosjekter
-  Avdelinger
-  Kostsentre

Ledelsen bruker kostnadsobjekter til å kvantifisere kostnader, men også til å utføre fortjenesteanalyse.

**Kostnadselement**

Brukes som en funksjon for å spore og kategorisere kostnader. Det er to typer kostnadselementer: primær og sekundær.

Primære kostnadselementer representerer kostnadsstrømmen fra finansiell regnskap til kostnadsregnskap. Strukturen svarer typisk til resultatregnskapsstrukturen i hovedboken hvor et kostnadselement kan tilsvare en hovedkonto. Ikke alle hovedkontoer må nødvendigvis vises som kostnadselementer, avhengig av forretningskravene. 

Sekundære kostnadselementer representerer den interne kostnadsstrømmen fordi disse kostnadene kun brukes i kostnadsregnskap. De brukes i kostnadsopprullingen for å samle kostnader i meningsfulle grupper som brukes av overheadberegning. 

**Kostnadsklassifisering**

Kostnadsklassifisering grupperer kostnader i henhold til felles egenskaper. Kostnader kan for eksempel grupperes etter elementer, sporbarhet og atferd.

-   **Etter elementer** – materialer, arbeid og utgifter.
-   **Etter sporbarhet** – direkte og indirekte kostnader. Direktekostnader tilordnes direkte til kostobjekter. Indirekte kostnader kan ikke spores direkte til kostobjekter. Indirekte kost fordeles til kostobjekter.
-   **Etter atferd** – faste, variable og delvis variable.

**Kostnadsatferd**

Kostnadsatferd klassifiserer kostnader i henhold til atferden i forhold til endringer i viktige aktiviteter. Hvis du vil angi kostnader effektivt, må ledelsen forstår kostnadsatferden. Det finnes tre typer kostnadsatferdsmønster: faste, variable og delvis variable.

- **Fast kostnad** – En fast kostnad som har en kostnad som ikke variere på kort sikt, uavhengig av endringer i nivå for aktiviteten. Faste kostnader kan for eksempel være en grunnleggende operative utgifter i en virksomhet, for eksempel husleie, som ikke vil bli påvirket selv om aktivitetsnivået øker eller minker.

- **Variabel kostnad** – Variable kostnader endres i takt med endringer i nivå for aktiviteten. For eksempel er en bestemt direkte materialer kostnad knyttet til hver vare som selges. Jo flere produkter som selges, jo høyere direkte materialkostnader er det.

- **Delvis variabel kostnad** – Delvis variable kostnader er delvis faste og delvis variable kostnader. Et Internett-tilgangsgebyr omfatter for eksempel en standard månedsavgift for tilgang og et gebyr for bredbåndsbruk. Standard månedsgebyr er en fast kostnad, mens bredbåndsbrukgebyret er en variabel kostnad.

**Kostnadskontrollenhet**

Kostnadskontrollenheten representerer kostnadsstrukturen. Strukturen bestemmer hvordan kostnadene flyter i en hierarkisk rekkefølge mellom kostnadsobjektdimensjoner og deres respektive kostnadsobjekter. 

**Kostnadsdistribusjon**

Brukes til å distribuere kostnad fra ett kostnadsobjekt til en eller flere andre kostnadsobjekter ved å bruke en relevant allokeringsbase. Kostnadsfordeling og kostnadallokering er forskjellig, fordi kostnadsfordeling alltid skjer på nivået av primærkostningselementet til den opprinnelige kostnaden, og ingen gjensidig behandling.

**Kostnadsfordelinger**

Brukes til å allokere balansen til et kostnadsobjekt til andre kostnadsobjekter ved å bruke en allokeringsbase. Finance and Operations støtter gjensidig tildelingsmetode. I den gjensidige tildelingsmetoden gjenkjennes fullstendig de gjensidige tjenestene som hjelpekostnadsobjekter utveksler. Systemet bestemmer automatisk rekkefølgen for å utføre tildelingene i og gjenta over den. Saldoen på et kostnadsobjekt tildeles av ett enkelt tildelingsgrunnlag. Allokeringer på tvers av kostnadosbjektdimensjoner og deres respektive medlemmer støttes. Tildelingsrekkefølgen styres av kostnadskontrollenheten.

**Kostnadsfordelingspolicy**

En policy for fordeling av kostnad definerer beløp og antall som må fordeles. Fordelingsregler inkluderer kildefordelingsregler, som bestemmer kostnadene som fordeles, og fordelingsmålregler, som bestemmer hvor kostnadene fordeles. Alle kostnader for lokale tjenester er for eksempel en fordelingskilde som kan fordeles på ulike avdelinger i en organisasjon (det vil si til fordelingsmål).

**Kostnadsopprulling**

Formålet med kostnadsopprulling er å aggregere kostnader i meningsfulle grupper. Nivået for aggregering er brukerdefinert og involverer tildelinger av sekundære kostnadselementer. Hvis kostnadsopprulling ikke brukes vil hvert element for en kostnad allokeres fra et kostnadsobjekt til et annet

**Policy for kostnadssats**

Kostnadssatsen brukes til å beregne prisen per kostobjekt. Hvis du vil forstå elementene i prisen, kan du definere policyer for kostnadssats. Det finnes to typer kostnadssats: historisk kostnadssats og planlagt kostnadssats. En historisk kostnadssats er en beregnet sats som skal brukes som en multiplikator for fordelingsgrunnlaget for et kostobjekt. Satsen beregnes basert på kostfordelingene i forrige periode. En planlagt sats er en brukerdefinert sats.

**Dimensjonshierarki**

Det finnes to dimensjonshierarkier: kategoriseringshierarki og klassifiseringshierarki. Dimensjonskategoriseringshierarkiet brukes for rapportformål. Det støtter bare kostnadselementdimensjonene. Dimensjonsklassifiseringshierarkiet brukes for å definere policyer og for rapportformål. Det støtter alle dimensjoner, for eksempel kostnadsobjekter, kostnadselementer og statistiske dimensjoner. 

**Datakobling**

Kostnadsregnskapet støtter integrering av data fra kildesystemer via et sett med datakoblinger. Følgende datakoblinger er tilgjengelige:

-  Importerte transaksjoner (forhåndskonfigurert)
-  Dynamics 365 for Finance and Operations (forhåndskonfigurert)
-  Dynamics AX (konfigurasjon kreves)

**Merk:** Datatilkoblingens importerte transaksjoner er basert på dataenheter.

**Dataleverandør**

De fleste kildesystemer kan gi data som samsvarer med en eller flere datakilder i kostnadsregnskap. For å justere data fra kildesystemene med datakilden i Kostnadsregnskap, må en dataoperatør konfigureres. Tabellen nedenfor viser tilgjengeligheten av dataleverandører per datakontakt og datakilde.

|  **Datakilder** |  **Datakilder for importerte transaksjoner** | **Datakobling for Dynamics 365 for Finance and Operations**  | **Datatilkobling for Dynamics AX**  |
|---|---|---|---|
| Medlemmer av dimensjon for kostnadselement  |  Ja | Ja  | Ja  |
|  Medlemmer av dimensjon for kostnadsobjekt |  Ja | Ja  | Ja  |
|  Statistiske medlemmer av dimensjon | Ja  | Antall  | Antall  |
|  Økonomimodul | Ja  | Ja  | Ja  |
|  Budsjettoppføringer  | Ja  | Ja  | Ja  |
|  Statistiske målinger | Ja  | Ja  | Ja  |

**Formel**

Formeltildelingsgrunnlag lar deg definere avanserte formler for å oppnå det riktige tildelingsgrunnlaget. Du kan opprette formeltildelingsgrunnlag manuelt. Du kan bruke følgende operatorer til å definere formelen.

|  **Symboler** | **Tekst**  |
|---|---|
|  ( ) | Parenteser  |
|  < |  Mindre enn |
|  > |  Større enn |
|  + |  Tillegg |
|  – |  Subtraksjon |
| *  | Multiplikasjon  |

Tradisjonelle IF-setninger støttes ikke. Du kan imidlertid lage setninger og validere om de er sanne.

|  **Setningsvalidering** | **Resultat**  |
|---|---|
|  a > b| Sann  |
|  a > b |  Usann |

**Administrasjonskostnad**

Indirekte kostnader refererer til de pågående utgiftene for drift av en virksomhet. De er kostnader som ikke kan kobles direkte til bestemte aktiviteter. Her er noen eksempler på indirekte kostnader:

-   Regnskapsgebyrer
-   Avskrivninger
-   Forsikring
-   Interesser
-   Juridiske gebyrer
-   Avgifter
-   Verktøykostnader

**Overhead-sats**

Satsene er definert per kostnadsobjekt og kostnadselement. Det finnes to typer satser: finansiell periode og bruker-spesifisert. Finansiell periodesatser kalkuleres av overhead-kalkulering. En bruker-spesifisert sats er brukerdefinert og kan brukes til å allokere kostnader mellom kostnadsobjekter på en forhåndsbestemt sats i overhead-kalkulering.

**Publisert**

Hvis du setter dette feltet til Ja vil en brukes som er tildelt en av følgende roller kunne se rapporten i arbeidsområdet Kostnadskontroll:

-  Behandling av kostnadsregn
-  Regnskapsfører lager
-  Assisterende lagerregnskapsfører
-  Kontroller for kostnadsobjekt

Hvis du setter dette feltet til Nei, kan kun brukere som er tildelt en av følgende roller se og rapportere i arbeidsområdet Kostnadskontroll:

-  Behandling av kostnadsregn
-  Regnskapsfører lager
-  Assisterende lagerregnskapsfører

**Statistisk dimensjon**

En statistisk dimensjon og medlemmene av denne brukes til å registrere og kontrollere ikke-monetære oppføringer i kostnadsregnskap. Statistiske dimensjonsmedlemmer kan brukes til to formål:

-  Som en fordelingsbase i policyer som kostnadsfordeling eller kostnadsallokering.
-  For rapportering av ikke-monetært forbruk.

En statistisk dimensjon er uttrykket av en telling eller sum av en aktivitet som kan brukes som grunnlag for tildelinger eller renteberegninger. Den opprettes manuelt eller importeres fra kildesystemer. Eksempler på statistiske dimensjoner er antall ansatte, antall lisensiert programvare på hver enhet, strømforbruket til hver maskin, eller kvadratmeter for et kostsenter.

**Utdrag**

Oppgaver er visninger for ledere som har ansvar for å kontrollere kostnader. Utdrag er definert av en kostnadsregulator, og de gir en rask oversikt over faktiske kostnader, budsjetterte kostnader og avvik. En leder kan bore videre til detaljer om nødvendig. For å sikre at ledere kun ser på data som de er ansvarlige for, er data som vises i uttalelsene underlagt regler for tilgang.

**Versjon**

Versjoner brukes til å simulere, vise og sammenligne ulike resultater. Som standard vises alle faktiske kostnader i en grunnleggende versjon som kalles *Faktiske*. Du kan arbeide med så mange versjoner du har behov, for budsjetter og beregninger. Du kan for eksempel importere budsjettdata til en opprinnelig versjon og deretter endre budsjettet i en revidert versjon. For beregninger kan du opprette flere versjoner. I disse ulike versjonene kan du deretter opprette beregninger ved hjelp av andre beregningsregler som skal brukes for kostnadsfordeling.



