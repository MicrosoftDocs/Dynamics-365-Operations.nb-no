---
title: Feilsøke reserveringer i lagerstyring
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lagerreservasjoner i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5f3a9ab907c3cb0e6b99c414a78b6878bd5353274472c54e1f5eaf1d167f046a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773111"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>Feilsøke reserveringer i lagerstyring

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lagerreservasjoner i Microsoft Dynamics 365 Supply Chain Management.

For emner som er relatert til parti- og serienummerregistreringer, kan du se [Feilsøke lagerparti- og seriereserveringshierarkier](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
