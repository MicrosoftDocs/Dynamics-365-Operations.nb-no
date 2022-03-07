---
title: Vanlige spørsmål om personalhandlinger
description: Dette emnet inneholder svar på spørsmål du kan ha hvis organisasjonen bruker personalhandlinger.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: c952bdc95b49c92fea34aef63b57c7e193b2f09a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065157"
---
# <a name="personnel-actions-faq"></a>Vanlige spørsmål om medarbeiderhandlinger


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet inneholder svar på spørsmål du kan ha hvis organisasjonen bruker personalhandlinger. Personalhandlinger er flere trinn du må fullføre når du utfører bestemte personalrelaterte oppgaver. 

Eksempler på oppgaver som kan kreve personalhandlinger, er:
 - Når du oppretter nye stillinger. 
 - Når du endrer eksisterende stillingsverdier. 
 - Når du ansetter nye arbeidere. 
 - Når du overfører arbeiderer. 
 - Når du endrer arbeiderkompensasjon. 
 - Når du endrer stillingstilordninger. 
 - Når du sier opp arbeidere.

> [!NOTE]
> Personalhandlinger er kun tilgjengelig hvis feltene **Aktiver ansatthandlinger** og **Aktiver stillingshandlinger** er satt til **Ja** i kategorien **Personalhandlinger** på siden **Delte parametere for personaladministrasjon**. 

## <a name="how-can-i-tell-if-my-organization-requires-personnel-actions"></a>Hvordan vet jeg om organisasjonen krever personalhandlinger?
Personalhandlinger er nødvendige for organisasjonen hvis du blir bedt om å velge en personalhandling når du oppretter nye stillinger, endrer eksisterende stillinger, ansetter nye arbeidere, overførr arbeidere, endrer arbeideres kompensasjon, endrer stillingstilordninger, sier opp arbeidere eller angir permisjon for arbeidere. 

## <a name="what-is-the-difference-between-a-position-action-and-a-worker-action"></a>Hva er forskjellen mellom en stillingshandling og arbeiderhandlingen?
Det er to typer personalhandlinger:

- **Stillingshandling** – En stillingshandling utføres på eksisterende stillinger eller nye stillinger. En stillingshandling kan for eksempel være nødvendig hvis du endrer en verdi i en eksisterende stilling, eller hvis du oppretter en ny sesongstilling. 

- **Arbeiderhandling** – En arbeiderhandling er utført på eksisterende ansatte eller nye ansatte. En arbeiderhandling kan for eksempel være nødvendig når en ny ansatt ansettes eller en eksisterende ansatt forfremmes. 

## <a name="what-do-the-statuses-of-the-personnel-actions-mean"></a>Hva betyr statusene til personalhandlingene?
Personalhandlinger kan ha følgende status:

- **Utkast** – Hvis arbeidsflyt brukes, vil handlingen ikke sendt. Hvis arbeidsflyt ikke brukes, er ikke handlingen fullført.
- **Til vurdering**– Personalhandlingen er sendt til arbeidsflyten, men arbeidsflyten er ikke fullført.
- **Godkjente venter** – Arbeidsflyten er fullført, men endringene pågår fortsatt. **Avbrutt** – Arbeidsflyten ble avbrutt, eller personalhandlingen ble kalt tilbake. **Avvist** – Handlingsforespørselen ble avvist av godkjenneren.
- **Behandler handling** – Handlingsforespørselen er godkjent, og endringene behandles.
- **Arbeidsflyt fullført**  – Arbeidsflyten er fullført, og endringene er behandlet. **Mislykket** – Arbeidsflyten mislyktes fordi informasjonen er for gammel. Klikk på **Aktiver på nytt** for å vise den nyeste informasjonen og fortsette.
- **Fullført**– Stillingen ble opprettet eller endret uten feil, eller den ansatt ble ansatt, overført eller avsluttet uten feil, eller har fått endret kompensasjon. **Feil** – Det oppstod et annet problem enn at informasjonen var utdatert. Åpne **Meldingslogg for personalhandlinger** for å finne årsaken til feilen.
- **Avslått** – Handlingsforespørselen ble avvist av godkjenneren.

