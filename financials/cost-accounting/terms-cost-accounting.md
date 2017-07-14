---
title: Terminologi for kostnadsregnskap
description: Dette emnet beskriver de viktigste begrepene som brukes i Kostnadsregnskap.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMCostControlWorkspaceConfiguration
audience: Application User
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 35b8e510e7e2c13aebb73f46d20b16275d097432
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017


---

# Terminologi for kostnadsregnskap
<a id="cost-accounting-terminology" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Dette emnet beskriver de viktigste begrepene som brukes i Kostnadsregnskap.

**Kostnadsregnskap**

Med Kostnadsregnskap kan du samle inn data fra forskjellige kilder, for eksempel i økonomimodulen, underfinans, budsjetter og statistisk informasjon. Deretter kan du analysere, summere og evaluere kostnadsdata, slik at ledelsen kan gjøre best mulig avgjørelsene for prisoppdateringer, budsjetter, kostnadskontroll og så videre. Kildedataene som brukes til å foreta kostnadsanalyser, behandles uavhengig av hverandre i Kostnadsregnskap. Oppdateringer i Kostnadsregnskap påvirker derfor ikke kildedataene. Når du samler inn kostnadsdata fra forskjellige kilder, og særlig når du importerer hovedkontoene fra Microsoft Dynamics 365 for Finance and Operations, Enterprise edition som kostnadselementer, er det imidlertid overflødige data, fordi de samme dataene som finnes i både Finans og Kostnadsregnskap. Denne overflødigheten er nødvendig, fordi du kan bruke Økonomistyring for ekstern rapportering og Kostnadsregnskap for intern rapportering.

**Kostnadsregnskapsfinans**

Kostnadsregnskapsfinansen er et spesialisert rammeverk som bestemmer hvordan prosesser, verdier og antall som er angitt og presenteres for et bestemt område i Kostnadsregnskap. Kostnadsregnskapsfinansen definerer prosesser og regler for å måle kostnadene på kostobjekter. Den håndterer kostnadstransaksjoner, og administrerer dokumenter som kan registrerer endringer i verdier og antall som kostnadstransaksjoner produserer.

**Kostnadsoppføring**

Kostposter er et resultat av en overføring via data koblinger fra finansposter, kostnadsfordelinger og bokførte kostposter i kostkladder.

**Kostnadsobjekt**

Kostnadsobjekter er en hvilken som helst type objekt som kostnadene tildeles til. Her er noen vanlige objekter:

-   Produkter
-   Prosjekter
-   Ressurser
-   Avdelinger
-   Kostsentre
-   Geografiske områder

Ledelsen bruker kostnadsobjekter til å kvantifisere kostnader, men også til å utføre fortjenesteanalyse.

**Kostnadselement**

Kostnadselementer brukes til å spore og kategorisere der kostnadene flyter til. Det finnes to typer kostnadselementer: primærkostnader og sekundærkostnader. **Primærkostnader** De primære kostnadselementer representerer kostflyten fra finansbokføring til kostnadsregnskap. Kostnadselementstrukturen tilsvarer kontostrukturen for resultat i økonomimodulen, der en kostnadselement kan tilsvare en hovedkonto. Ikke alle hovedkontoer må nødvendigvis vises som kostnadselementer, avhengig av forretningskravene. Her er noen eksempler på primærkostnadselementer:

-   Solgte varers kost (COG-er)
-   Indirekte materialkostnader
-   Personalkostnader
-   Energikostnader

**Sekundært kostnadselement** 

Sekundære kostnadselementer representerer kostflyten internt fordi disse kostnadene opprettes og brukes bare i Kostnadsregnskap. Sekundærkostnadselementer bidrar til å garantere at kilden til kostnadene kan spores. Disse kostnadselementene brukes i kostnadsfordelinger og beregninger for indirekte kostnader. Her er noen eksempler på sekundærkostnadselementer:

-   Produksjonskostnader
-   Indirekte kostnader for produksjon, material og markedsføring

**Kostnadskontrollenhet**

En kostnadskontrollenhet representerer kostnadsstrukturen. Den må være knyttet til kostnadsobjektdimensjoner i en kostnadsregnskapsfinans.

**Versjon**

Versjoner brukes til å simulere, vise og sammenligne ulike resultater. Som standard vises alle faktiske kostnader i en grunnleggende versjon som kalles *Faktiske*. Du kan arbeide med så mange versjoner du har behov, for budsjetter og beregninger. Du kan for eksempel importere budsjettdata til en opprinnelig versjon og deretter endre budsjettet i en revidert versjon. For beregninger kan du opprette flere versjoner. I disse ulike versjonene kan du deretter opprette beregninger ved hjelp av andre beregningsregler som skal brukes for kostnadsfordeling.

**Utdrag**

