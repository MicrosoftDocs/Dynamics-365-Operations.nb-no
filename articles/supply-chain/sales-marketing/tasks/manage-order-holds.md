---
title: Behandle ordresperrer
description: Denne fremgangsmåten forklarer hvordan du plasserer salgsordrer for kunden på vent, hvordan du arbeider med ordresperreutsjekkinger og fjerner ordresperrer.
author: omulvad
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38e5ea0dcec84704c9674412d12d0e857459975b3e928467a76e9fa677f6cbc1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771305"
---
# <a name="manage-order-holds"></a>Behandle ordresperrer

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten forklarer hvordan du plasserer salgsordrer for kunden på vent, hvordan du arbeider med ordresperreutsjekkinger og fjerner ordresperrer. En ordre kan settes på vent av en rekke ulike årsaker. Du kan for eksempel sperre en ordre til kundens adresse eller betalingsmetode kan bekreftes, eller til en leder kan gå gjennom kundens kredittgrense. Mens ordren er på vent, kan den ikke behandles av lageret for forsendelse. 

Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.


## <a name="set-up-order-holds"></a>Definer ordresperrer
1. Gå til **Navigasjonsrute > Moduler > Salg og markedsføring > Oppsett > Salgsordrer > Ordresperrekoder**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i **Sperrekode**-feltet. Skriv for eksempel inn Ring tilbake.  
4. Skriv inn en verdi i **Beskrivelse**-feltet.
    - For eksempel Ordre sperret i påvente av at kunden ringer tilbake.  
    - Du kan også merke av for **Fjernede reservasjoner** for å fjerne fysiske reservasjoner fra ordren når denne sperrekoden legges til.  
5. Klikk på **Lagre**.

## <a name="place-order-on-hold"></a>Sett ordre på vent
1. Gå til **Navigasjonsrute > Moduler > Salg og markedsføring > Salgsordrer > Alle salgsordrer**.
2. Klikk på **Ny**.
3. Angi eller velg en verdi i **Kundekonto**-feltet.
4. Klikk på **OK**.
5. Angi eller velg en verdi i **Varenummer**-feltet.
6. Angi et tall i **Antall**-feltet.
7. Klikk på **Salgsordre** i **handlingsruten**.
8. Klikk på **Ordresperrer**.
9. Klikk på **Ny**.
10. Velg koden du har opprettet i den forrige underoppgaven, i **Sperrekode**-feltet.
11. Klikk på **Lagre**.
12. Lukk siden.
13. Gå til **Salg og markedsføring > Salgsordrer > Alle salgsordrer**.
14. Merk den valgte raden i listen. Ordrer som er på vent, har feltene "Ikke behandle" og "Vent" merket av.
15. Klikk på **Plukk og pakk** i handlingsruten.

## <a name="manage-order-holds"></a>Behandle ordresperrer
1. Gå til **Salg og markedsføring > Salgsordrer > Åpne ordrer > Ordresperrer**. Siden **Ordresperrer** fungerer som et arbeidsområde der du kan få en oversikt over alle gjeldende og behandlede sperrer, og behandle dem og tilknyttede salgsordrer.     
2. Merk den valgte raden i listen.
3. Klikk på **Sperre - utsjekking** i **handlingsruten**.
4. Klikk på **Sjekk ut**.
5. Fjern merket for den valgte raden i listen. Feltet **Sjekk ut til** viser nå bruker-ID-en din.   
6. Klikk på **Fjern utsjekking**.
7. Klikk på **Fjern sperre** i **handlingsruten**.
    - Når du er klar til å fjerne sperren og la ordren gå videre til neste trinn i fullføringen, må du fjerne sperren. Hvis ordren ikke krever noen endringer, kan du kjøre Fjern sperrer-handlingen. Du kan imidlertid bruke Fjern og endre-handlingen hvis ordren må oppdateres når du fjerner en sperre.      
    - **Fjern og send**-handlingen gjelder bare når du bruker Telefonsenterfunksjonalitet.  
8. Klikk på **Fjern sperrer**. Sperringen er nå fjernet fra ordren og fjernet fra listen over aktive sperringer. Hvis du vil se alle sperringene eller delsettet i henhold til en bestemt status, kan du endre verdien i Vis-feltet.     



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]