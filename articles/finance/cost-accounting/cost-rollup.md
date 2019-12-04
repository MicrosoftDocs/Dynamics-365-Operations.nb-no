---
title: Policy for opprullet kost og beregning av administrasjonskostnader
description: Dette emnet inneholder informasjon om hvordan du fastsetter riktig nivå for sekundære kostnadselementer og lager regler for opprullet kost som passer inn i organisasjonsrapportering og kostnadssporbarhet.
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostRollupRule, CAMDimensionHierarchy
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 083b6cb604115c3f2a72a5ba23199e1517fc1ea1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771907"
---
# <a name="cost-rollup-policy-and-overhead-calculation"></a>Policy for opprullet kost og beregning av administrasjonskostnader 

[!include [banner](../includes/banner.md)]

Kostnadsregnskap gir deg innsikt i hvordan kostnadsflyten er knyttet til produktene og tjenestene som leveres i en organisasjon. Hvis du vil se kostnadsgjennomsiktigheten, er det avgjørende å oppnå kostnadsfordeling mellom kostnadsobjekter basert på et passende tildelingsgrunnlag. Kostnadsfordelingen oppnås som standard for det primære kostnadselementet, som er ønskelig i noen tilfeller, men det har enkelte implikasjoner som må vurderes.

-   Hjelpekostnadsobjekter slutter med null i saldo for det primære kostnadselementet etter beregning av indirekte kostnader.

-   Antallet kostnadsoppføringer som genereres ved beregning av indirekte kostnader, kan være svært høyt.

-   Det går ikke an å spore kostnadsflyten mellom kostnadsobjekter.

Kostnadsregnskap lar deg konfigurere kostnadsfordeling slik at den passer med rapporteringskravene i organisasjonen, og dermed unngår du disse implikasjonene. Dette emnet diskuterer hvordan du kan fastsette riktig nivå for sekundære kostnadselementer og lage regler for opprullet kost som passer inn i organisasjonsrapportering og kostnadssporbarhet.

> [!NOTE]
> Du kan endre konfigurasjoner hvis rapporteringskravene endres.

## <a name="example-of-cost-rollup-policy-setup"></a>Eksempel på oppsett av policy for opprullet kost

La oss si at en organisasjon har følgende struktur med fire kostsentre.

![Eksempel på en organisasjonsstruktur](./media/dimension-hierarchy-org.png)

**Kostnadsobjektdimensjon**

| Kostsentre | beskrivelse          |
|--------------|-----------|
| CC001        | Personale        |
| CC002        | Finans   |
| CC003        | Samling  |
| CC004        | Innpakning |

**Kostnadselementdimensjon**

| Kostnadselementer | beskrivelse | Type    |
|---------------|-------------|---------|
| 1001          | Strøm | Primær |
| 1 002          | Lønn    | Primær |
| 1003          | Reklame | Primær |

Et dimensjonshierarki som oppfyller organisasjonens rapporteringskrav, kan defineres som følger.

**Detaljer for dimensjonshierarki**

| Dimensjonshierarkinavn | Dimensjon    | Navn på dimensjonshierarkitype      | Hierarki for tilgangsliste |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisasjon             | Kostsentre | Hierarki for dimensjonsklassifisering | Ingen                    |

**Dimensjonshierarki**

|              | Dimensjonsmedlemsområder |                     |
|--------------|-------------------------|---------------------|
| **Noder**        | **Fra dimensjonsmedlem**   | **Til dimensjonsmedlem** |
| Organisasjon |                         |                     |
| &nbsp;&nbsp;Administrator             |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Finans              | CC001                   | CC001               |
| &nbsp;&nbsp;&nbsp;&nbsp;Personale               | CC002                   | CC002               |
| &nbsp;&nbsp;Produksjon               |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Innpakning              | CC003                   | CC003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Samling             | CC004                   | CC004               |

Et dimensjonshierarki som oppfyller policykravene, kan defineres som følger.

**Detaljer for dimensjonshierarki**

| Dimensjonshierarkinavn | Dimensjon     | Navn på dimensjonshierarkitype      |
|--------------------------|---------------|------------------------------------|
| Resultatregnskap  | Kostnadselementer | Hierarki for dimensjonsklassifisering |

**Dimensjonshierarki**

