---
title: Periodiske oppgaver for kredittstyring
description: Dette emnet beskriver de periodiske oppgavene som er en del av prosessen for å behandle kredittgrenser for kunder.
author: JodiChristiansen
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 53b7cd00b3287f18ba65391842ac259ab2434b86
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735443"
---
# <a name="periodic-credit-management-tasks"></a>Periodiske oppgaver for kredittstyring

[!include [banner](../includes/banner.md)]

Dette emnet beskriver de periodiske oppgavene som er en del av prosessen for å behandle kredittgrenser for kunder.

## <a name="update-risk-scores"></a>Oppdater risikopoeng

Ettersom selskaper utvikler seg og forhold endres, kan kredittrisiko for en gitt kunde også endre seg. Hvis du vil ha hjelp til å vedlikeholde riktige kredittgrenser for kundene, må du jevnlig gå gjennom kriteriene for hver risikopoengsum og oppdatere resultatene for hver kunde. Du kan oppdatere følgende resultater ved å bruke siden **Oppdater risikopoeng** (**Kreditt og innkreving \> Periodiske oppgaver \> Kredittbehandling \> Oppdater risikopoeng**). Alle brukerdefinerte beregninger blir også behandlet.

- **Gjennomsnittlig betalingsdager** – Denne poengsummen er gjennomsnittlig antall dager en kunde bruker for å betale fakturaer.
- **Kunde siden** – Denne poengsummen er antall år en kunde har vært kunde i organisasjonen.
- **Drevet virksomhet siden** – Denne poengsummen er antall år en kunde har drevet virksomhet. Den bruker verdien i feltet **Forretningsstart** på **Kunder**-siden.
- **Dager utestående salg** – Denne poengsummen er basert på kundesaldoen, salgsinntekter og antall dager i forrige 12-månedersperiode.
- **Gjennomsnittlig saldo**– Denne poengsummen er basert på kundesaldoen for forrige 12-månedersperiode.
- **Kredittbehandlingsgruppe**, **Kontostatus** og **Land** – Disse resultatene bruker informasjon fra kunden.

## <a name="update-customer-balance-statistics"></a>Oppdatere kundesaldostatistikk

Du kan kjøre prosessen **Oppdater kundesaldostatistikk** for å oppdatere beregningen av saldostatistikk som vises på siden **Forespørsel om saldostatistikk**. Denne informasjonen brukes til å beregne risikoresultater og verdiene som vises i faktaboksene for kredittstatistikk på **Kunde**-siden.

Når du kjører prosessen, oppdaterer den kundesaldostatistikk for en enkelt kunde. Hvis du vil definere en satsvis jobb for å kjøre prosessen for flere kunder, kan du bruke siden **Beregn saldostatistikk** (**Kredittbehandling \> Periodiske oppgaver \> Beregn saldostatistikk**).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
