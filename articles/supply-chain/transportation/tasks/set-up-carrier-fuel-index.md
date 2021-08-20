---
title: Definere en transportørdrivstoffindeks
description: Denne veiledningen viser hvordan du oppretter et område for drivstoffindeks, en drivstoffindeks og en drivstoffindeks for transportør.
author: ShylaThompson
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFuelIndexRegion,TMSCarrierFuelIndexTable,TMSFuelIndex
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 504c5143fac0e46f4d7be134d400ae53d999d25b1b364fe0278343b3d7664bf0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782329"
---
# <a name="set-up-a-carrier-fuel-index"></a>Definere en transportørdrivstoffindeks

[!include [banner](../../includes/banner.md)]

Denne veiledningen viser hvordan du oppretter et område for drivstoffindeks, en drivstoffindeks og en drivstoffindeks for transportør. Området for drivstoffindeks angir hvilket område drivstoffindeksen skal gjelde for, og drivstoffindeksen angir en drivstoffpris for en bestemt tidsperiode. Hvis du vil gjenspeile endringen i drivstoffpriser over tid, kan du knytte flere drivstoffindekser til en transportør.  Disse oppgavene utføres vanligvis av en transportkoordinator. Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.


## <a name="create-a-fuel-index-region"></a>Opprette et område for drivstoffindeks
1. Gå til Transportstyring > Oppsett > Drivstoffindekser > Områder for drivstoffindeks.
    * Først må du opprette ulike områder, der du arbeider og beregner ulike drivstofftillegg.  
2. Klikk på Ny.
3. Skriv inn en verdi i Område-feltet.
4. Skriv inn en verdi i Navn-feltet.
5. Klikk på Lagre.

## <a name="create-a-fuel-index"></a>Opprette en drivstoffindeks
1. Gå til Transportstyring > Oppsett > Drivstoffindekser > Drivstoffindekser.
    * Du må angi de gjeldende prisene for drivstoff for områdene du har definert.  
2. Klikk på Ny.
3. Klikk på rullegardinknappen i Område-feltet for å åpne oppslaget.
4. Klikk på koblingen i den valgte raden i listen.
5. Skriv inn et tall i feltet Pris per liter.
6. Angi dato og klokkeslett i feltet Effektiv startdato og effektivt startklokkeslett.
7. Klikk på Lagre.

## <a name="create-a-carrier-fuel-index"></a>Opprette en drivstoffindeks for transportør
1. Gå til Transportstyring > Oppsett > Drivstoffindekser > Drivstoffindekser for transportør.
2. Klikk på Ny.
3. Angi en verdi i feltet Drivstoffindeks for transportør.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk på Ny.
6. Angi dato og klokkeslett i feltet Effektiv startdato og effektivt startklokkeslett.
7. Angi et tall i feltet PPG fra.
    * I dette eksemplet kan du angi PPG fra-feltet som 1,95.  
8. I feltet PPG til angir du et tall.
    * I dette eksemplet kan du angi PPG til-feltet som 2.  
9. Angi et tall i Prosent-feltet.
    * I dette eksemplet kan du angi prosenten som 3.  
10. Klikk på rullegardinknappen i Valuta-feltet for å åpne oppslaget.
11. Finn og velg ønsket post i listen.
12. Klikk på koblingen i den valgte raden i listen.
13. Klikk på Lagre.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]