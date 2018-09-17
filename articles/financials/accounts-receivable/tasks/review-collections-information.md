--- 
title: "Gå gjennom innkrevingsinformasjon"
description: "Denne prosedyren hjelper deg med å gå gjennom innkrevingsinformasjon og forskjellige oppsettsalternativer og innkrevingstransaksjoner."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustCollectionsPool, SysQueryForm, CustCollectionsAgent, OMTeamSelectMemberDialog, CustVendReportInterval, CustParameters, CustAgingSnapshot, CustVendAgingBucketLookUp, CustCollectionsPoolsListPage, CustCollectionsContactPart, CustCollections
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: eb0866505702ec5d047b6c8f3f0657aae787bedc
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="review-collections-information"></a>Gå gjennom innkrevingsinformasjon

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren hjelper deg med å gå gjennom innkrevingsinformasjon og forskjellige oppsettsalternativer og innkrevingstransaksjoner. Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.


## <a name="create-customer-pools"></a>Opprette kundepuljer
1. Gå til Kreditt og innkreving > Oppsett > Kundepuljer.
    * Bruk denne siden til å definere kundepuljer, som er spørringer som definerer en gruppe kundekontoer som kan vises og administreres for purringer eller aldersfordelingsprosesser. Bruk kundepuljer for å filtrere informasjon på listesiden for innkrevinger og tilknyttede listesider. Du kan også bruke kundepuljer til å filtrere kundekontoene som inkluderes når øyeblikksbilder av aldersfordeling opprettes.  
    * Du kan bruke kundepuljer til å filtrere kundekontoene som inkluderes når øyeblikksbilder av aldersfordeling opprettes.  
2. Klikk Ny.
3. Skriv inn en verdi i feltet Pulje-ID.
4. Skriv inn en verdi i Puljebeskrivelse-feltet.
5. Klikk Velg puljekriterier.
6. Skriv inn en verdi i Kriterier-feltet.
7. Klikk OK.
8. Klikk Forhåndsvis kundepulje.

## <a name="create-collections-agents"></a>Opprette innkrevingsagenter
1. Gå til Kreditt og innkreving > Oppsett > Innkrevingsagenter.
    * Bruk denne siden til å definere arbeidere som innkrevingsagenter og eventuelt tilordne kundepuljer til dem. En innkrevingsagent er en person som arbeider med kunder for å sørge for at betalinger kreves inn i tide.  
    * Innkrevingsagenter som er definert på denne siden, legges automatisk til et innkrevingsteam. Hvis et team er valgt i Team-feltet på Kundeparametere-siden, legges innkrevingsagenter til dette teamet. Hvis et team ikke er valgt, opprettes det automatisk et nytt team kalt Innkrevinger og innkrevingsagentene legges til det teamet.  
2. Klikk Ny.
3. Klikk Legg til.
4. Klikk Lukk.
5. Klikk Legg til.
6. Merk den valgte raden i listen.
7. Klikk rullegardinknappen i feltet Pulje-ID for å åpne oppslaget.
8. Finn og velg ønsket post i listen.
9. Merk av eller fjern merket for Standardpulje.
    * Velg dette alternativet for å inkludere alle kundepuljer i filterlister for den valgte innkrevingsagenten. Hvis det ikke er merket av for dette alternativet, vil bare kundepuljer som er tilordnet til innkrevingsagenten, være tilgjengelige i filterlister.  

## <a name="create-aging-period-definition"></a>Opprette definisjon av aldersfordelingsperiode
1. Gå til Kreditt og innkreving > Oppsett > Definisjoner av aldersfordelingsperiode.
    * Du kan bruke definisjoner av aldersfordelingsperiode til å analysere modenheten til kundekontoer og leverandørkontoer, basert på en dato du angir. Hver aldersfordelingsperiode du angir i definisjonen av aldersfordelingsperiode, svarer til en kolonne på listesiden eller i skjemaet eller rapporten når analysen blir utført.  
