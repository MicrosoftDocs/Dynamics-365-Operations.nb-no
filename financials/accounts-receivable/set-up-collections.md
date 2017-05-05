---
title: Definer kreditt og innkreving
description: Denne artikkelen forklarer hvordan du konfigurerer innkrevingsfunksjonene.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustCollectionsActivitiesListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14031
ms.assetid: dcc6da2f-9af5-4f1d-abaa-b72967b66979
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 1a9bf1067d0f6e0e139ef13d939d2f0e9bf2126b
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-credit-and-collections"></a>Definer kreditt og innkreving

[!include[banner](../includes/banner.md)]


Denne artikkelen forklarer hvordan du konfigurerer innkrevingsfunksjonene.

<a name="set-up-aging-period-definitions"></a>Definer definisjoner av aldersfordelingsperiode
-------------------------------

Angi definisjon av aldersfordelingsperiode. En definisjon på aldersfordelingsperioden definerer kolonnene som vises på listesidene **Aldersfordelte saldoer**, **Innkrevingsaktiviteter** og **Innkrevingssaker**. Den definerer også periodene som vises på siden **Innkrevinger**. Hvis det er definert en kundepulje, brukes aldersfordelingsperioden for puljen. Hvis det ikke er definert puljer, brukes standarddefinisjonen for aldersfordelingsperiode som er angitt på siden **Kundeparametere**. Hvis det ikke er angitt en definisjon av standard aldersfordelingsperiode, brukes den første definisjonen av aldersfordelingsperiode som er angitt på siden **Definisjoner av aldersfordelingsperiode**.

## <a name="create-an-aging-snapshot"></a>Opprett et øyeblikksbilde av aldersfordeling
Opprett poster for øyeblikksbilde av aldersfordeling for alle kunder eller for kundene i en kundepulje. Øyeblikksbilde av aldersfordeling vises på listesiden **Aldersfordelte saldoer** og på siden **Innkrevinger**. Du må opprette et øyeblikksbilde av aldersfordeling før du kan bruke listesiden. Listesiden vise bare informasjon for kunder det er blitt opprettet et øyeblikksbilde av aldersfordeling for.

## <a name="optional-set-up-customer-pools"></a>Valgfritt: Definer kundepuljer
Du kan definere kundepuljer for å representere kundegrupper. Du kan bruke kundepuljer som filtre for kundeinformasjonen som vises på listesidene **Innkrevinger** på siden **Innkrevinger**, eller når du oppretter øyeblikksbilder av aldersfordeling.

## <a name="optional-create-a-collections-team"></a>Valgfritt: Opprett et innkrevingsteam
Hvis flere mennesker i organisasjonen gjør innkrevingsarbeid, kan du definere et innkrevingsteam. Du kan velge teamet på siden **Kundeparametere**. Hvis du ikke oppretter et innkrevingsteam, vil det bli opprettet ett automatisk når du definerer innkrevingsagenter på siden **Innkrevingsagent**.

## <a name="set-up-a-collections-case-category"></a>Definer en inkassosakskategori
Hvis du vil organisere innkrevingsarbeidet ved hjelp av saker, definerer du en sakskategori med kategoritypen **Innkrevinger**. Dette oppsettet er bare nødvendig hvis du vil bruke saksfunksjonaliteten på siden **Innkrevinger**.

## <a name="set-up-journal-names-settlement-writeoff-and-nsf"></a>Definer journalnavn for (utligning, avskrivning og ingen dekning)
Definere journalnavn som brukes når transaksjoner behandles på siden **Innkrevinger**. Denne prosessen inkluderer utligning av en transaksjon, avskriving av en transaksjon og behandling av en betaling uten dekning.

| Beskrivelse | Journaltype     |
|-------------|------------------|
| Bosetting  | Kundebetaling |
| Avskrivning   | Daglig            |
| Ingen dekning         | Kundebetaling |

## <a name="set-up-a-reason-code-for-writeoff-transactions"></a>Definer en årsakskode for avskrivningstransaksjoner
Definer standard årsakskode som skal brukes når transaksjoner avskrives på siden **Innkrevinger**. Du kan endre koden i løpet av avskrivingsprosessen.

