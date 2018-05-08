---
title: Opprette og behandle et avvik
description: "Bruk denne fremgangsmåten til å utføre behandling av avvik, basert på en eksisterende kvalitetsordre."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e5187c44aac881273900b2fc0ca91045a65cd838
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-process-a-conformance"></a>Opprette og behandle et avvik

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bruk denne fremgangsmåten til å utføre behandling av avvik, basert på en eksisterende kvalitetsordre. Du kan kjøre denne registreringen i USMF demofirmaet, og du kan bruke de foreslåtte verdiene. Denne prosedyren utføres vanligvis av en kvalitetsassistent.  Kjør oppgaveregistreringen "Kontrollere varekvaliteten" er en forutsetning. Hvis du vil behandle godkjenningen av et avvik, må brukeren som kjører oppgaveregistreringen ha en "Navn"-verdi som er tilordnet på siden Brukere. Hvis du vil bruke merknader i dokumentet, må brukeren også ha Dokumenthåndtering aktivert i brukeralternativene.


## <a name="select-a-quality-order"></a>Velge en kvalitetsordre
1. Gå til Kvalitetsordrer.
2. Merk den valgte raden i listen.
    * Velg kvalitetsordren som ble opprettet fra oppgaveregistrering Kontrollere varekvaliteten.  

## <a name="create-a-nonconformance"></a>Opprette et avvik
1. Klikk Forespørsler.
2. Klikk Avvik.
3. Klikk Ny.
4. Klikk rullegardinknappen i feltet Problemtype for å åpne oppslaget.
    * Velg problemet som ble funnet under inspeksjonsprosessen.  
5. Klikk rullegardinknappen i feltet Problemtype for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
7. Klikk koblingen i den valgte raden i listen.
8. Klikk OK.

## <a name="approvereject-a-nonconformance"></a>Godkjenne/avvise et avvik
1. Klikk Funksjoner.
2. Klikk Godkjenn avvik.
    * Godkjenn avviket for dette eksemplet. Godkjente avvik kan knyttes til relaterte operasjoner for å registrere arbeid som utføres som en del av avvikshåndtering og, som i denne oppgaveregistreringen, behandling av rettelseshandlingen.  
3. Klikk Ja.

## <a name="create-a-correction-action"></a>Opprette en rettelseshandling
1. Klikk Rettelser.
2. Klikk Ny.
3. Merk den valgte raden i listen.
4. Klikk rullegardinknappen i feltet Personalnummer for å åpne oppslaget.
5. Klikk koblingen i den valgte raden i listen.
6. Klikk Velg.
7. Klikk Vedlegg.
    * Opprett en merknad om rettelsen. I dette eksemplet er handlingen å kontakte leverandøren for å diskutere avvikssaken.  
8. Klikk Ny.
9. Klikk Notat.
    * Legg merke til at, avhengig av oppsettet for rapporten, kan ulike dokumenttyper skrives ut på rapporter som er knyttet til behandling av avvik.  
10. Skriv inn en verdi i feltet Beskrivelse.
11. Lukk siden.

## <a name="maintain-a-correction"></a>Vedlikeholde en korreksjon
1. Klikk Merk som fullført.
2. Klikk OK.
3. Lukk siden.

## <a name="close-a-nonconformance"></a>Lukke et avvik
1. Klikk Funksjoner.
2. Klikk Lukk avvik.
3. Klikk Ja.
4. Lukk siden.
5. Lukk siden.