2. Klikk Ny.
3. Angi en verdi i feltet Definisjon av aldersfordelingsperiode.
4. Skriv inn en verdi i feltet Beskrivelse.
    * Angi periodenavn, enhet og intervall for hver aldersfordelingsperioden som skal tas med i definisjonen av aldersfordelingsperiode. Linjen som har 0 (null) i Enhet-feltet, representerer datoen som analysen kjøres. Linjer før null vil ha -1, og linjer etter null vil ha 1 som en standardoppføring i Enhet-feltet, men kan endres.  Klikk opp- og nedknappene for å ordne om på linjene. Linjen 0 (null) kan ikke flyttes.  
    * Plasser pekeren der du vil sette inn en ny linje, og klikk deretter Legg til.  
    * Velg en indikator som skal representere aldersfordelingsperioden på purreskjemaet og listesiden. Du kan for eksempel velge en grønn indikator for en gjeldende periode, en gul indikator for en periode på 30 dager over frist og en rød indikator for en periode på 90 dager over frist.  
    * Veg utskriftsretningen for definisjonen av aldersfordelingsperioden. Dette valget bestemmer rekkefølgen som kolonnene vises i, i rapporten Aldersfordelt saldoliste for kunder eller Aldersfordelt saldoliste for leverandører.  Fremover – Skriv ut kolonner i samme rekkefølge som overskrifter vises i, i tabellen, fra og med den øverste raden.  Bakover – Skriv ut kolonner i motsatt rekkefølge som overskrifter vises i, i tabellen, fra og med den nederste raden.    

## <a name="setup-collections-parameters"></a>Konfigurere innkrevingsparametere
1. Gå til Kreditt og innkreving > Oppsett > Kundeparametere.
2. Klikk kategorien Innkrevinger.
3. Vis eller skjul delen Innkrevingsstandarder.
    * Velg en definisjon av aldersfordelingsperiode for standard aldersfordelingsøyeblikksbilde som skal brukes i purreskjemaet.  
    * Velg et team som innkrevingsagenter tilordnes til, i Innkrevingsagent-skjemaet. Bare team som har en teamtype for purringer, vises i listen.  
4. Vis eller skjul Avskrive-delen.
    * Velg journalnavnet, som er definert for daglig finansjournaler, som skal brukes når en transaksjon avskrives ved hjelp av purreskjemaet eller tilknyttede listesider.  
    * Velg standard årsakskode som skal brukes når avskrivningstransaksjoner opprettes ved hjelp av purreskjemaet eller relaterte listesider.  
    * Velg dette alternativet for å opprette en egen journallinje for mva-beløp når avskrivningstransaksjoner opprettes ved hjelp av Innkrevinger-siden eller relaterte listesider. Hvis du velger dette alternativet, kan du enkelt spore mva-beløp som er involvert i avskrivningstransaksjoner. Du kan spore mva-beløp separat for å hjelpe deg å enkelt justere skyldig merverdiavgift for den aktuelle perioden.  
5. Vis eller skjul delen E-postmal.
    * Velg e-postmalen som skal brukes når du sender en e-postmelding ved hjelp av E-post > Transaksjoner til kontakthandlingen i purreskjemaet.  
    * Velg e-postmalen som skal brukes når du sender et kundekontoutdrag som vedlegg i en e-postmelding ved hjelp av E-post > Utdrag til kontakthandlingen i purreskjemaet.  
    * Velg e-postmalen som skal brukes når du sender en e-postmelding ved hjelp av E-post > Transaksjoner til selgerhandlingen i purreskjemaet.  

## <a name="age-customer-balance"></a>Aldersfordele kundesaldo
1. Gå til Kreditt og innkreving > Periodiske oppgaver > Aldersfordel kundesaldoer.
    * Velg en definisjon av aldersfordelingsperiode. Prosessen for øyeblikksbilde av aldersfordeling aldersfordeler transaksjoner i henhold til aldersfordelingsperiodene som er definert i den valgte definisjonen av aldersfordelingsperiode.  
    * Velg en kundepulje, eller la dette feltet stå tomt for å opprette et øyeblikksbilde av aldersfordeling for alle kunder. Hvis en kundepulje er valgt, brukes prosessen for øyeblikksbilde av aldersfordeling bare for kundekontoer som er en del av kundepuljen. Den valgte kundepuljen må være av typen Øyeblikksbilde av aldersfordeling.  
    * Velg datotypen som øyeblikksbildet av aldersfordeling skal baseres på.    Transaksjonsdato – Aldersfordel hver transaksjon basert på transaksjonsdatoen.    Forfallsdato – Aldersfordel hver transaksjon basert på forfallsdatoen.    Dokumentdato – Aldersfordel hver transaksjon basert på dokumentdatoen.  
    * Velg datoen som skal brukes som den gjeldende datoen for øyeblikksbildet av aldersfordeling. Aldersfordelingsperioder beregnes basert på denne datoen.    Dagens dato – Bruk systemdatoen. Bruk dette alternativet hvis behandling er konfigurert for å utføres i et gjentakende parti. Hvis du bruker denne datoen, kan det gjentakende partiet kjøres med jevne mellomrom, og systemdatoen på dette tidspunktet brukes.    Valgt dato – Bruk en dato du angir. Hvis du velger dette alternativet, angir du en aldersfordelingsdato.  
