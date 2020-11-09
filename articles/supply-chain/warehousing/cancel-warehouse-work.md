---
title: Avbryte lagerarbeid for unntaksbehandling
description: Dette emnet beskriver Avbryt arbeid-funksjonen som gjør det mulig for lagersjefer å håndtere blokkert arbeid.
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: daa8f0d19de75e6c126fe7a5fe312bca24c89bdc
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016247"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Avbryte lagerarbeid for unntaksbehandling

[!include [banner](../includes/banner.md)]

Funksjonen Avbryt arbeid i Microsoft Dynamics 365 Supply Chain Management lar administratorbrukeren avbryte bestemt lagerarbeid som pågår, men som er blokkert av systemet eller ikke kan fullføres på grunn av eksepsjonelle omstendigheter. Denne funksjonaliteten er et attraktivt og sikkert alternativ til SQL-korrigerte skript som retter opp inkonsekvente data. Disse skriptene er som regel anmodet fra IT-medarbeidere, men kan også brukes av brukere i firmaet som har administratorrettigheter.

Du kan få tilgang til Avbryt arbeid-funksjonen ved å gå til **Lagerstyring** \> **Periodiske oppgaver** \> **Opprydding \> Avbryt arbeid**. I dialogboksen **Avbryt arbeid** angir du arbeids-IDen for arbeidet som skal annulleres, og deretter velger du **OK**.

## <a name="warehouse-work-that-can-be-canceled"></a>Lagerarbeid som kan annulleres

Under lagerplukkinger, kan en arbeider støte på situasjoner der de har registrert antall som plukket fra en lagringslokasjon til brukerlokasjonen, men de kan ikke registrere plasseringsoperasjonen. Inkonsekvente lagerdata er ofte, men ikke alltid, årsaken til at arbeidet er blokkert.

I motsetning til den vanlige Avbryt-funksjonaliteten som du får tilgang til ved å bruke **Avbryt** -knappen i arbeidshodet, krever ikke funksjonen Avbryt arbeid at den siste fullførte arbeidslinjen er en arbeidslinje av typen **Plasser**. Med andre ord, for å avbryte Avbryt arbeid-funksjonen, kan annulleringslogikken kjøres selv om vareantallet på en arbeidslinje er på en brukerlokasjon.

> [!NOTE]
> For arbeid som må avbrytes av hensyn til driften, må lagerbrukere fortsette å bruke den vanlige Avbryt-funksjonaliteten på arbeidssiden.

Bare arbeid av typen **Salg** , **Utstedelse for overføring** , **Råvareplukking** eller **Etterfylling** kan annulleres ved hjelp av funksjonen Avbryt arbeid. Annulleringslogikk vil ikke kjøres for plukkarbeid av fryste råvarer eller arbeid som kan avbrytes ved å bruke den vanlige Avbryt-funksjonaliteten (se den foregående merknaden).

Hvis du vil oppheve blokkeringen av arbeidet, avbryter systemet alle gjenværende arbeidslinjer og reparerer lagerdataene som er knyttet til arbeids-IDen som brukeren har angitt. Eventuelle vanlige lagerhåndteringsoperasjoner som involverer det berørte vareantallet, kan deretter fortsette.

Hvis du vil plassere den berørte varen på en bestemt lokasjon etter at arbeidet er annullert, må brukeren bruke en lagerbevegelse eller antallsjusteringsoperasjon på en mobil enhet.
