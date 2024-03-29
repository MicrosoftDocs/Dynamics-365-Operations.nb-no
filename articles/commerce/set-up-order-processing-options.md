---
title: Definere telefonsenterkanaler
description: Denne artikkelen gir informasjon om hvordan du behandler ordrer for telefonsentre ved hjelp av Dynamics 365 Commerce.
author: josaw1
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCROrderParameters, MCRSalesTableOrderHistory, SalesOrderProcessingWorkspace
audience: Application User
ms.reviewer: josaw
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c6d21385d956534c799af5b9e20a54c9970da368
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854877"
---
# <a name="set-up-call-center-channels"></a>Definere telefonsenterkanaler

[!include [banner](includes/banner.md)]

Et firma kan definere flere telefonsenterkanaler i Dynamics 365 Commerce. Telefonsenterkanaler konfigureres under **Retail og Commerce** \> **Kanaler** \> **Telefonsentre** \> **Alle telefonsentre**, og de er spesifikke for en juridisk enhet.

Når det opprettes en ny telefonsenterkanal, tildeles den et driftsenhetsnummer systematisk. Fordi telefonsentre opprettes som driftsenheter, kan brukere koble telefonsenterkanalen til forskjellige Commerce-funksjoner, for eksempel sortimenter, kataloger og bestemte leveringsmåter.

Et standardlager kan konfigureres på telefonsenterkanalen. Deretter, når det opprettes salgsordrer i denne kanalen, angis standardlageret automatisk i salgsordrehodet, med mindre et annet lager er definert på kunden som er valgt for salgsordren. I så fall er kundens lager angitt som standard.

Brukere må være koblet til en telefonsenterkanal for å kunne bruke funksjonene for telefonsenter. Salgsordrer som en bruker oppretter, kobles automatisk til denne brukerens telefonsenterkanal. For øyeblikket kan ikke en enkeltbruker kobles til flere telefonsenterkanaler samtidig.

En profil for e-postvarsling kan også konfigureres på telefonsenterkanalen. Profilen definerer settet med e-postmaler som brukes når e-post sendes til kunder som foretar bestillinger via telefonsenterkanalen. Du kan konfigurere e-postutløsere mot systemhendelser, for eksempel ordreoverføring eller overføringsordre.

Før salget kan behandles korrekt gjennom en telefonsenterkanal, må korrekte [betalingsmåter](/dynamics365/unified-operations/retail/work-with-payments) og leveringsmåter defineres for kanalen.

På nivået for telefonsenterkanalen kan du definere andre standardverdier som er knyttet til finansdimensjonene som skal knyttes til ordrer som opprettes av kanalen.

## <a name="options-for-order-processing-behavior"></a>Alternativer for virkemåten for ordrebehandling

Tre innstillinger i konfigurasjonen av et telefonsenter har en stor innvirkning på funksjonene som er tilgjengelige for salgsordrer som opprettes mot dette telefonsenteret: **Aktiver ordrefullføring**, **Aktiver styrt salg** og **Aktiver ordrepriskontroll**.

### <a name="enable-order-completion"></a>Aktiver ordrefullføring

Innstillingen **Aktiver ordrefullføring** på telefonsenterkanalen har en stor innvirkning på flyten av salgsordrer som er angitt for for den kanalen. Når denne innstillingen er aktivert, må alle salgsordrer gå gjennom et sett med valideringsregler før de kan bekreftes. Du kjører disse reglene ved å velge **Fullført**-knappen som legges til i handlingsruten på siden for salgsordren. Alle salgsordrer som opprettes når innstillingen **Aktiver ordrefullføring** er slått på, må gå gjennom prosessen for ordrefullføring. Denne prosessen implementerer logikken for registrering av betaling og betalingsvalidering. I tillegg til betalingsaktivering kan ordresendingsprosessen utløse [svindelkontroller](/dynamics365/unified-operations/retail/set-up-fraud-alerts) som du konfigurerer i systemet. Ordrer som ikke består betalings- eller svindelkontroller, blir satt på vent og kan ikke gjøres tilgjengelig for ytterligere behandling (for eksempel plukking eller levering) før problemet som forårsaket sperringen, er løst.

Når innstillingen **Aktiver ordrefullføring** er slått på for telefonsenterkanalen, og hvis linjeelementer er angitt i en salagsordre og kanalbrukeren prøver å lukke eller navigere bort fra salgsordreskjemaet uten først å velge **Fullført**, bruker systemet ordrefullføringsprosessen ved å åpne siden Salgsordresammendrag og kreve at brukeren sendrer ordren korrekt. Hvis ordren ikke kan sendes riktig sammen med betalingen, kan brukeren bruke funksjonen [ordresperrer](/dynamics365/unified-operations/retail/work-with-order-holds) til å sette ordren på vent. Hvis brukeren prøver å avbryte ordren, må han eller hun avbryte den riktig ved hjelp av kanselleringsfunksjonen eller slettingsfunksjonen, avhengig av funksjonen som tillates av brukerens sikkerhet.

Hvis innstillingen **Aktiver ordrefullføring** er slått på for telefonsenterkanalen, spores **Betalingsstatus**-feltet i ordren. Systemet beregner **betalingsstatusen** når salgsordren sendes. Bare ordrer med godkjent betalingsstatus kan gå gjennom systemet for flere ordrebehandlingstrinn, for eksempel plukking og forsendelse. Hvis betalinger er avslått, aktiveres **ikke behandle**-flagget for den detaljerte ordrestatusen. Dette setter ordren på vent til betalingesproblemet er løst.

