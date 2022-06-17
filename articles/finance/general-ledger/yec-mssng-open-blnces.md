---
title: Manglende åpningssaldoer ved årsavslutning
description: Denne artikkelen beskriver hvorfor åpningssaldoer kan mangle når du avslutter et år, og hvordan du gjenoppbygger disse saldoene hvis de mangler.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9b64118fc3ff368e21ea8935c1e706f2161c620f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894855"
---
# <a name="year-end-close-missing-opening-balances"></a>Manglende åpningssaldoer ved årsavslutning

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvorfor åpningssaldoer kan mangle når du avslutter et år, og hvordan du gjenoppbygger disse saldoene hvis de mangler.

### <a name="symptom"></a>Symptom

Hvorfor er det ingen startsaldoer etter at du har kjørt årsavslutning for økonomimodulen? 

### <a name="resolution"></a>Løsning

Her er ting du kan sjekke hvis du har avsluttet et år i økonomimodulen og deretter generert en råbalanse som ikke viser åpningssaldoer, for det neste regnskapsåret.

Hvis feltet **Angre forrige avslutning** er satt til **Ja**, blir den forrige årsavslutningen for det samme regnskapsåret tilbakeført. Når du kjører en prosess for å tilbakeføre årsavslutningen, slettes alle oppføringer for både slutt- og åpningssaldoer som om året aldri var blitt avsluttet. Bilagene slettes også. Årsavslutningsprosessen kjøres ikke automatisk på nytt. Du må starte prosessen på nytt, og denne gangen må du oppdatere alternativet **Angre forrige avslutning** til **Nei**.

Dette scenarioet dekkes i artikkelen om årsavslutning i vanlige spørsmål. Hvis du vil ha mer informasjon, kan du se [Vanlige spørsmål om årssluttaktiviteter](faq-year-end-activities.md).

### <a name="symptom"></a>Symptom

Jeg kjørte årsavslutning med alternativet **Angre forrige avslutning** satt til **Nei**, og jeg har fremdeles ikke åpningssaldoer for regnskapsåret mitt.

### <a name="resolution"></a>Løsning

Kontroller først statusen til den satsvise jobben. Avslutning av et år omfatter en rekke separate oppgaver, men det mest kritiske trinnet er den satsvise oppgaven med oppgavebeskrivelsen **Trinn 5.0.0**. Postering av åpningstransaksjonene, og eventuelt avslutningstransaksjonene, til økonomimodulen skjer i dette trinnet. 

[![Satsvis logg.](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)

Hvis dette trinnet ble avsluttet, men du ikke ser åpningssaldoer på siden **Forespørsel om råbalanse** (**Økonomimodul > Forespørsler og rapporter > Råbalanse**), kan du se gjennom resultatene for den satsvise jobben ved årsavslutning for å se om trinnet Gjenoppbygg saldoer er fullført.

[![Resultater av den satsvise jobben for årsavslutning.](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)

Hvis dette trinnet av en eller annen grunn har mislykkes, ble åpningstransaksjonene (og eventuelt avslutningstransaksjonene) sannsynligvis postert. Du kan kontrollere at økonomimodultransaksjonene ble postert på riktig måte ved hjelp av siden **Forespørsel om bilagstransaksjoner** ved å angi bilagsnummeret og datoen som er angitt i dialogboksen for årsavslutning, for året du lukket (**Økonomimodul > Forespørsler og rapporter > Bilagstransaksjoner**).

[![Forespørsel om bilagstransaksjoner.](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)

Hvis åpningsbilagene (og eventuelt avslutningsbilagene) finnes, trenger du ikke å kjøre årsavslutningen på nytt. Du kan i stedet se den neste delen for å få informasjon om hvordan du går videre.

### <a name="symptom"></a>Symptom

Trinnet Gjenoppbygg saldoer i årsavslutningen mislyktes. Må jeg kjøre hele årsavslutningsprosessen på nytt?

### <a name="resolution"></a>Løsning

Trinnet Gjenoppbygg saldoer oppdaterer økonomimodulsaldoene som brukes når forespørselen om råbalanse genereres.  Det er det siste trinnet i årsavslutningsprosessen.  Hvis dette trinnet er det eneste trinnet som mislyktes, er transaksjonene i økonomimodulen postert.  Du trenger ikke å kjøre årsavslutningen på nytt. Du kan kjøre prosessen for å gjenoppbygge saldoene manuelt ved å bruke siden **Finansdimensjonssett** (**Økonomimodul > Kontoplan > Dimensjoner > Finansdimensjonssett**).

[![Knappen Gjenoppbygg saldoer på siden Finansdimensjonssett.](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)

Hvis det tar lang tid å behandle dette trinnet, anbefaler vi at du går gjennom anbefalte fremgangsmåter for finansdimensjonssett, som beskrevet i [Anbefalte fremgangsmåter for oppdatering av finansdimensjonssett](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets). 

