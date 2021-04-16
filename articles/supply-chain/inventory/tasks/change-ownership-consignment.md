---
title: Endre eierskap for forsendelseslager basert på produksjonsbehov
description: Denne fremgangsmåten viser hvordan du endrer eieren av forsendelseslageret fra leverandøren til den juridiske enheten når det er behov for beholdningen i produksjonen.
author: perlynne
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6385fba0b6288416a85f1b7de73d3bb4972a852a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834127"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a>Endre eierskap for forsendelseslager basert på produksjonsbehov

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du endrer eieren av forsendelseslageret fra leverandøren til den juridiske enheten når det er behov for beholdningen i produksjonen. Denne endringen av eierskap gjøres ved å opprette og postere en endringsjournal for lagereierskap. Endringsjournallinjene for lagereierskap kan opprettes manuelt eller, som vist her, basert på eksisterende produksjonsbehov. Vanligvis utfører en arbeidsleder denne oppgaven. Du kan bruke denne fremgangsmåten i USMF-demodatafirmaet eller ved hjelp av dine egne data. Hvis du bruker dine egne data, må du kontrollere at følgende forutsetninger er tilstede: et lagerjournalnavn som har blitt definert for lagereierskapsendringen, fysisk registrerte leverandøreide varer på lager og én eller flere produksjonsordrelinjer for materialet. Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.

> [!NOTE]
> Utgående forsendelsesprosesser støttes ikke som standard, og automatisk behandling av eierskapsjournal støttes ikke.

## <a name="create-an-inventory-ownership-journal"></a>Opprette en lagereierskapsjournal
1. Gå til Lagerstyring > Journaloppføringer > Varer > Endring av lagereierskap.
2. Klikk på Ny.
    * Endringsjournalen for lagereierskap brukes til å endre eieren av forsendelseslageret fra leverandøren til gjeldende juridiske enhet. Denne endringen av eierskap gjøres ved å frigi lagerbeholdningen som eies av leverandøren. og deretter motta dette lageret i den gjeldende juridiske enheten.  
3. Angi eller velg en verdi i Navn-feltet.
    * Du kan bare velge lagerjournalnavn som har journaltypen Endring av eierskap.  
4. Klikk på OK.
5. Klikk på Funksjoner.
6. Klikk på Opprett journallinjer fra produksjonsordrer.
    * Du kan starte endringen av eierskapsprosessen ved å spørre alle produksjonslinjer som har behov for forbruk av råvarer.  
7. Velg et alternativ i feltet Lageravgangsstatus som skal inkluderes.
    * Dette alternativet gjør at du kan filtrere etter avgangsstatus for lagertransaksjonene. Du kan for eksempel opprette journallinjer for lager som har statusen Plukket og Fysisk reservert.  
8. Utvid delen Poster som skal inkluderes.
    * Denne delen lar deg bruke ekstra filtrering. Du kan for eksempel velge en bestemt råvaredato.  
9. Klikk på OK.

## <a name="post-the-inventory-ownership-change-journal"></a>Postere endringsjournalen for lagereierskap
1. Klikk på Poster.
    * Når journalen posteres, frigis det leverandøreide lageret ved hjelp referansen Endring av eierskap. Lageret blir deretter mottatt som på lager ved hjelp av en lagertransaksjon som oppdateres med en bestillingsmottaksseddel. Vær oppmerksom på at bare transaksjoner som er knyttet til den posterte journalen, opprettes. Ingen forventede lagertransaksjoner opprettes.  
2. Klikk på OK.
3. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]