---
title: "Årsavslutning"
description: "Dette emnet beskriver den nødvendige konfigurasjonen og trinnene for å kjøre Finans Lukk årsavslutningsprosessen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerClosingSheet
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 22233cfa1df79076c8ea42f75ea309bac990d574
ms.lasthandoff: 03/31/2017


---

# <a name="year-end-close"></a>Årsavslutning

Dette emnet beskriver den nødvendige konfigurasjonen og trinnene for å kjøre Finans Lukk årsavslutningsprosessen. 

På slutten av et regnskapsår, må du kjøre Lukk årsavslutningsprosessen for å overføre åpningssaldoer for det nye året. De fleste organisasjoner vil kjøre Lukk årsavslutningsprosessen flere ganger. Første gang, vil være å få saldoene flyttet inn i det nye regnskapsåret. Ved årsslutt lukking kan deretter kjøres på nytt, som ofte er nødvendig for å flytte saldoene fra justeringsposter i det nye regnskapsåret. 

Det finnes to typer mulige transaksjoner som er opprettet under årets close-prosessen. En åpning transaksjon genereres alltid og brukes til å opprette åpningssaldoene i det nye regnskapsåret. Den åpne transaksjonen viser balansen finanssaldoer-konto i det nye regnskapsåret og balanserer fra fortjeneste og tap Finans kontosaldoene i finanskontoen for fri egenkapital i det nye regnskapsåret. Avsluttende transaksjonen opprettes også for å vise saldoene i resultatkontoer ned til null i regnskapsåret lukkes.

## <a name="prepare-to-run-the-year-end-close"></a>Klargjør kjøring av den ved årsavslutning
Før du kjører årsavslutningsprosessen Lukk, må du kontrollere innstillingene for følgende: 

På **Hovedkonto**-siden:

-   Validere den **Main kontotypen** er riktig definert for hver hovedkontoen. Hoved-kontotypen brukes til å avgjøre om saldoen for hovedkontoen skal meldes som en startsaldo eller lukket til fri egenkapital i den åpne transaksjonen.
-   Den **åpner konto** feltet kan brukes til å overføre saldoen for hovedkontoen til en ny hovedkonto under ved årsslutt lukking. Ny hovedkontoen er angitt i den **åpner konto** feltet. Vanligvis vil dette bli brukt til hovedvinduet balansekonti når hovedkontoen er deaktiveres og en ny hovedkonto brukes for det nye regnskapsåret.

På den **økonomimodulparametere** side **årsavslutning**:

-   Den **Slett Lukk år transaksjoner** alternativet brukes til å angi om systemgenererte åpne transaksjonen fra en tidligere ved årsslutt lukking skal slettes når ved årsslutt lukking kjøres på nytt. Hvis dette alternativet er satt til **Ja**, slettes den forrige åpne transaksjonen og en ny åpning transaksjon opprettes basert på gjeldende saldoer. Hvis dette alternativet er satt til **ingen**, tidligere åpning transaksjonen forblir og en mer åpne transaksjonen er opprettet for å flytte fremover saldoene fra justering av transaksjoner som er postert etter den forrige årsavslutning.
-   Den **opprette lukkingstransaksjoner under overføring** alternativet brukes til å opprette avslutningstransaksjoner i regnskapsåret lukkes for å vise saldoene i resultatkontoer og balansekontoer til null. Hvis dette alternativet er satt til **Ja**, både åpne transaksjonen og avslutningstransaksjoner opprettes. Hvis dette alternativet er satt til **ingen**, bare åpne transaksjonen opprettes i det neste regnskapsåret skal overføre balansene. Fortjeneste og tap kontosaldoene forblir på slutten av regnskapsåret.
-   Den **Sett regnskapsåret til permanent lukket** alternativet brukes til å angi regnskapsåret til statusen lukket permanent. Bruk denne innstillingen med forsiktighet, fordi alle perioder med godt lukket status ikke kan åpnes på nytt, hindrer justeringer posteres til regnskapsår. Det er lurt å sette dette til **ingen**.
-   Den **bilagsnummer må fylles ut** alternativet brukes til å definere om et bilagsnummer er nødvendig når du kjører Lukk årsavslutningsprosessen. Det er en god til å kreve et bilagsnummer for å enkelt identifisere den åpne transaksjonen.

