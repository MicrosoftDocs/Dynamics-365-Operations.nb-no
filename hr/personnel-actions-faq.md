---
title: "Vanlige spørsmål om personalhandlinger"
description: "Dette emnet inneholder svar på spørsmål du kan ha hvis organisasjonen bruker personalhandlinger. Personalhandlinger er flere trinn du må fullføre når du utfører bestemte personalrelaterte oppgaver."
author: shielas
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 4c17441b70a75f032c900c9360da6c0730cf89ba
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017


---

# Vanlige spørsmål om personalhandlinger
<a id="personnel-actions-faq" class="xliff"></a>
Dette emnet inneholder svar på spørsmål du kan ha hvis organisasjonen bruker personalhandlinger. Personalhandlinger er flere trinn du må fullføre når du utfører bestemte personalrelaterte oppgaver. Eksempler på oppgaver som kan kreve personalhandlinger, er når du oppretter nye stillinger, endrer verdier for eksisterende stillinger, ansette nye arbeidere, overføre arbeidere, endre arbeiderkompensasjon, endre stillingstilordninger eller avslutte arbeidere.

**Merk:** Personalhandlinger er bare tilgjengelige hvis konfigurasjonsnøkkelen Personalhandlinger er valgt. 

## Hvordan vet jeg om organisasjonen krever personalhandlinger?
<a id="how-can-i-tell-if-my-organization-requires-personnel-actions" class="xliff"></a>
Personalhandlinger er nødvendige for organisasjonen hvis du blir bedt om å velge en personalhandling når du oppretter nye stillinger, endrer eksisterende stillinger, ansetter nye arbeidere, overførr arbeidere, endrer arbeideres kompensasjon, endrer stillingstilordninger, sier opp arbeidere eller angir permisjon for arbeidere. 

## Hva er forskjellen mellom en stillingshandling og arbeiderhandlingen?
<a id="what-is-the-difference-between-a-position-action-and-a-worker-action" class="xliff"></a>
Det er to typer personalhandlinger:

- Stillingshandling – En stillingshandling utføres på eksisterende stillinger eller nye stillinger. En stillingshandling kan for eksempel være nødvendig hvis du endrer en verdi i en eksisterende stilling, eller hvis du oppretter en ny sesongstilling. Hvis du vil ha mer informasjon om hvordan du bruker stillingshandlinger, se Hovedoppgaver: eksisterende arbeiderstillinger eller Hovedoppgaver: nye Arbeiderstillinger.

- Arbeiderhandling – En arbeiderhandling er utført på eksisterende ansatte eller nye ansatte. En arbeiderhandling kan for eksempel være nødvendig når en ny ansatt ansettes eller en eksisterende ansatt forfremmes. Hvis du vil ha mer informasjon om hvordan du bruker arbeiderhandlinger, kan du se Tilordne personalhandlinger til arbeidere.

## Hva betyr statusene til personalhandlingene?
<a id="what-do-the-statuses-of-the-personnel-actions-mean" class="xliff"></a>
Personalhandlinger kan ha følgende status:

- **Utkast** – Hvis arbeidsflyt brukes, vil handlingen ikke sendt. Hvis arbeidsflyt ikke brukes, er ikke handlingen fullført.
- **Til vurdering**– Personalhandlingen er sendt til arbeidsflyten, men arbeidsflyten er ikke fullført.
- **Godkjente venter** – Arbeidsflyten er fullført, men endringene pågår fortsatt. Avbrutt – Arbeidsflyten ble avbrutt, eller personalhandlingen ble kalt tilbake. Avvist – Handlingsforespørselen ble avvist av godkjenneren.
- **Behandler handling** – Handlingsforespørselen er godkjent, og endringene behandles.
- **Arbeidsflyt fullført**  – Arbeidsflyten er fullført, og endringene er behandlet. Mislykket – Arbeidsflyten mislyktes fordi informasjonen er for gammel. Klikk Aktiver på nytt for å vise den nyeste informasjonen og fortsette.
- **Fullført**– Stillingen ble opprettet eller endret uten feil, eller den ansatt ble ansatt, overført eller avsluttet uten feil, eller har fått endret kompensasjon. Feil – Det oppstod et annet problem enn at informasjonen var utdatert. Åpne Meldingslogg for personalhandlinger for å finne årsaken til feilen.
- **Avslått** – Handlingsforespørselen ble avvist av godkjenneren.