2. Klikk OK.

## <a name="view-aged-customer-balances"></a>Vise aldersfordelte kundesaldoer
1. Gå til Kreditt og innkreving > Innkrevinger > Aldersfordelte saldoer.
    * Bruk denne listesiden til å vise kundesaldoer og aldersfordelte beløp etter aldersfordelingsperiode. Denne informasjonen er lagret i et øyeblikksbilde av aldersfordeling. Aldersfordelingsperiodene bestemmes av den definisjonen av aldersfordelingsperiode som er i bruk. Definisjonen av aldersfordelingsperiode hentes fra kundepuljen, hvis det er angitt en slik for puljespørringen. Hvis kundepuljen ikke har en definisjon for aldersfordelingsperiode, brukes standarddefinisjonen for aldersfordelingsperiode som er angitt i Kundeparametere-skjemaet.  
2. Vis faktaboksen Kontakt.
    * Kontaktpersonen for purringer for kunden.  
    * Standardselgeren for kunden.  
3. Vis faktaboksen Kredittgrense.
    * Bruk faktaboksen Kredittinformasjon til å vise kredittgrensen og gjeldende saldoinformasjon for kunden.  

## <a name="view-customer-collections-details"></a>Vise detaljer om kundepurringer
1. Klikk koblingen i den valgte raden i listen.
2. Vis faktaboksen Adresse.
3. Vis faktaboksen Kontakt.
4. Vis faktaboksen Aldersfordeling.
5. Vis faktaboksen Kredittgrense.
6. Klikk Innkreving i handlingsruten.
    * Oppdater øyeblikksbildet av aldersfordeling for kunden med gjeldende dato som aldersfordelingsdato som transaksjonsdatoene sammenlignes med. Hvis øyeblikksbildet av aldersfordeling inneholder informasjon for flere juridiske enheter, inneholder øyeblikksbildet av aldersfordeling informasjon for det samme settet med juridiske enheter. Beløp lagres i regnskapsvalutaen for den juridiske enheten som du er logget på når du oppdaterer øyeblikksbildet av aldersfordeling.  
    * Velg en definisjon av aldersfordelingsperiode. Som standard vises definisjonen av aldersfordelingsperiode som er tilknyttet øyeblikksbildet av aldersfordeling for kunden. Definisjonen av aldersfordelingsperiode styrer aldersfordelingsperiodene og beløpene som vises i faktaboksen Aldersfordelte saldoer og Kredittinformasjon.  
    * Åpne en meny med følgende elementer: Firma – Vis beløpene i faktaboksen Aldersfordelte saldoer og Kredittinformasjon i regnskapsvalutaen for den juridiske enheten.    Kunde – Vis beløpene i faktaboksen Aldersfordelte saldoer og Kredittinformasjon i kundens valuta.  
    * Velg én eller flere juridiske enheter i kundens øyeblikksbilde av aldersfordeling som det skal vises informasjon for. De juridiske enhetene som vises i listen, ble merket da øyeblikksbildet av aldersfordeling ble opprettet.  
    * Vis kundens utdrag i Microsoft Excel-format. Du kan velge en startdato for transaksjonsområdet som skal tas med i utdraget, og bestemme om du vil inkludere bare åpne transaksjoner eller både åpne og utlignede transaksjoner. Hvis øyeblikksbildet av aldersfordeling inneholder informasjon for flere juridiske enheter, inkluderes transaksjoner for alle juridiske enheter.  
    * Åpne Dokumenter-skjemaet, der du kan opprette eller redigere dokumenter og notater.  
