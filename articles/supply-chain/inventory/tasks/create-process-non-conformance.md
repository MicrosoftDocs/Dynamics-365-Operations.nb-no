---
title: Opprette og behandle et avvik
description: Dette emnet forklarer hvordan du utfører behandling av avvik, basert på en eksisterende kvalitetsordre.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bf20ed737707b7cf99023e3c78489caf4a68eab
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434672"
---
# <a name="create-and-process-a-conformance"></a>Opprette og behandle et avvik

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du utfører behandling av avvik, basert på en eksisterende kvalitetsordre. Du kan kjøre denne registreringen i USMF demofirmaet, og du kan bruke de foreslåtte verdiene. Denne prosedyren utføres vanligvis av en kvalitetsassistent.  Fullføring av instruksjonene i [Kontrollere varekvaliteten](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) er en forutsetning. Hvis du vil behandle godkjenningen av et avvik, må brukeren som kjører oppgaveregistreringen ha en "Navn"-verdi som er tilordnet på siden Brukere. Hvis du vil bruke merknader i dokumentet, må brukeren også ha Dokumenthåndtering aktivert i brukeralternativene.


## <a name="select-a-quality-order"></a>Velge en kvalitetsordre
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Periodiske oppgaver > Kvalitetsstyring > Kvalitetsordrer**.
2. I listen velger du kvalitetsordren som ble opprettet i [Kontrollere varekvaliteten](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).  

## <a name="create-a-nonconformance"></a>Opprette et avvik
1. Velg **Forespørsler** i handlingsruten.
2. Velg **Avvik**.
3. Velg **Ny**.
4. Velg problemet som ble funnet under inspeksjonen, i rullegardinmenyen for **Problemtype**-feltet.  
5. Velg **OK**.

## <a name="approvereject-a-nonconformance"></a>Godkjenne/avvise et avvik
1. Velg **Funksjoner**.
2. Velg **Godkjenn avvik**. Godkjenn avviket for dette eksemplet. Godkjente avvik kan knyttes til relaterte operasjoner for å registrere arbeid som utføres som en del av avvikshåndtering og, som i dette emnet, behandling av rettelseshandlingen.  
3. Velg **Ja**.

## <a name="create-a-correction-action"></a>Opprette en rettelseshandling
1. Velg **Rettelser**.
2. Velg **Ny**.
3. I **Personalnummer**-feltet i den nye raden velger du ønsket post fra rullegardinmenyen.
4. Klikk **Velg**.
5. Velg **Legg ved**. Opprett en merknad om rettelsen. I dette eksemplet er handlingen å kontakte leverandøren for å diskutere avvikssaken.  
6. Velg **Ny**.
7. Velg **Notat**. Avhengig av oppsettet for rapporten kan ulike dokumenttyper skrives ut på rapporter som er knyttet til behandling av avvik.  
8. Skriv inn en verdi i **Beskrivelse**-feltet.
9. Lukk siden.

## <a name="maintain-a-correction"></a>Vedlikeholde en korreksjon
1. Velg **Merk som fullført**.
2. Velg **OK**.
3. Lukk siden.

## <a name="close-a-nonconformance"></a>Lukke et avvik
1. Velg **Funksjoner**.
2. Velg **Lukk avvik**.
3. Velg **Ja**.
4. Lukk sidene.