På den **regnskapskalenderen** side:

-   Det neste regnskapsåret må finnes før du kjører den ved årsslutt lukking. Det neste regnskapsåret er nødvendig for å opprette startsaldoer i den første perioden.

På den **Finanskalender** side:

-   Valgfritt: Hver regnskapsperiode for regnskapsåret lukkes kan settes til **på vent** å forhindre at nye transaksjoner registreres. Når justeringer er identifisert, kan videre hold periodene åpnes på nytt for å postere justeringer, selv om Lukk årsavslutningsprosessen allerede er kjørt.

## <a name="define-year-end-close-templates"></a>Definere maler for årets Lukk
Etter at systemet er konfigurert, kan du kjøre Lukk årsavslutningsprosessen. På den **årsavslutning** -siden en mal som kan defineres for en gruppe med juridiske enheter som årsavslutning prosessen skal kjøres. Malen som skal brukes ved hver årsavslutning tett, men kan endres hvis organisasjonen endres. 

Først definere den **navn på** for malen, og velg den økonomiske kalenderen. Gruppenavnet må identifisere gruppe med juridiske enheter som er inkludert.  For eksempel kan malene være satt opp basert på geografi, med separate grupper som er opprettet for juridiske enheter for Nord-Amerika, juridiske enheter i EMEA og APAC juridiske enheter. 

Neste, juridiske enheter kan legges til i malen. Juridiske enheter kan legges ved å velge et organisasjonshierarki, eller ved å velge de juridiske enhetene. Hvis det velges et organisasjonshierarki, legges bare juridiske enheter i hierarkiet som bruker den valgte regnskapskalenderen i malen. Hvis du bruker juridiske enheter for å legge til malen, kan du legge til juridiske enheter med samme regnskapskalenderen. Den samme regnskapskalenderen er nødvendig fordi ved årsslutt lukking kjøres ved å velge et regnskapsår, som kan variere fra kalender til kalender. 

Når de juridiske enhetene som er lagt til, kan du definere egenkapital hoved-kontoer for hver juridiske enhet. Den **datoen for slutten av forrige år lukke** oppdateres hver gang årsslutt lukking kjøres for juridisk enhet. 

Den **finansdimensjon** brukes til å definere hvilke økonomiske dimensjoner som skal brukes på den åpne transaksjonen. Legg merke til at innstillingene du definerer gjelder bare for juridisk enhet som er valgt i den **juridiske enheter** rutenett. Du vil gjenta oppsettet for hver juridiske enhet i rutenettet. 

Den **overføre balansen dimensjoner** brukes til å definere om økonomiske dimensjoner på transaksjoner som er postert til balansekontoer skal beholdes på den åpne transaksjonen. Det er lurt å angi dette alternativet til å **Ja**. Den **overføre resultat dimensjoner** brukes til å definere hvilke økonomiske dimensjoner på transaksjoner som er postert til fortjeneste og tapskonto vil bli overført til hovedkontoen for fri egenkapital. Først må du angi finansdimensjonene som er relevante for den valgte juridiske enheten. Dette omfatter alle økonomiske dimensjoner som postert mot i løpet av året, selv om den økonomiske dimensjonen ikke er en del av en aktiv kontostruktur. Deretter definerer du hver dimensjon som enten **Lukk enkelt** eller **lukke alle**.  Standard er **lukke alle**, som opprettholder den opprinnelige finansdimensjonen verdier fra posterte transaksjoner og bruker dem for å lage åpning saldoer for kontoen for fri egenkapital. Egen fri egenkapital startsaldoer opprettes for hver unike kombinasjon av økonomiske dimensjonsverdier. Hvis **Lukk enkelt** er valgt, alle transaksjoner som er postert med den økonomiske dimensjonen blir summert i en fri egenkapital, startsaldo for dimensjonsverdien som er angitt i feltet etter **Lukk enkelt**. Anta for eksempel at alle transaksjonene for regnskapsåret ble postert med kontostrukturen for hovedkontoen - avdeling. For avdeling finansdimensjonen på malen, **Lukk enkelt** er valgt, og 100 er verdien som er angitt. Hvis samlet inntekt av alle transaksjoner som er postert til avdelinger 200, 300 og 400 $100,000, opprettes det en startsaldo for Retained inntekter - 100. Hvis du velger **Lukk ett** og la det stå tomt finansdimensjonsverdien, alle transaksjoner med denne dimensjonsverdien som tom bokfører til egenkapital. 

