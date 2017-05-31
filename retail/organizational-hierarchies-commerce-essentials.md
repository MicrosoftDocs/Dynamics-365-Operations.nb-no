---
title: Organisasjoner og organisasjonshierarkier (Grunnleggende om handel)
description: "Grunnleggende om handel har tre typer interne organisasjoner som du kan definere for å hjelpe en organisasjon utføre en forretningsprosess eller oppnå et mål."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21251
ms.assetid: 2bfc6bfe-784b-42e8-8bf0-116e9f0a558e
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 17d434f5d49d544003ee7cb862391d88ac5c723a
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="organizations-and-organizational-hierarchies-commerce-essentials"></a>Organisasjoner og organisasjonshierarkier (Grunnleggende om handel)

[!include[banner](includes/banner.md)]


Grunnleggende om handel har tre typer interne organisasjoner som du kan definere for å hjelpe en organisasjon utføre en forretningsprosess eller oppnå et mål. 

En organisasjon er en gruppe personer som samarbeider for å utføre en forretningsprosess eller oppnå et mål. Et organisasjonshierarki representerer relasjonene mellom forretningsenhetene som utgjør organisasjonen.

## <a name="organizations"></a>Organisasjoner
I Grunnleggende om handel kan du definere tre typer interne organisasjoner: juridiske enheter, driftsenheter og team. I Microsoft Dynamics AX er alle interne organisasjoner typer av Part-enheten. Disse organisasjonene bruker derfor en adressebok til å lagre adresser og annen kontaktinformasjon. En part kan være enten en person eller organisasjon og kan tilhøre én eller flere adressebøker.
### <a name="legal-entities"></a>Juridiske enheter

En juridisk enhet er en organisasjon som har en registrert eller lovfestet juridisk struktur. Juridiske enheter kan inngå juridiske kontrakter og er påkrevd for å klargjøre oppgjør som rapporterer om prestasjonen. Et firma er en type juridisk enhet som du kan opprette i Microsoft Dynamics AX, og hver juridisk enhet er tilknyttet en firma-ID. Denne tilknytningen finnes fordi en firma-ID eller DataAreaId brukes i noen datamodeller der firmaer brukes som en grense for datasikkerhet. Brukere har bare tilgang til data for firmaet de er logget på.

### <a name="operating-units"></a>Driftsenheter

En driftsenhet er en organisasjon som brukes til å fordele kontrollen over økonomiske ressurser og driftsprosesser i en virksomhet. Personer i en driftsenhet har plikt til å gjøre mest mulig ut av knappe ressurser, forbedre prosesser og gjøre rede for egen ytelse. I Grunnleggende om handel omfatter driftsenhetstypene kostsentre, forretningsenheter, verdistrømmer, avdelinger og detaljhandelskanaler. Følgende tabell inneholder mer informasjon om hver type driftsenhet.
|                         |                                                                                         |                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Driftsenhetstype** | **Beskrivelse**                                                                         | **Formål**                                                                                                                                 |
| Forretningsenhet           | En delvis uavhengig driftsenhet som er opprettet for å nå strategiske forretningsmål. | Bruk forretningsenheter for finansrapportering som er basert på bransjer eller produktlinjer som organisasjonen leverer på tvers av juridiske enheter. |
| Detaljhandelskanal          | En driftsenhet som representerer en fysisk butikk.                             | Bruk til å administrere og kontrollere én eller flere butikker i eller på tvers av juridiske enheter.                                                               |

## <a name="organizational-hierarchies"></a>Organisasjonshierarkier
I Grunnleggende om handel er hvert hierarki tilordnet til et formål. Formålet med et hierarki bestemmer hvilke organisasjonstyper som kan inkluderes i hierarkiet. Formålet bestemmer også bruksscenariene for hierarkiet. Et hierarki kan for eksempel brukes til å kjøpe og selge produkter i detaljhandelen. Organisasjoner i et hierarki kan dele parametere, policyer og transaksjoner. En organisasjon kan arve eller overstyre parameterne for den overordnede organisasjonen. Delte hoveddata, for eksempel produkter og adressebøker, gjelder imidlertid for hele organisasjonen og kan ikke overstyres for individuelle organisasjoner.
### <a name="best-practices-for-setting-up-an-organization-in-a-hierarchy"></a>Anbefalte fremgangsmåter for å konfigurere en organisasjon i et hierarki

Vurder følgende anbefalte fremgangsmåter når du implementerer et organisasjonshierarki:
-   Opprett en avdeling for å angi skjæringspunktet mellom en juridisk enhet og en forretningsenhet. Du kan deretter rulle opp data fra en avdeling for en juridisk enhet for lovbestemt rapportering og fra en avdeling til en forretningsenhet for intern rapportering.
-   Ikke definer flere hierarkier for samme hierarkiformål i én juridisk enhet.
-   Ikke opprett et hierarki for hvert formål. Vanligvis kan du bruke ett hierarki til flere formål. Ett hierarki av driftsenheter kan for eksempel tilordnes til alle policy-relaterte formål.
-   Opprett balanserte hierarkier. Alle noder som har samme avstand fra rotnoden i et hierarki, defineres som et nivå. Bare én type driftsenhet kan forekomme på hvert nivå i et balansert hierarki, og avstanden fra rotnoden til hvert nivå er ensartet. Hvis det er mellomnivåer mellom en avdeling og en juridisk enhet eller en forretningsenhet, må kanskje plassholderorganisasjoner opprette et balansert hierarki.
-   Ikke utform et eget hierarki av driftsenheter hvis strukturen for juridiske enheter også er driftsstrukturen. En blandet hierarki av juridiske enhetenr og driftsenheter kan brukes til begge formål.
-   Før du definerer store omstruktureringsscenarier, bruker du hierarkiets gyldighetsdatoer til å foreta en konsekvensanalyse og en valideringstest.
-   Lagre et hierarki som et utkast hvis du kanskje vil endre et hierarki før du publiserer det.
-   Begrense antall personer som har tillatelse til å legge til eller fjern organisasjoner fra et hierarki i et produksjonsmiljø. Et mindre antall reduserer sjansen for at kostbare feil kan oppstå, og at det må gjøres rettelser.

## <a name="retail-store-management"></a>Administrasjon av detaljhandelsbutikk
Tabellen nedenfor beskriver scenariene for Grunnleggende om handel hvor organisasjonshierarkier kan brukes.
| Oppgave                                                                           | Beskrivelse                                                                                                                                                                                                                                                                                                | Hierarkiformål    |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| Behandle detaljhandelssortimenter                                                      | Identifisere produktene som er tilgjengelige i hver detaljhandelsbutikk.                                                                                                                                                                                                                                             | Detaljhandelsortiment    |
| Behandle detaljhandelsetterfylling                                                    | Grupper butikker for å etterfylle beholdning basert på etterfyllingsregler.                                                                                                                                                                                                                                          | Detaljhandeletterfylling |
| Rapportere data for butikker                                                         | Grupper butikker for rapportering.                                                                                                                                                                                                                                                                                | Detaljhandelsrapportering     |
| Postere beholdning, beregne utdrag eller postere utdrag for en gruppe butikker | Opprett en gruppe med butikker som kan tilordnes til en satsvis jobb. Når du definerer en satsvis jobb for å postere lager, beregne utdrag eller postere utdrag, kan du angi hvilket hierarki jobben gjelder. Når butikker legges til i eller fjernes fra hierarkiet, trenger du ikke å endre den satsvise jobben. | Retail POS-postering   |