|                         | Dimensjonsmedlemsområder |                     |
|-------------------------|-------------------------|---------------------|
| Noder                   | Fra dimensjonsmedlem   | Til dimensjonsmedlem |
| Resultatregnskap |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Primær kostnad                    | 10001                   | 10003               |

Etter at økonomimoduloppføringene er behandlet, ser kostnadsoppføringssaldoen etter kostnadsobjekt slik ut.

|                      | **Kostnadsobjekt** |           |           |           | **Total**     |
|----------------------|-----------------|-----------|-----------|-----------|---------------|
| **Kostnadselement**     | **CC001**       | **CC002** | **CC003** | **CC004** |               |
| **1001 Strøm** | 100,00          | 200 00    | 6.000,00  | 2.000,00  | **8.300,00**  |
| **1002 Lønn**    | 10.000,00       | 10.000,00 | 8.000,00  | 6.500,00  | **34.500,00** |
| **1003 Reklame** | 0,00            | 4.000,00  | 0,00      | 0,00      | **4.000,00**  |
|                      | 10.100,00       | 14.200,00 | 14.000,00 | 8.500,00  | **46.800,00** |

**Statistisk dimensjon**

| Statistiske elementer |    beskrivelse   |
|----------------------|------------------|
| SE-1                 | Personaletjenester      |
| SE-2                 | Finanstjenester |

Kostnadsobjekt CC001 Personale bidrar med Personaletjenester til flere kostnadsobjekter.

Personaletjenester forbrukes av følgende distribusjon av størrelse.

| Kostnadsobjekt | beskrivelse |   Personaletjenester |
|-------------|-------------|----|
| CC002       | Finans     | 35 |
| CC003       | Samling    | 55 |
| CC004       | Innpakning   | 10 |

Kostnadsobjekt CC002 Finans bidrar til flere kostnadsobjekter.

Finanstjenester forbrukes av følgende distribusjon av størrelse.

| Kostnadsobjekt |   beskrivelse    |  Finanstjenester   |
|-------------|------------------|----|
| CC003       | Samling         | 65 |
| CC004       | Innpakning        | 35 |

Kostnadsfordelingspolicyer kan defineres som følger.

| Policynavn | beskrivelse     | Dimensjonsobjekt for kostnadselement | Statistisk dimensjon | Kostnadselementdimensjon |
|-------------|-----------------|---------------------------------|-----------------------|------------------------|
| 2017        | Kostnadsavregninger | Organisasjon                    | Statistiske elementer  | Kostnadselementer          |

Regler for kostnadsfordeling kan defineres som følger.

| Dimensjonshierarkihode for kostnadsobjekt | Kostnadsatferd | Tildelingsgrunnlag        |
|--------------------------------------|---------------|------------------------|
| CC001                                | Sum         | **Personaletjenester**        |
| CC002                                | Sum         | **Finanstjenester** |

<a name="brhow-cost-flows-between-cost-centers"></a><br>Hvordan kostnad flyter mellom kostsentre 
---------------------------------------------------

Hvis du vil vite hvordan kostnad flyter mellom kostsentrene i organisasjonen, kan du opprette kostnadselementer av typen **Sekundær** for hvert kostsenter. Disse kostnadselementene brukes deretter til å overføre saldoer mellom kostsentrene under beregningen av indirekte kostnader.

Medlemmer av dimensjon for kostnadselement kan defineres som følger.

| Kostnadselementer | Type          |               |
|---------------|---------------|---------------|
| 1001          | Strøm   | Primær       |
| 1 002          | Lønn      | Primær       |
| 1003          | Reklame   | Primær       |
| **SC-CC001**  | **Personale**        | **Sekundær** |
| **SC-CC002**  | **Finans**   | **Sekundær** |
| **SC-CC003**  | **Samling**  | **Sekundær** |
| **SC-CC004**  | **Innpakning** | **Sekundær** |

Dimensjonshierarkiet **Resultatregnskap** må oppdateres med de nye dimensjonsmedlemmene, slik at dimensjonshierarkiet inneholder riktige data som kan brukes til å definere rapportering og policyer.

**Detaljer for dimensjonshierarki**

| Dimensjonshierarkinavn | Dimensjon     | Navn på dimensjonshierarkitype      |
|--------------------------|---------------|------------------------------------|
| Resultatregnskap  | Kostnadselementer | Hierarki for dimensjonsklassifisering |

**Dimensjonshierarki**

