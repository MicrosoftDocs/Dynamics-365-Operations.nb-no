---
title: Definere og behandle gjentakende fakturaer
description: Denne artikkelen forklarer hvordan du konfigurerer og behandler gjentakende fakturaer. Du kan bruke gjentakende fakturaer hvis du må fakturere kunder for det samme beløpet regelmessig.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: roschlom
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b155d163c57f3c917b4d87fae7cbd737e7c45fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971609"
---
# <a name="set-up-and-process-recurring-invoices"></a>Definere og behandle gjentakende fakturaer

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du konfigurerer og behandler gjentakende fakturaer. Du kan bruke gjentakende fakturaer hvis du må fakturere kunder for det samme beløpet regelmessig.

<a name="create-a-recurring-free-text-invoice-template"></a>Opprette en mal for gjentakende fritekstfaktura
---------------------------------------------

Hvis du vil fakturere kunder for de samme tjenestene med jevne mellomrom, må du definere en mal for fritekstfaktura som kan brukes på nytt til å opprette fakturaene. Denne malen inneholder følgende informasjon:

-   Hodeinformasjon, for eksempel avgiftsgrupper, betalingsbetingelser og betalingsmåten
-   Linjeinformasjon, for eksempel tjenestebeskrivelse, inntektskontoer, enhetspris og fakturabeløp
-   Tillegg for levering eller håndtering
-   Regnskapsdistribusjoner sammen med informasjon om finansdimensjon, for eksempel kostsentre og forretningsenheter

Du oppretter i praksis en hel faktura og lagrer den som en mal. Du kan definere malene ved hjelp av siden **Gjentakende fakturaer**.

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a>Tilordne en mal for fritekstfaktura til en kunde og angi gjentakelsesdetaljer
Når malen er opprettet, må du tilordne den til kundene du vil fakturere. I tillegg må du angi når og hvor ofte fakturaen skal brukes. Du kan tilordne malene i **Faktura**-fanen på **Kunder**-siden. Legg til malen i listen, og oppdater følgende informasjon:

-   Startdatoen og eventuelt sluttdatoen for den gjentakende fakturaen
-   Frekvensen for den gjentakende faktureringen (for eksempel hver dag eller én gang i måneden)
-   Det maksimale faktureringsbeløpet (hvis denne informasjonen er nødvendig)

En kunde kan ha flere maler som har forskjellige frekvenser.

## <a name="generate-the-recurring-invoices"></a>Generere gjentakende fakturaer
På siden **Gjentakende fakturaer** er det en oppgave som behandler maler for gjentakende faktura. Du angir fakturadatoen og malen du vil generere fakturaer fra. Fakturaer genereres og tilordnes ett gjentakende ID-nummer for hver gruppe med fakturaer som behandles.

<a name="post-recurring-free-text-invoices"></a>Postere gjentakende fritekstfakturaer
---------------------------------

Når gjentakende fakturaer er generert, vises ID-ene for fakturagjentakelse i en posteringsoppgave på siden **Gjentakende fakturaer**. Du kan vise alle fakturaene for en gjentakelses- ID ved å klikke koblingen. Du kan slette enkeltfakturaer under gjennomgangen av fakturaer for gjentakelses-ID-en. Kundens innstillinger for gjentakelse tilbakestilles for denne malen, slik at den kan genereres på nytt senere. Du kan postere én, mange eller alle fakturaer for en gjentakelses-ID. Hvis arbeidsflyter er aktivert, må du klikke **Send** før du kan postere fakturaene.

<a name="print-recurring-free-text-invoices"></a>Skrive ut gjentakende fritekstfakturaer
----------------------------------

Når gjentakende fakturaer er postert, kan du skrive ut fakturaene på listesiden for fritekstfakturaer. Du kan skrive ut fakturaene som er valgt, eller du kan velge et område med fakturaer som skal skrives ut.