Hvis innstillingen **Aktiver ordrefullføring** er slått på når brukere oppretter salgsordrer og er i modus for linjeelementregistrering, er i tillegg **Kilde**-feltet tilgjengelig i det primære salgsordrehodet. **Kilde**-feltet brukes til å registrere en [katalogkildekode](/dynamics365/unified-operations/retail/call-center-catalogs) i et salgsscenario for direktemarkedsføring. Denne koden kan deretter brukes til spesialpriser og kampanjer.

Selv om innstillingen **Aktiver ordrefullføring** er deaktivert, kan brukere fremdeles bruke en kildekode til en salgsordre. De må imidlertid først åpne topptekstdetaljene for salgsordre for å få tilgang til **Kilde**-feltet. Med andre ord kreves noen ekstra klikk. Samme virkemåte gjelder funksjoner som forsendelsen ble fullført og fremskyndede ordrer. Disse funksjonene er tilgjengelige for alle ordrer som opprettes i telefonsenteret. Når innstillingen **Aktiver ordrefullføring** er aktivert, kan imidlertid brukerne se konfigurasjonen av disse funksjonene på salgshodet mens de er i linjeregistreringsvisning. De trenger ikke drille ned til topptekstdetaljene for salgsordre for å finne de riktige innstillingene og feltene.

> [!NOTE]
> Når funksjonen **Commerce-ordrebetalinger for omnikanal** er aktivert, er telefonsenterknappen **Aktiver ordrefullføring** skjult i hovedkvarteret på hurtigfanen **Generelt** for kanalen din på **Detaljhandel og handel \> Kanaler \> Telefonsentre**.

### <a name="enable-direct-selling"></a>Aktiver styrt salg

Hvis innstillingen **Aktiver styrt salg** er slått på for telefonsenterkanalen, kan brukere dra nytte av funksjonene mersalg og kryssalg i Commerce. I så fall vises popup-vinduer under ordreregistrering, og foreslår andre produkter som telefonsenterbrukeren kan tilby til kunden. Produktene som foreslås, er basert på produktet som nettopp ble bestilt på salgsordrelinjen. Forslagene for mersalg og kryssalg er for øyeblikket konfigurert på varenivå for produkter eller kataloger. Hvis innstlinngen **Aktiver styrt salg** er deaktivert for telefonsenterkanalen, vises ikke popup-vinduer under ordreregistrering, selv om gyldig mersalg og kryssalg ble definert for en vare som bestilles.

Når innstillingen **Aktiver styrt salg** er slått på, er også skript- og bildefunksjonene for siden salgsordreregistrering slått på. Et informasjonspanel er da tilgjengelig til høyre på siden under ordreregistrering. Dette panelet kan vise skript som er knyttet til den vanlige ordreregistreringsprosessen, katalogkildekoden som ble brukt, eller skript som er knyttet til varene som bestilles. Bildepanelet kan også vise et produktbilde for varene som bestilles, hvis et bilde er definert for varen i produktoppsettet.

### <a name="enable-order-price-control"></a>Aktiver ordrepriskontroll

Når innstillingen **Aktiver ordrepriskontroll** er slått på, kan bare autoriserte brukere endre salgsprisen for en vare under ordreregistrering. Endringene må være innenfor de definerte avvikene. Brukere som ikke har riktig autorisasjon, må sende en forespørsel om en prisendring i stedet. Forespørselen behandles deretter ved hjelp av systemarbeidsflyter for gjennomgang og godkjenning.

## <a name="channel-users"></a>Kanalbrukere

Når du definerer telefonsenterkanalen, må du knytte kanalbrukerne til telefonsenteret. Ellers kan ikke telefonsenteret brukes i systemet. Når brukere logger på Commerce og registrerer salgsordrer eller returordrer på en side som er knyttet til ordreregistrering, blir deres bruker-ID validert mot konfigurasjonen av telefonsenterkanalen. Hvis en bruker er koblet til en bestemt telefonsenterkanal, arver ordrer som brukeren oppretter, egenskapene og standardverdiene for denne kanalen.

Som standard er **Salg**-flagget på salgsordrehodet aktivert for alle ordrer som telefonsenterbrukere oppretter. Ordrene kan deretter dra nytte av systemets handelsspesifikke funksjoner for pris og kampanjer.


Brukere som ikke er koblet til en telefonsenterkanal, bruker standardfunksjonene for ordreregistrering i Microsoft Dynamics 365 Finance. Ordrer som disse brukerne legger inn via skjemaet for salgsordreregistrering, identifiseres ikke systematisk som handelsordrer. I tillegg vil ikke disse ordrene som legges inn av disse brukerne, være underlagt noen av behandlingsreglene for ordrefullføring, logikk for prissetting eller andre ordrevalideringer som kan defineres i konfigurasjonen av telefonsenterkanalen eller systemparameterne for telefonsenter.

Når du er ferdig med å konfigurere telefonsenterkanalen og definere kanalbrukere, må du kontrollere at alle nødvendige telefonsenterparametere er definert under **Retail og Commerce** \> **Kanaloppsett** \> **Telefonsenteroppsett** \> **Telefonsenterparametere**. Kontroller også at relaterte nummerserier er definert.

> [!NOTE]
> Konfigurasjonsnøkkelen for **Flere forsendelsesadresser** må være aktivert for å bruke funksjonalitet for telefonsenter. Denne konfigurasjonsnøkkelen kan finnes i nøklene for **Handelskonfigurasjon** under **Systemadministrasjon**\> **Oppsett** \> **Lisenskonfigurasjon**. Dette er nødvendig på grunn av telefonsenterfunksjonaliteten som utfører forskjellige valideringer basert på leveringsadressen som er konfigurert på salgsordrelinjenivå. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