|                         | Dimensjonsmedlemsområder |                     |
|-------------------------|-------------------------|---------------------|
| Noder                   | Fra dimensjonsmedlem   | Til dimensjonsmedlem |
| Resultatregnskap |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Primær kostnad                        | 10001                   | 10003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Sekundær kostnad                         | **SC-CC001**            | **SC-CC004**        |

Opprett en **Policy for opprullet kost** der hvert kostsenter er tilordnet til et tilsvarende kostnadselement av typen **Sekundær**.

**Policyer for opprullet kost**

| Policynavn | beskrivelse | Dimensjonsobjekt for kostnadselement | Dimensjonshierarki for kostnadselement |
|-------------|-------------|---------------------------------|----------------------------------|
| 2017        | Kostnadsflyt   | Organisasjon                    | Resultatregnskap          |

**Regler for opprullet kost**

| Dimensjonshierarkihode for kostnadsobjekt | Dimensjonshierarkihode for kostnadselement | Sekundært kostnadselement |
|--------------------------------------|---------------------------------------|------------------------|
| CC001                                | Resultatregnskap               | **SC-CC001**           |
| CC002                                | Resultatregnskap               | **SC-CC002**           |
| CC003                                | Resultatregnskap               | **SC-CC003**           |
| CC004                                | Resultatregnskap               | **SC-CC004**           |

## <a name="perform-overhead-calculation"></a>Beregn indirekte kostnader

**Journalen**

| Journalen | Journaltype            | Økonomisk kalenderperiode | År | Periode | Versjon       |
|---------|-------------------------|------------------------|------|--------|---------------|
| 00002   | Kostfordelingsjournal | Skattemessig                 | 2017    | Periode 1 | Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1 |

Systemet bruker nå **Policy for opprullet kost** når det oppretter **Journaloppføringer for kostnadsobjektsaldo**.

**Journaloppføringer for kostnadsobjektsaldo**

| Regnskapsdato | Kostnadsobjekt | beskrivelse  | Kostnadselement | beskrivelse |  Beløp |
|-----------------|-------------|--------------|----------|-----------|-----------|
| 31.01.2017      | CC001       | Personale           | SC-CC001 | Personale        | 10.100,00 |
| 31.01.2017      | CC002       | Finans      | SC-CC002 | Finans   | 17.735,00 |
| 31.01.2017      | CC003       | Samling     | SC-CC003 | Samling  | 31.082,75 |
| 31.01.2017      | CC004       | Innpakning    | SC-CC004 | Innpakning | 15.717,25 |

> [!NOTE]
> Journaloppføringene opprettes basert på reglene i **Policy for opprullet kost**, hvis det finnes en policy. Saldoen som vises, er saldoen for beregningen av indirekte kostnader.

Siden **Detaljer om journaloppføring for kostnadssaldo for kostnadsobjekt** som åpnes fra journaloppføringene, viser hvordan saldoen innhentes.

**Eksempel: Journaloppføringen for kostnadsobjekt CC002 Finans**

**Detaljer om journaloppføring for kostnadssaldo for kostnadsobjekt**

| Medlem av dimensjon for kostnadselement | beskrivelse |  Beløp   |
|-------------------------------|-------------|-----------|
| 1001                          | Strøm | 200 00    |
| 1 002                          | Lønn    | 10.000,00 |
| 1003                          | Reklame | 4.000,00  |
| SC-CC001                      | Personale          | 3.535,00  |

**Kostnadsoppføringer generert av beregningen av indirekte kostnader**

| Kostnadsobjekt | beskrivelse  | Kostnadselement   | beskrivelse  |        Beløp     |       Regnskapsdato     |
|-------------|--------------|----------|-----------------|-------------|------------|
| CC001       | Personale           | SC-CC001 | Personale              | 10.100,00. \- | 31.01.2017 |
| CC002       | Finans      | SC-CC001 | Personale              | 3.535,00    | 31.01.2017 |
| CC003       | Samling     | SC-CC001 | Personale              | 5.555,00    | 31.01.2017 |
| CC004       | Innpakning    | SC-CC001 | Personale              | 1.010,00    | 31.01.2017 |
| CC002       | Finans      | SC-CC002 | Finans         | 17.735,00. \- | 31.01.2017 |
| CC003       | Samling     | SC-CC002 | Finans         | 11.527,75   | 31.01.2017 |
| CC004       | Innpakning    | SC-CC002 | Finans         | 6.207,25    | 31.01.2017 |