## <a name="set-up-a-folder-for-email-attachments-and-create-email-templates"></a>Definer en mappe for e-postvedlegg og opprett e-postmaler
Hvis du skal sende e-postmeldinger fra siden **Innkrevinger** side som Microsoft Excel-vedlegg, kan du opprette valgfrie e-postmaler for disse meldingene.

## <a name="set-up-accounts-receivable-parameters-for-collections"></a>Definere kundeparametere for innkrevinger
Definer kundeparametere som vises i fanen **Innkrevinger**.

## <a name="optional-set-up-collections-agents"></a>Valgfritt: Definer innkrevingsagenter
Hvis flere mennesker i organisasjonen gjør innkrevingsarbeid, kan du definere innkrevingsagenter. En innkrevingsagent er en arbeider som er definert som en bruker på siden **Brukerforbindelser**. Du kan tilordne kundepuljer (kundespørringer) til innkrevingsagenter for å hjelpe agentene å organisere arbeidet sitt. Innkrevingsagentene legges til teamet som velges på siden **Kundeparametere**. Hvis et team ikke er valgt på den siden, opprettes det automatisk et nytt team kalt **Innkrevinger**, og innkrevingsagentene legges til det teamet.

## <a name="set-up-a-writeoff-account"></a>Definer en avskrivningskonto
Definer avskrivningskontoen som anvendes for økonomimodulens avskrivingsoppføring når en transaksjon skrives av. Denne kontoen lagres på kundeposteringsprofilen.

## <a name="set-up-nsf-information-for-bank-accounts"></a>Definer informasjon om manglende dekning for bankkontoer
Oppdater bankkontoer slik at de har den riktige journalen når betalinger uten dekning identifiseres på siden **Innkrevinger**. I kategorien **Valutamanagement** i feltet **Journal for betaling uten dekning** velger du en betalingsjournal.

## <a name="set-up-outlook-settings-for-users-of-the-collections-page"></a>Definer Outlook-innstillinger for brukere av siden Innkrevinger
Før arbeidere kan opprette aktiviteter eller sende e-postmeldinger ved hjelp av siden **Innkrevinger** må du kontrollere at **Microsoft Outlook-synkronisering**-konfigurasjonsnøkkelen er valgt, og at Outlook-synkronisering er definert for disse arbeiderne.

## <a name="set-up-email-and-address-settings-for-collections-customer-contacts"></a>Definer e-post- og adresseinnstillinger for inkassokontakter for kunder
Definer e-postadresser for kundekontakter hvis du vil sende e-postmeldinger til disse kontaktene fra siden **Innkrevinger**. Innkrevingskontakten brukes som standardkontakt på siden **Innkrevinger**. Du kan definere en utdragsadresse for en kunde hvis utdrag skal ha en annen adresse enn hovedadressen. 

På hurtigfanen **Kreditt og innkreving** for en bruker, i feltet **Innkrevingskontakt**, velger du personen i kundeorganisasjonen som arbeider med din innkrevingsagent. Denne personen brukes som standardkontakt på siden **Innkrevinger**, og e-postmeldinger sendes til vedkommende. 

> [!NOTE] 
> Hvis innkrevingskontakt ikke er angitt for en kunde, brukes kundens hovedkontakt. Hvis det ikke er angitt hovedkontakt, sendes e-postmeldinger til den første adressen som er oppført på **Kontakter**-siden.

## <a name="set-up-email-settings-for-salespeople"></a>Definer e-postinnstillinger for selgere
Definer e-postadresser for selgere hvis du vil sende e-postmeldinger til selgere fra siden **Innsamlinger**. Definer en e-postadresse for hver selter i hver provisjonssalgsgruppe. Selgeren som er merket av som **Kontakt**, er standardselgeren som e-postmeldinger sendes til. 

Hvis det ikke er angitt en selger, brukes kundeorganisasjonens hovedselger. Hvis det ikke er angitt hovedselger, sendes e-post meldinger til den første selgeren som er oppført på siden.