Lukk årsavslutningsprosessen ikke etterkommer grensesnittdefinisjonen kontostrukturer. Dette er fordi kontostrukturer kan endre i løpet av et regnskapsår, og det er ikke alltid mulig å identifisere den relevante kontostrukturen på grunn av disse endringene.  Når åpningstransaksjoner opprettes, utviklet saldoene fremover med økonomiske dimensjoner som er definert i år end Lukk malen. Begynnelsen saldoer poster kan ikke lenger ta med økonomiske dimensjoner i gjeldende konto struktur og segment kombinasjoner er ikke lenger gyldig i den gjeldende kontostrukturen. Hvis organisasjonen ønsker å utelate en finansdimensjon for tilbakeholdt øker med startsaldo, angir finansdimensjonen du vil være **Lukk ett** og la det stå tomt dimensjonsverdien.

## <a name="run-the-year-end-close-process"></a>Kjøre Lukk årsavslutningsprosessen
Etter at årets Lukk malene er opprettet, Lukk årsavslutningsprosessen startes ved å velge **kjører regnskapsåret** i handlingsruten. Velg alle eller et delsett av juridiske enheter fra mal å kjøre den ved årsslutt lukking. Når du kjører i årets lukke for første gang i et regnskapsår, velger du sannsynligvis alle juridiske enheter til å opprette startsaldoer for alle juridiske enheter. Hvis du kjører den ved årsslutt lukking på nytt, kan du velge å kjøre-prosessen for bare juridiske enheter som å justere postene ble bokført. 

Velg regnskapsåret som du vil kjøre år end Lukk prosessen mot. Hvis det finnes mer enn en avslutningsperiode for den siste perioden i regnskapsåret, den **navn** feltet vil bli tilgjengelige slik at du kan velge hvilke avslutningsperiode å postere avslutningstransaksjoner, hvis installasjonen er definert til å opprette avslutningstransaksjoner. 

Angi et bilag nummer som eller kan være nødvendige, avhengig av oppsettet i Økonomiparametere. Det samme bilagsnummeret brukes for alle juridiske enheter valgt for år end Lukk prosessen. Bilagsnummeret som genereres ved hjelp av en nummerserie. Det er lurt å angi et bilagsnummer, selv om det ikke er påkrevd. Angi et bilagsnummer, gjør det enklere å finne den åpne transaksjonen i det nye regnskapsåret. Hvis du ikke skrive inn et bilagsnummer, er bilaget tomt for den åpne transaksjonen. 

Hvis du vil snu en tidligere årsslutt lukking for det valgte regnskapsåret, **angre tidligere lukking** til **Ja**. Tilbakeføres ved årsslutt lukking, men prosessen kan kjøres på nytt når som helst. Hvis du tilbakefører en ved årsslutt lukking, den **datoen for slutten av forrige år lukke** vil ikke være tilgjengelig. 

Lukk årsavslutningsprosessen standardene til å kjøre i satsvis modus. Det er lurt å kjøre-prosessen i satsvis modus, som tillater brukeren å gå tilbake til andre aktiviteter. Etter år end Lukk prosessen er fullført, den **datoen for slutten av forrige år lukke** vil bli oppdatert med datoen for klientøkt.

Hvis du vil ha mer informasjon, se [lukke Finans ved periodeslutt](close-general-ledger-at-period-end.md).


