---
title: Importere funksjoner fra det globale repositoriet
description: Denne artikkelen forklarer hvordan du importerer globaliseringsfunksjoner fra det globale repositoriet.
author: gionoder
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 5a72673e17c5653d43b60d3348d5518e09c40a15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278319"
---
# <a name="import-features-from-the-global-repository"></a>Importere funksjoner fra det globale repositoriet

[!include [banner](../includes/banner.md)]

Det globale repositoriet inneholder funksjoner for elektronisk fakturering som deles med konfigurasjonsleverandøren. Alle funksjoner for elektronisk fakturering fra Microsoft deles med alle firmaer. Du får automatisk tilgang til alle funksjonene for elektronisk fakturering som Microsoft utgir og publiserer i det globale repositoriet.

For å begynne å arbeide med funksjoner for elektronisk fakturering som deles med konfigurasjonsleverandøren, importerer du dem til forekomsten din av Regulatory Configuration Service (RCS) fra det globale repositoriet. Gå deretter gjennom funksjonsdetaljene, for eksempel konfigurasjonene og datasamlebåndene for behandling for elektronisk rapportering (ER).

## <a name="import-a-feature-from-the-global-repository"></a>Importer en funksjon fra det globale repositoriet

1. Logg på RCS-kontoen.
2. I arbeidsområdet **Globaliseringsfunksjon**, i **Funksjoner**-delen velger du flisen **Elektronisk fakturering**.
3. Velg **Importer** for å åpne oppslaget **Importer funksjon fra globalt repositorium**.
4. Hvis du vil bla gjennom funksjonene for elektronisk fakturering i det globale repositoriet som er tilgjengelige for en bestemt konfigurasjonsleverandør, synkroniserer du organisasjonens RCS-forekomst ved å velge **Synkroniser**. Etter at synkroniseringen er fullført, oppdateres listen over tilgjengelige funksjoner for elektronisk fakturering fra det globale repositoriet. Denne oppdateringen kan ta noen minutter.
5. Velg funksjonen som skal importeres, og velg deretter **Importer**.

Hvis du vil vise den importerte funksjonen for elektronisk fakturering, kontrollerer du at riktig konfigurasjonsleverandør er valgt. Funksjoner som ble opprettet av den aktive konfigurasjonsleverandøren, filtreres ut automatisk som standard. Du kan justere filteret for å vise funksjoner som ble opprettet av andre leverandører, for eksempel Microsofts konfigurasjonsleverandør.

Du kan nå arbeide med den importerte funksjonen. Du kan se gjennom detaljene og opprette en ny funksjon ved å bruke den importerte funksjonen som en mal.

> [!NOTE]
> Du kan bare endre en funksjon hvis den ble opprettet av konfigurasjonsleverandøren som er aktiv for øyeblikket. Du kan opprette en ny funksjon ved å bruke den opprinnelige funksjonen som basis. Du kan deretter gjøre de nødvendige endringene eller konfigurere parameterne.

Når Microsoft eller et annet firma som deler globaliseringsfunksjoner med firmaet ditt, oppdaterer funksjoner du har importert, kan du se etter oppdaterte versjoner ved å velge **Se etter funksjonsoppdateringer** i delen **Relaterte innstillinger** i arbeidsområdet **Globaliseringsfunksjoner**.

Hvis du ser oppdateringer for en funksjon du bruker som mal, kan du importere en ny versjon etter at du har synkronisert listen over publiserte funksjoner i det globale repositoriet.