## Kan jeg slette en personalhandling?
<a id="can-i-delete-a-personnel-action" class="xliff"></a>
Ja, du kan slette personalhandlinger som har statusen **Utkast**, **Feil**, **Mislykket** eller **Avbrutt**.

## Hva er den raskeste metoden for å kontrollere statusen for en forespørsel om personalhandling?
<a id="what-is-the-fastest-way-to-check-the-status-of-a-personnel-action-request" class="xliff"></a>
Åpne en av listesidene for personalehandling, og velg en personalehandling.

## Hva gjør jeg hvis en forespørsel for personalhandling mislykkes?
<a id="what-should-i-do-if-a-personnel-action-request-fails" class="xliff"></a>
Hvis en forespørsel om personalhandling mislykkes, følger du denne fremgangsmåten for å rette feilen og sende forespørselen på nytt:

> 1. Klikk **Feiltekst**-knappen i **handlingsruten** for å vise meldingsteksten som beskriver problemet.

> 2. Klikk **Aktiver på nytt** i **handlingsruten** for å laste inn den nyeste informasjonen og sette statusen for personalhandlingen tilbake til **Utkast**.

> 3. Rett opp feilen, og klikk deretter **Fullført** eller **Send inn**.

## Hva skjer med en personalhandling som bruker arbeidsflyt når den endelige godkjenningen er fullført?
<a id="what-happens-to-a-personnel-action-that-uses-workflow-when-the-final-approval-is-completed" class="xliff"></a>
Hvis det ikke finnes feil, blir personalhandlingen skrivebeskyttet. (Du kan vise loggen i på listesiden **Alle arbeiderhandlinger**, men du kan ikke endre personalhandlingen.) Når statusen til en personalhandling er **fullført**, er stillingen eller arbeiderposten allerede oppdatert. Hvis du vil vise endringene som ble utført, åpner du listesiden **Stillinger** eller **Arbeidere**.

## Hvorfor får jeg følgende feil når jeg angir en annen verdi enn null i Lønnssats-feltet? «Verdien er utenfor gyldig område – den må være mellom 0,00 og 0,00»
<a id="why-do-i-receive-the-following-error-when-i-enter-a-non-zero-value-in-the-pay-rate-field-the-value-is-out-of-its-valid-range--it-much-be-between-000-and-000" class="xliff"></a>
Du får denne meldingen fordi Nivå-feltet i Jobb-skjemaet er tomt for jobben som er tilknyttet den valgte stillingen.

Hvis du vil løse dette problemet, gjør du følgende:

> 1. Klikk Stilling-feltet på skjemaet Tilordninger for arbeiderstilling.  
> 2. Klikk jobbfeltverdien for å åpne jobbsiden.
> 3. Klikk Rediger i handlingsruten.
> 4. Klikk kategorien Kompensasjon.
> 5. Velg et nivå i Nivå-feltet.
> 6. Lukk jobbsiden.
> 7. Lukk stillingssiden.
> 8. Gå tilbake til kategorien Kompensasjon på arbeidersiden, og velg Fast kompensasjon.  Velg Nny og angi den ansattes stilling i stillingsfeltet.  Angir en verdi i Plan-feltet, og angi deretter den ansattes kompensasjon i feltet Lønnssats.

## Hvorfor kan jeg ikke endre gyldig dato i hodet i Arbeiderhandling-skjemaet?
<a id="why-cant-i-change-the-effective-date-in-the-header-of-the-worker-action-form" class="xliff"></a>
Du kan ikke endre gyldighetsdatoen fordi feltet fylles ut med den mest logiske datoen for handlingstypen.

For eksempel

- Ikrafttredelsesdatoen i overskriften til en **Avslutt en arbeider**-handling er datoen du anga i  **Avslutningsdato**-feltet.
- Ikrafttredelsesdatoen i overskriften til en **Ansett en arbeider**-handling er datoen du anga i feltet  **Startdato for ansettelse**.
- Ikrafttredelsesdatoen i overskriften til en **Overfør en arbeider**-handling er datoen du anga i feltet  **Startdato for tilordning** for arbeideren.