Etter at **Beregning av indirekte kostnader** er fullført, kan du rapportere resultatene ved hjelp av verktøy som Microsoft SharePoint Workspace, Excel eller Power BI.

## <a name="view-reporting-in-excel"></a>Vise rapportering i Excel 

Dimensjonshierarkiene gjør at du kan vise dataene på ulike aggregeringsnivåer.

Her er et eksempel på Power Pivot-rapportering i Excel.

| **Resultatregnskap** | **Kostnadsobjekt** |                |               |               |  **Sum**    |
|-----------------------------|-----------------|----------------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002**      | **CC003**     | **CC004**     |               |
| **Primær kostnad**            | **10.100,00**   | **14.200,00**  | **14.000,00** | **8.500,00**  | **46.800,00** |
| 1001. &nbsp;&nbsp;&nbsp;&nbsp;                            | 100,00          | 200 00         | 6.000,00      | 2.000,00      | **8.300,00**  |
| 1002. &nbsp;&nbsp;&nbsp;&nbsp;                            | 10.000,00       | 10.000,00      | 8.000,00      | 6.500,00      | **34.500,00** |
|1003. &nbsp;&nbsp;&nbsp;&nbsp;                             | 0,00            | 4.000,00       | 0,00          | 0,00          | **4.000,00**  |
|**Sekundær kostnad**                            | **-10.100,00**  | **-14.200,00** | **17.082,75** | **7.217,25**  | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC001                            | 10.100,00. \-     | 3.535,00       | 5.555,00      | 1.010,00      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC002                             | 0,00            | 17.735,00. \-    | 11.527,75     | 6.207,25      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC003                            | 0,00            | 0,00           | 0,00          | 0,00          | 0,00          |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC004                             | 0,00            | 0,00           | 0,00          | 0,00          | 0,00          |
| **Total**                   | **0,00**        | **0,00**       | **31.082,75** | **15.717,25** | **46.800,00** |

Du kan bruke **Policy for opprullet kost** og **Kostnadselementer av typen sekundær** til å la den primære kostnaden per kostnadsobjekt for intern rapportering være den primære kostnaden som gjenstår etter **Beregning av indirekte kostnader**.

Hvis det samme eksemplet hadde blitt utført uten å opprette **Policy for opprullet kost**, hadde rapportresultatet blitt vist som nedenfor. Kostnaden flyter riktig, men sporbarheten og innsikten i hvordan kostnaden flyter mellom kostsentrene, går tapt.

| **Resultatregnskap** | **Kostnadsobjekt** |           |               |               |          **Total**  |
|-----------------------------|-----------------|-----------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002** | **CC003**     | **CC004**     |               |
| **Primær kostnad**            | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |
|1001. &nbsp;&nbsp;&nbsp;&nbsp;                              | 0,00            | 0,00      | 6.207,75      | 2.092,25      | **8.300,00**  |
| 1002. &nbsp;&nbsp;&nbsp;&nbsp;                             | 0,00            | 0,00      | 22.275,00     | 12.225,00     | **34.500,00** |
|1003. &nbsp;&nbsp;&nbsp;&nbsp;                              | 0,00            | 0,00      | 2600,00       | 1.400,00      | **4.000,00**  |
|**Sekundær kostnad**                            | **0,00**        | **0,00**  | **0,00**      | **0,00**      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC001                             | 0,00            | 0,00      | 0,00          | 0,00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC002                             | 0,00            | 0,00      | 0,00          | 0,00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC003                             | 0,00            | 0,00      | 0,00          | 0,00          | 0,00          |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC004                             | 0,00            | 0,00      | 0,00          | 0,00          | 0,00          |
| **Total**                   | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |

Avhengig av kravene til rapportering og sporbarhet i organisasjonen kan du fastsette riktig nivå for sekundære kostnadselementer og lage regler for opprullet kost som passer behovene dine.

Det klare skillet mellom **Kostnadsfordelinger** og **Policyer for opprullet kost** gir deg fleksibiliteten til å gjøre kontinuerlige oppdateringer uten at de påvirker hverandre.



## <a name="additional-resources"></a>Tilleggsressurser
-  [Dimensjoner for kostnadsobjekt](cost-objects.md)
-  [Kostnadselementdimensjoner](cost-elements.md)
-  [Dimensjonshierarki](dimension-hierarchy.md)
-  [Beregning av indirekte kostnader](overhead-calculation.md)