7. Klikk Kommuniser i handlingsruten.
    * Åpne Outlook, der du kan sende en e-postmelding til kontakten som er angitt i feltet Kontakt. Hvis innkrevingskontakten ikke er angitt, brukes primæradressen for kunden. Hvis det ikke er angitt hovedkontakt, sendes e-post meldinger til den første adressen som er oppført i Kontakter-skjemaet . Transaksjonene som velges, tas med som et vedlegg. Vedlegget er i Excel-format og inneholder tre regneark. En e-postmal for meldinger til kundekontakter kan angis i Kundeparametere-skjemaet.  
    * Denne knappen er ikke tilgjengelig hvis kontakten som er valgt i dette skjemaet, ikke har definert en e-postadresse.  
    * Forbered et utdrag, og åpne Outlook, der du kan sende en e-postmelding med et vedlagt utdrag til adressen som er angitt i Kontakt-feltet. Hvis innkrevingskontakten ikke er angitt, brukes primæradressen for kunden. Hvis det ikke er angitt hovedkontakt, sendes e-post meldinger til den første adressen som er oppført i Kontakter-skjemaet .  
    * Denne knappen er ikke tilgjengelig hvis kontakten som er valgt i dette skjemaet, ikke har definert en e-postadresse.  
    * Åpne Outlook, der du kan sende en e-postmelding til den ansatte som er angitt som selger for salgsgruppen som er knyttet til kunden. Hvis transaksjoner velges, tas de med som et vedlegg. Vedlegget er i Excel-format og inneholder to regneark. En e-postmal for meldinger til selgere kan angis i Kundeparametere-skjemaet.  
    * Denne knappen er ikke tilgjengelig hvis selgeren som vises i skjemaet, ikke har definert en e-postadresse.  
    * Vis og utfør handlinger for transaksjoner for kunden. Hvis du bruker sentraliserte betalinger, inkluderes informasjon for alle juridiske enheter som er inkludert i kundens øyeblikksbilde av aldersfordeling. Du kan begrense informasjonen for den juridiske enheten ved hjelp av Firma-knappen i Velg gruppe i handlingsruten.  
    * Endre purrestatusen for de valgte transaksjonene.    Ikke bestridt – Ingen innkrevingshandling har funnet sted for transaksjonen.    Tvist – Kunden har varslet deg om at det er et problem med transaksjonen.    Løfte om betaling – Kunden har avtalt å betale transaksjonsbeløpet.    Løst – Alle problemer med transaksjonen er løst, og flere innkrevinger er ikke nødvendig.  
    * Åpne en meny, og velg ett av følgende elementer for å angi hvilke transaksjoner som skal vises i dette formatet: Åpen – Vis bare transaksjoner som ikke er utlignet.    Åpen og lukket – Vis alle transaksjoner, både utlignede og ikke er utlignede.  
    * Behandle den valgte betalingen som en betaling uten dekning.    Denne knappen er bare tilgjengelig hvis den valgte transaksjonen er en betaling (en kreditsaldo uten en faktura) som er registrert i en betalingsjournal, en bankkonto er tilordnet til transaksjonen, og betalingen har ikke blitt annullert tidligere.  
    * Avskriv de valgte transaksjonene.  
    * Merk de valgte transaksjonene for utligning med hverandre.  
    * Åpne Opprinnelig dokument-skjemaet, der du kan vise og skrive ut dokumentet for den valgte transaksjonen.  
    * Åpne en meny med følgende elementer: Purringer – Vis bare aktiviteter som ble opprettet i purreskjemaet.    Alle – Vis alle aktiviteter for kunden, uansett hvor aktivitetene ble opprettet.  
    * Åpne en meny med følgende elementer: Åpen – Vis bare aktiviteter som ikke er lukket.    Åpen og lukket – Vis alle aktiviteter, uavhengig av status.  
    * Velg en innkrevingssak som er tilordnet til kunden, eller la dette feltet stå tomt. Hvis en sak er valgt, vises bare transaksjoner og aktiviteter som er tilknyttet saken, i dette skjemaet.  
8. Klikk Vis liste.
    * Velg en kundekonto eller godta standardoppføringen. Som standard er dette den valgte kundekontoen på listesiden eller i skjemaet som du åpnet dette skjemaet fra. Hvis du åpnet skjemaet fra en listeside, er kundene i listen kundene som er inkludert i purringspuljen som brukes på listesiden.  


