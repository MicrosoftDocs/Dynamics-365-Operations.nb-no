---
title: Avbryt lagerarbeid for unntaksbehandling
description: Denne artikkelen beskriver funksjonen for arbeidsavbrudd som gjør at lagersjefer kan håndtere blokkert arbeid.
author: Mirzaab
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b1e2036e4e7a8a47d6df029f285df7aca0fa74e6
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403674"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Avbryt lagerarbeid for unntaksbehandling

[!include [banner](../includes/banner.md)]

Funksjonen for arbeidsavbrudd i Microsoft Dynamics 365 Supply Chain Management lar administratorbrukeren avbryte bestemt lagerarbeid som pågår, men som er blokkert av systemet eller ikke kan fullføres på grunn av eksepsjonelle omstendigheter. Denne funksjonaliteten er et attraktivt og sikkert alternativ til SQL-korrigerte skript som retter opp inkonsekvente data. Disse skriptene er som regel anmodet fra IT-medarbeidere, men funksjonen for arbeidsavbrudd kan også brukes av brukere i firmaet som har administratorrettigheter.

Du kan få tilgang til funksjonen for arbeidsavbrudd ved å gå til **Lagerstyring** \> **Periodiske oppgaver** \> **Opprydding \> Avbryt arbeid**. I dialogboksen **Avbryt arbeid** angir du arbeids-IDen for arbeidet som skal annulleres, og deretter velger du **OK**.

## <a name="warehouse-work-that-can-be-canceled"></a>Lagerarbeid som kan annulleres

Under lagerplukkinger, kan en arbeider støte på situasjoner der de har registrert antall som plukket fra en lagringslokasjon til brukerlokasjonen, men de kan ikke registrere plasseringsoperasjonen. Inkonsekvente lagerdata er ofte, men ikke alltid, årsaken til at arbeidet er blokkert.

I motsetning til den vanlige avbruddsfunksjonaliteten som du får tilgang til ved å bruke **Avbryt**-knappen i arbeidshodet, krever ikke funksjonen for arbeidsavbrudd at den siste fullførte arbeidslinjen er en arbeidslinje av typen **Plasser**. Med andre ord kan avbruddslogikken for funksjonen for arbeidsavbrudd kjøres selv om vareantallet på en arbeidslinje er på en brukerlokasjon.

> [!NOTE]
> For arbeid som må avbrytes av hensyn til driften, må lagerbrukere fortsette å bruke den vanlige avbruddsfunksjonaliteten på arbeidssiden.

Bare arbeid av typen **Salg**, **Utstedelse for overføring**, **Råvareplukking** eller **Etterfylling** kan avbrytes ved hjelp av funksjonen for arbeidsavbrudd. Avbruddslogikk vil ikke kjøres for plukkarbeid av fryste råvarer eller arbeid som kan avbrytes ved å bruke den vanlige avbruddsfunksjonaliteten (se den foregående merknaden).

Hvis du vil oppheve blokkeringen av arbeidet, avbryter systemet alle gjenværende arbeidslinjer og reparerer lagerdataene som er knyttet til arbeids-IDen som brukeren har angitt. Eventuelle vanlige lagerhåndteringsoperasjoner som involverer det berørte vareantallet, kan deretter fortsette.

Hvis du vil plassere den berørte varen på en bestemt lokasjon etter at arbeidet er annullert, må brukeren bruke en lagerbevegelse eller antallsjusteringsoperasjon på en mobil enhet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]