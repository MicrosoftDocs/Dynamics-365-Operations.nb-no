---
title: Definer overføringsdokumentene for varebevegelse i et selskap
description: Denne fremgangsmåten viser hvordan du konfigurerer overføringsdokumenter for flytting av varer i et selskap.
author: AdamTrukawka
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
ms.openlocfilehash: 333c5b5e5cfa25e705c9864542517f8ec5532dfe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282342"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a>Definer overføringsdokumentene for varebevegelse i et selskap

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du oppretter overføringsdokumenter for flytting av varer i et selskap. Denne fremgangsmåten er bare tilgjengelig for juridiske enheter med hovedadresse i Litauen. Prosedyren ble opprettet med demonstrasjonsdatafirmaet DEMF med en primæradresse i Litauen. Før du kan fullføre denne prosedyren, må du fullføre fremgangsmåten Konfigurere overføringsdokumenter for flytting av varer i et selskap. Denne prosedyren er ment for lagerregnskapsførere. Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.


## <a name="create-a-transfer-order"></a>Opprett overføringsordre
1. Gå til Lagerstyring > Innkommende ordrer > Overføringsordre.
2. Klikk Ny.
3. Angi eller velg en verdi i feltet Fra lager.
4. Angi eller velg en verdi i feltet Til lager.
5. Klikk Legg til.
6. Merk den valgte raden i listen.
7. Angi eller velg en verdi i Varenummer-feltet.

## <a name="enter-transportation-details-for-the-transfer-order"></a>Angi transportdetaljer for overføringsordren
1. Klikk Lagre.
2. Klikk Send i handlingsruten.
3. Klikk Transportdetaljer.
4. Velg Ja i feltet Skriv ut transportdetaljer.
5. Angi eller velg en verdi i feltet Utstedte varer.
6. Skriv inn en verdi i feltet Pakke.
7. Skriv inn en verdi i feltet Risikonivå for lasten.
8. Angi eller velg en verdi i feltet Transportør.
9. Angi eller velg en verdi i feltet Modell.
10. Skriv inn en verdi i feltet Registreringsnummer.
11. Skriv inn en verdi i feltet Registreringsnummer for lastebil
12. Angi eller velg en verdi i feltet Sjåfør.
13. Skriv inn en verdi i feltet for sjåførnavn.
14. Klikk Lagre.
15. Lukk siden.

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a>Vise følgeseddelen for den uposterte overføringsordren
1. Klikk Følgeseddel.
2. Klikk OK.
3. Lukk siden.

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a>Vise følgeseddelen for den posterte overføringsordren
1. Klikk Overføringsordre i handlingsruten.
2. Klikk Send i handlingsruten.
3. Klikk Send overføringsordre.
4. Klikk kategorien Generelt.
5. Velg et alternativ i feltet Oppdater.
6. Klikk kategorien Oversikt.
7. Skriv inn en verdi i Følgeseddel-feltet.
8. Klikk OK.
9. Klikk Send i handlingsruten.
10. Klikk Følgeseddel.
11. Klikk OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
