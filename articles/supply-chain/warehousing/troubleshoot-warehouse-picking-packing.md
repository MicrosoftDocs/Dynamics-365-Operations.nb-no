---
title: Feilsøke plukking og pakking
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du plukker og pakker i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 74854fa95837dd8a133860e2a017be4c92ff84a3
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645483"
---
# <a name="troubleshoot-picking-and-packing"></a>Feilsøke plukking og pakking

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du plukker og pakker i Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a>Jeg får følgende feilmelding: Dimensjonslokasjonen kan ikke stå tom hvis dimensjonsserienummeret er angitt.

### <a name="issue-description"></a>Problembeskrivelse

Du får denne feilmeldingen hvis du oppretter en overføringsordre for en serievare ved hjelp av et lager som er aktivert for avansert lagerstyring (WMS), og etter at arbeidet er fullført, prøver du å bekrefte forsendelsen.

### <a name="issue-resolution"></a>Problemløsning

Feltet **Standard mottakssted** er tomt for et transittlager i fra-lageret. Du kan løse dette problemet ved å angi en standard mottakssted i transittlageret. Kontroller at denne plasseringen er nummerskiltkontrollert.

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a>Jeg får følgende feilmelding: Ugyldig nummerskilt.

### <a name="issue-description"></a>Problembeskrivelse

Du får denne feilmeldingen i lagerappen når du skanner en nummerskilt-ID.

### <a name="issue-resolution"></a>Problemløsning

Kontroller at det finnes en nummerskilt-ID i nummerskilttabellen, og at varene og antallene på nummerskiltet er tilgjengelige (med andre ord de er ikke blokkert).

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a>Jeg får følgende feilmelding: Feltet Lastvekt (=-%1) kan bare inneholde positive tall. Oppdateringen er avbrutt.

### <a name="issue-description"></a>Problembeskrivelse

Du får denne feilmeldingen hvis det er åpent arbeid når du behandler arbeid fra emballasjelokasjoner til oppsamlingslokasjoner, eller fra oppsamlingslokasjoner til forankringslokasjoner.

### <a name="issue-resolution"></a>Problemløsning

Hvis du vil løse dette problemet, går du til **Systemadministrasjon \> Periodiske oppgaver \> Database \> Konsekvenskontroll** og kjører prosessen for **Konsekvenskontroll av lagerlastvekt**.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Jeg får følgende feilmelding: Antallet er ikke gyldig for enhet %1.

### <a name="issue-description"></a>Problembeskrivelse

Du får denne feilmeldingen når du prøver å utføre en *delt plukking* på tvers av flere partier.

### <a name="issue-resolution"></a>Problemløsning

Lagerarbeideren må bruke *Plukking med mangler*-prosessen i lagerappen. Hvis du prøver å plukke flere partier fra samme lokasjon, kan du også bruke **Fullstendig**-alternativet i lagerappen.

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a>Jeg kan ikke flytte lager til en lokasjon som er nummerskiltkontrollert.

### <a name="issue-description"></a>Problembeskrivelse

Du kan ikke redusere plukket antall på en last.

### <a name="issue-resolution"></a>Problemløsning

I tidligere versjoner kan du ikke redusere plukket antall på en last. Du kan imidlertid nå legge tilbake til en nummerskiltkontrollert lokasjon. Du må angi både en **Lokasjon**-verdi og en **Nummerskilt**-verdi for lastlinjen på siden **Reduser plukket antall**.

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a>Kan jeg skrive ut en følgeseddel eller pakkeinnhold etter lager?

### <a name="issue-description"></a>Problembeskrivelse

Du vil skrive ut en følgeseddel eller pakkeinnhold etter lager eller område på siden **Oppdatering av revisjonsmallinje**.

### <a name="issue-resolution"></a>Problemløsning

Når du skriver ut et dokument ved hjelp av innstillinger for utskriftsbehandling, begrenser du området (område/lager) til utskriftsbehandling i stedet for å velge **Rediger utskriftsinnstillinger** på siden **Oppgradering av revisjonsmallinje**.

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Jeg kan ikke avbryte en følgeseddel etter at den er postert fra en salgsordre.

### <a name="issue-description"></a>Problembeskrivelse

Når plukk- og leveringsprosesser er aktivert for WMS, kan du ikke avbryte en følgeseddel etter at den er postert fra en salgsordre.

### <a name="issue-resolution"></a>Problemløsning

Hvis du vil korrigere posterte følgesedler for varer som er aktivert for WMS, må du utføre posteringen fra lasten, ikke direkte fra ordren. Microsoft har evaluert dette problemet og har funnet ut at det er en funksjonsbegrensning. Vanligvis kan en salgsordre som er plukket og sendt gjennom lagerstyringsprosesser, følgeseddeloppdateres fra lasten eller forsendelsen og selve salgsordredokumentet. Hvis du imidlertid følgeseddeloppdaterer salgsordren fra salgsordredokumentet, kan fremdeles ikke følgeseddeltilbakeføring utføres fra lasten eller salgsordren. Derfor anbefaler vi at du bruker følgeseddelposteringen fra lasten. I dette tilfellet blir tilbakeføringen som må gjøres fra lasten, aktivert.

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a>Jeg får følgende feilmelding: Finner ikke nok arbeid for gruppen.

### <a name="issue-description"></a>Problembeskrivelse

Når du bruker prosessen *Systemkontrollert gruppeplukking*, hvis du konfigurerer en gruppeprofil der for eksempel 10 stillinger kan plukkes, fungerer prosessen som planlagt når det er nok arbeid til å plukke til 10 stillinger. Men hvis det bare er åtte stillinger som skal plukkes, får du denne feilmeldingen fordi det ikke er nok arbeid for én gruppe.

### <a name="issue-resolution"></a>Problemløsning

Du kan løse dette problemet ved å redigere gruppeprofilen og sette **Aktiver stillinger**-alternativet til *Nei*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]