Oppgaver er visninger for ledere som har ansvar for å kontrollere kostnader. Oppgaver defineres av en kostnadskontroller, og de gir et raskt overblikk over faktiske og budsjetterte kostnader, og i tillegg avvik og beregningsversjoner. For å garantere at ledere bare viser data de er ansvarlige for, er dataene som vises i oppgjør, underlagt tilgangsreglene.

**Datakobling**

Dataene kan importeres til Kostnadsregnskap fra eksterne systemer via datakoblinger. Du kan for eksempel importere kontostrukturer, dimensjoner, finansposter og budsjettposter. Du kan bruke forhåndskonfigurerte datakoblinger eller egendefinerte koblinger til å importere data og opprette datatilkoblinger.

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

**Administrasjonskostnad**

Indirekte kostnader refererer til de pågående utgiftene for drift av en virksomhet. De er kostnader som ikke kan kobles direkte til bestemte aktiviteter. Her er noen eksempler på indirekte kostnader:

-   Regnskapsgebyrer
-   Avskrivninger
-   Forsikring
-   Interesser
-   Juridiske gebyrer
-   Avgifter
-   Verktøykostnader

**Kostnadsfordelinger**

Kostnadsfordeling er prosessen med å tilordne og fordele kostnader, basert på roten årsakene til de vanlige kostnadene. Du tildeler kostnader og antall fra ett kostobjekt til én eller flere kostobjekter. Kostnader for alle lokale tjenester blir for eksempel tilordnet til de ulike avdelingene som bruker det vanlige kontorbygget.

**Kostnadsfordelingspolicy**

En policy for fordeling av kostnad definerer beløp og antall som må fordeles. Fordelingsregler inkluderer kildefordelingsregler, som bestemmer kostnadene som fordeles, og fordelingsmålregler, som bestemmer hvor kostnadene fordeles. Alle kostnader for lokale tjenester er for eksempel en fordelingskilde som kan fordeles på ulike avdelinger i en organisasjon (det vil si til fordelingsmål).

**Tildelingsgrunnlag**

Fordelingen er grunnlaget som kan brukes til å måle og telle aktiviteter, for eksempel maskindriftstid som brukes, kilowatt timer som er brukt, direkte arbeidstimene som er brukt eller kvadratmeter som er tatt i bruk. Den brukes til å fordele kostnader til ett eller flere kostobjekter.

**Tildelingsprinsipp**

Ett av fordelingsprinsippene er å fordele kostnader etter kostnadssats. Du kan velge å fordele kostnader ved hjelp av den faktiske periodesatsen eller en historisk sats. Fordeling som bruker den gjensidige metoden, bidrar til å sikre at fordelingsgrunnlaget bestemmes av en serie med samtidige formler før fordeling utføres ved hjelp av den faktiske periodesatsen.

**Kostnadsopprulling**

Formålet med kostnadsopprulling er å inkludere alle kostnader for et gitt kostobjekt. Samlingsnivået er brukerdefinert. Ved hjelp av kostnadsopprulling kan du samle elementer av kostnader som må fordeles fra ett kostobjekt til et annet. Når kostnadsopprulling ikke er i bruk, fordeles hvert element med kostnader fra ett kostobjekt til et annet.

**Policy for kostnadssats**

Kostnadssatsen brukes til å beregne prisen per kostobjekt. Hvis du vil forstå elementene i prisen, kan du definere policyer for kostnadssats. Det finnes to typer kostnadssats: historisk kostnadssats og planlagt kostnadssats. En historisk kostnadssats er en beregnet sats som skal brukes som en multiplikator for fordelingsgrunnlaget for et kostobjekt. Satsen beregnes basert på kostfordelingene i forrige periode. En planlagt sats er en brukerdefinert sats.

**Dimensjonshierarki**

Dimensjonshierarkier brukes som rapporteringsstrukturer når du definerer reglene for fordeling, kostnadssats og kostnadsopprullinger, viser oppgaver eller data i Microsoft Excel, og definerer tilgang til de samlede dataene. Det finnes to dimensjonshierarkier: kategoriseringshierarki og klassifiseringshierarki. Et kategoriseringshierarki defineres basert på kostnadselementer, mens et klassifiseringshierarki defineres basert på kostobjekter.

**Statistisk dimensjon**

En statistisk dimensjon er uttrykket for et antall eller en sum for et objekt som kan brukes som grunnlag for fordelinger eller kostnadssatsberegninger. Den opprettes manuelt eller importeres fra kildesystemer. Eksempler på statistiske dimensjoner er antall ansatte, antall lisensiert programvare på hver enhet, strømforbruket til hver maskin, eller kvadratmeter for et kostsenter.

**Statistisk oppføring**

Statistisk oppføringer inneholder den registrerte summen eller tellingsverdien for en gitt statistisk dimensjon. Den registrerte summen eller tellingsverdien kalles også størrelsen.