## <a name="can-i-delete-a-personnel-action"></a>Kan jeg slette en personalhandling?
Ja, du kan slette personalhandlinger som har statusen **Utkast**, **Feil**, **Mislykket** eller **Avbrutt**. Du kan bare slette personalhandlinger som har statusen **Fullført**, hvis du har angitt alternativet **Tillat sletting av fullførte arbeiderhandlinger** til **Ja** på siden **Delte parametere for Human Resources**.

## <a name="what-is-the-fastest-way-to-check-the-status-of-a-personnel-action-request"></a>Hva er den raskeste metoden for å kontrollere statusen for en forespørsel om personalhandling?
Åpne en av listesidene for **personalehandling**, og velg en personalehandling.

## <a name="what-should-i-do-if-a-personnel-action-request-fails"></a>Hva gjør jeg hvis en forespørsel for personalhandling mislykkes?
Hvis en forespørsel om personalhandling mislykkes, følger du denne fremgangsmåten for å rette feilen og sende forespørselen på nytt:

> 1. Klikk **Feiltekst**-knappen i **handlingsruten** for å vise meldingsteksten som beskriver problemet.
> 
> 2. Klikk **Aktiver på nytt** i **handlingsruten** for å laste inn den nyeste informasjonen og sette statusen for personalhandlingen tilbake til **Utkast**.
> 
> 3. Rett opp feilen, og klikk deretter **Fullført** eller **Send inn**.

## <a name="what-happens-to-a-personnel-action-that-uses-workflow-when-the-final-approval-is-completed"></a>Hva skjer med en personalhandling som bruker arbeidsflyt når den endelige godkjenningen er fullført?
Hvis det ikke finnes feil, blir personalhandlingen skrivebeskyttet. (Du kan vise loggen i på listesiden **Alle arbeiderhandlinger**, men du kan ikke endre personalhandlingen.) Når statusen til en personalhandling er **fullført**, er stillingen eller arbeiderposten allerede oppdatert. Hvis du vil vise endringene som ble utført, åpner du listesiden **Stillinger** eller **Arbeidere**.

## <a name="why-do-i-receive-the-following-error-when-i-enter-a-non-zero-value-in-the-pay-rate-field-the-value-is-out-of-its-valid-range--it-much-be-between-000-and-000"></a>Hvorfor får jeg følgende feil når jeg angir en annen verdi enn null i Lønnssats-feltet? «Verdien er utenfor gyldig område – den må være mellom 0,00 og 0,00»
Du får denne meldingen fordi **Nivå**-feltet på **Jobb**-siden er tomt for jobben som er tilknyttet den valgte stillingen.

Hvis du vil løse dette problemet, gjør du følgende:

> 1. Klikk på **Stilling**-feltet på siden **Tilordninger for arbeiderstilling**.  
> 2. Klikk på **Jobb**-feltverdien for å åpne **Jobb**-siden.
> 3. Klikk på **Rediger** i handlingsruten.
> 4. Klikk på **Kompensasjon**-fanen.
> 5. Velg et nivå i **Nivå**-feltet.
> 6. Lukk **Jobb**-siden.
> 7. Lukk **Stilling**-siden.
> 8. Gå tilbake til **Kompensasjon**-fanen på **Arbeider**-siden, og velg **Fast kompensasjon**.  Velg **Ny**, og angi den ansattes stilling i **Stilling**-feltet.  Angir en verdi i **Plan**-feltet, og angi deretter den ansattes kompensasjon i feltet **Lønnssats**.

## <a name="why-cant-i-change-the-effective-date-on-the-header-of-the-worker-action-page"></a>Hvorfor kan jeg ikke endre gyldig dato i hodet på Arbeiderhandling-siden?
Du kan ikke endre gyldighetsdatoen fordi feltet fylles ut med den mest logiske datoen for handlingstypen.

For eksempel

- Ikrafttredelsesdatoen i overskriften til en **Avslutt en arbeider**-handling er datoen du anga i  **Avslutningsdato**-feltet.
- Ikrafttredelsesdatoen i overskriften til en **Ansett en arbeider**-handling er datoen du anga i feltet  **Startdato for ansettelse**.
- Ikrafttredelsesdatoen i overskriften til en **Overfør en arbeider**-handling er datoen du anga i feltet  **Startdato for tilordning** for arbeideren.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
