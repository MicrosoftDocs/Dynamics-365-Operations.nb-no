---
title: Forskuddsbetalte fakturaer i forhold til forskuddsbetalinger
description: "Denne artikkelen inneholder beskriver og viser forskjellene mellom de to metodene som organisasjoner kan bruke for forskuddsbetaling. Med den ene metoden oppretter du en forskuddsbetalt faktura som er knyttet til en bestilling. Med den andre metoden oppretter du journalbilag for forskuddsbetaling ved å lage journaloppføringer og merke dem som journalbilag for forskuddsbetaling."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c4f127007cea1d8ccd0b4e9ea637f0674775278d
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="prepayment-invoices-vs-prepayments"></a>Forskuddsbetalte fakturaer i forhold til forskuddsbetalinger

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder beskriver og viser forskjellene mellom de to metodene som organisasjoner kan bruke for forskuddsbetaling. Med den ene metoden oppretter du en forskuddsbetalt faktura som er knyttet til en bestilling. Med den andre metoden oppretter du journalbilag for forskuddsbetaling ved å lage journaloppføringer og merke dem som journalbilag for forskuddsbetaling.

Organisasjoner kan utstede forskuddsbetalinger til leverandører for varer eller tjenester før varene eller tjenestene er oppfylt. To metoder kan brukes til å utstede forskuddsbetalinger til leverandører. Hvis du vil redusere risikoen, kan du spore forskuddsbetalinger ved å definere forskuddsbetalingen på en bestilling. For denne metoden må du opprette en forskuddsbetalt faktura som er knyttet til en bestilling. Denne metoden kalles forskuddsfakturering. Organisasjoner som ikke vil følge opp forskuddsbetalinger så tett, eller ikke mottar en forskuddsbetalt faktura fra leverandøren, kan bruke journalbilag for forskuddsbetaling i stedet for faktureringsmåten forskuddsbetaling. Du kan opprette journalbilag for forskuddsbetaling ved å lage journaloppføringer og merke dem som journalbilag for forskuddsbetaling. Du kan ikke spore hvilke forskuddsbetalinger til en leverandør som gjøres mot hvilke bestillinger for denne metoden. Du kan imidlertid merke en postert forskuddsbetaling for utligning mot en bestilling.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Når du bruker forskuddsfakturering i forhold til forskuddsbetalinger
| Forskuddsfakturering                                                                | Forskuddsbetalinger                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Definer en verdi for forskuddsbetaling på bestillingen.                                    | Ingen verdi for forskuddsbetaling er definert på bestillingen.                    |
| Nøkkel: En Forskuddsbetalt faktura og en sluttfaktura må posteres.                       | Ingen forskuddsfaktura må posteres.                                    |
| Ansvar for forskuddsbetalingen holdes på kontoen for forskuddsbetaling, ikke AP-kontoen. | Ansvar for forskuddsbetalingen holdes på AP-kontoen.                  |
| Leverandørsaldoen gjenspeiler ikke verdien forskuddsbetaling gjennom hele prosessen.     | Leverandørsaldoen gjenspeiler verdien forskuddsbetaling gjennom hele prosessen. |
| Forskuddsfakturering er bare tilgjengelig på leverandører.                         | Forskuddsbetalinger er tilgjengelig i Leverandører og Kunder.    |

## <a name="overview-of-the-prepayment-process"></a>Oversikt over forhåndsbetalingsprosessen
Regnskapspraksis i mange land/regioner krever at forskuddsbetaling (betalinger på forhånd) fra en kunde eller til en leverandør ikke posteres til de vanlige samlekontoene for kunden eller leverandøren. I stedet posteres disse forskuddbetalingene til spesielle økonomikontoer for forskuddsbetalinger. Når en salgsordre eller en bestilling opprettes, utstedes en faktura til kunden eller fra leverandøren. Når fakturaen betales, tilbakeføres forskuddbetalinger og forskuddbetalingsbilag av mva i finanskontoene for forskuddbetaling, og fakturabeløpene posteres automatisk til de vanlige samlekontoene. Hvis du vil opprette en forskuddsbetaling, gjør du følgende:

1.  Definer en posteringsprofil for forskuddsbetalinger.
2.  I Kundeparametere og Leverandørparametere, under **Finans og merverdiavgift**, velger du den nye posteringsprofilen ved hjelp av parameteren **Posteringsprofil for betalingsjournal med forskuddsbetaling**.
3.  Opprett en betalingsjournal, og opprett deretter den nye betalingen.
4.  Du kan flagge betalingen som en forskuddsbetaling. Hvis en betaling er flagget som en forskuddsbetaling, posteres betalingen til finanskontoer som er definert i posteringsprofilen som du definerer i trinn 1 og 2. Hvis betalingen er flagget som en forskuddsbetaling, beregnes også skatt. Noen myndigheter krever at avgiftene betales når det registreres en forskuddsbetaling, selv om det ikke er en faktura.
5.  Poster forskuddsbetalingen.
6.  Valgfritt: Du kan utligne forskuddsbetalingen mot bestillingen eller salgsordren før du oppretter fakturaen. I handlingsruten på salgsordre- eller bestillingssiden bruker du **Utlign transaksjoner**.
7.  Når leverandøren leverer varene eller tjenestene, kan du registrere fakturaen. Hvis du har utlignet forskuddsbetalingen mot bestillingen eller salgsordren i trinn 6, utlignes automatisk forskuddsbetalingen mot fakturaen som du opprettet. Hvis du ikke utlignet forskuddsbetalingen mot bestillingen eller salgsordren, kan du manuelt utligne den mot fakturaen ved hjelp av **Utlign transaksjoner** på kunde- eller leverandørsiden. Forskuddsbetalingsbeløpet tilbakeføres deretter ut fra den midlertidig AP/AR-finanskontoen. I tillegg, hvis merverdiavgift er beregnet, tilbakestilles de fordi fakturaen har de faktiske mva-beløpene.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Oversikt over forskuddsfaktureringsprosessen
Forskuddsbetalte fakturaer er vanlig forretningspraksis. En leverandør sender forskuddsbetalte fakturaer for å kreve et innskudd på innkjøpet før bestillingen er oppfylt. Noen leverandører krever for eksempel en forskuddsbetaling for tilpassede varer eller tjenester. Hvis en leverandør sender en faktura som ber om forskuddsbetaling, kan du bruke funksjonen for forskuddsfakturering. En verdi for forskuddsbetaling kan defineres i bestillingen, en forskuddsbetalt faktura registreres og betales, og deretter brukes forskuddsfakturaen på den endelige fakturaen. Hvis du vil opprette en forskuddsbetaling, gjør du følgende:

1.  Innkjøpsagenten oppretter, bekrefter og sender deretter en bestilling som leverandøren har bedt om forskuddsbetaling for. Verdien for forskuddsbetaling defineres i bestillingen som en del av avtalen.
2.  Leverandøren sender en forskuddsbetalt faktura.
3.  Leverandørkoordinatoren registrerer den forskuddsbetalte fakturaen mot bestillingen, og deretter betales den forskuddsbetalte fakturaen.
4.  Når leverandøren har levert varene eller tjenestene, og de tilknyttede leverandørfakturaene er mottatt, bruker leverandørkoordinatoren forskuddsbetalingsbeløpet som allerede er betalt mot fakturaen.
5.  Leverandørkoordinatoren betaler og utligner det gjenstående beløpet på fakturaen.





