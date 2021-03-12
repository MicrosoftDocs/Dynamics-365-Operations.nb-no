---
title: Feilsøke reserveringer i lagerstyring
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lagerreservasjoner i Microsoft Dynamics 365 Supply Chain Management.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a1ea23059d56ebf387a95a1378e2a3cd47556d5f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993881"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>Feilsøke reserveringer i lagerstyring

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lagerreservasjoner i Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a>Jeg får følgende feilmelding: Reservasjoner kan ikke fjernes fordi det er opprettet arbeid som er avhengig av reservasjonen.

### <a name="issue-description"></a>Problembeskrivelse

Du kan ikke reservere lager på en salgslinje, fordi det er åpent arbeid mot linjen.

### <a name="issue-resolution"></a>Problemløsning

Undersøk om det finnes åpent emballasjegruppearbeid for å hente varen fra en pakkestasjon til en annen lokasjon (f.eks. *Rampedør*). Se gjennom postene på sidene **Logg over oppretting av arbeid** og **Arbeidsdetaljer** for å fastslå hva som fysisk reserverer lageret, og fullfør eller slett arbeidet for å frigjøre reservasjonen.

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a>Jeg får følgende feilmelding: Lagerantall -%1 kan ikke oppdateres på grunn av utilstrekkelige lagertransaksjoner for vare %2 ....

### <a name="issue-description"></a>Problembeskrivelse

Dette problemet kan oppstå hvis systemet ikke kan oppdatere et lagerantall, fordi det ikke finnes nok lagertransaksjoner som har de angitte dimensjonene. Her er hele teksten til hele feilmeldingen:

> Lagerantall -%1 kan ikke oppdateres på grunn av utilstrekkelige lagertransaksjoner for varen %2 med dimensjonsstørrelse = %3, farge = %4, tillegg = %5, område = %6, lager = %7, lokasjon = %8, lagerstatus = tilgjengelig, nummerskilt = %9, partinummer = %10 for referanse-ID %11 på parti-ID %12.

### <a name="issue-resolution"></a>Problemløsning

Kontroller at ingen lagertransaksjoner fysisk reserverer antallet. Disse transaksjonene kan for eksempel åpne kvalitetsordrer, lagerblokkeringsposter eller ordrer.

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a>Jeg får følgende feilmelding: Fysisk lagerbeholdning ... kan ikke reserveres fordi bare 0,00 er tilgjengelig på lageret.

### <a name="issue-description"></a>Problembeskrivelse

Dette problemet kan oppstå hvis systemet ikke kan oppdatere et lagerantall, fordi det ikke finnes nok lagertransaksjoner som har de angitte dimensjonene. Her er hele teksten til hele feilmeldingen:

> Fysisk lagerbeholdning område = %1, lager = %2, lagerstatus = tilgjengelig, partinummer = %3, eier = %4: %5 kan ikke reserveres fordi bare 0,00 er tilgjengelig på lageret.

### <a name="issue-resolution"></a>Problemløsning

Dette problemet skyldes sannsynligvis åpent arbeid. Du må enten fullføre arbeidet eller motta uten arbeidsoppretting. Kontroller at ingen lagertransaksjoner fysisk reserverer antallet. Disse transaksjonene kan for eksempel være åpne kvalitetsordrer, lagerblokkeringsposter eller ordrer.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Jeg får følgende feilmelding: For å tilordne bølge må lastlinjer angi dimensjonene over lokasjonen. Hvis du vil tilordne disse dimensjonene, må du reservere og opprette lastlinjen på nytt.

### <a name="issue-description"></a>Problembeskrivelse

Når du bruker en vare som har et parti over-reservasjonshierarki (med **Partinummer**-dimensjonen som er plassert *over* **Lokasjon**-dimensjonen), fungerer ikke kommandoen **Frigi til lager** på siden **Arbeidsområde for lastplanlegging** for et delvis antall. Du får denne feilmeldingen, og det opprettes ikke noe arbeid for det delvise antallet.

Hvis du imidlertid bruker en vare som har et parti under-reservasjonshierarki (med **Partinummer**-dimensjonen som er plassert *under* **Lokasjon**-dimensjonen), kan du frigi en last fra siden **Arbeidsområde for lastplanlegging** for et delvis antall.

### <a name="issue-resolution"></a>Problemløsning

Denne virkemåten er standard. Hvis du legger en dimensjon til over **Lokasjon**-dimensjonen i reservasjonshierarkiet, må den angis før frigivelse til lageret. Microsoft har evaluert dette problemet, og har funnet ut at det er en funksjonsbegrensning under frigivelser til lageret fra arbeidsområdet for lastplanlegging. Delvise antall kan ikke frigis hvis én eller flere dimensjoner over **Lokasjon** ikke er angitt.

Hvis du vil ha mer informasjon, kan du se [Fleksibel dimensjonsreservasjonspolicy for lagernivå](flexible-warehouse-level-dimension-reservation.md).
