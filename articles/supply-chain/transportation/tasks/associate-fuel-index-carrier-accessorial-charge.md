---
title: Knytte en indeks for drivstoff til en operatør som et tilbehørsgebyr
description: Denne håndboken beskriver hvordan du oppretter en tilbehørstilordning, transportørens tilbehørsgebyr, tilbehørsmal for drivstofftillegg og knytter en drivstoffindeks for transportør til en transportør.
author: Weijiesa
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2df77fe94156e2b60b77fa1c995ea10eab048a0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670559"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a>Knytte en indeks for drivstoff til en operatør som et tilbehørsgebyr

[!include [banner](../../includes/banner.md)]

Denne håndboken beskriver hvordan du oppretter en tilbehørstilordning, transportørens tilbehørsgebyr, tilbehørsmal for drivstofftillegg og knytter en drivstoffindeks for transportør til en transportør. Du må ha definert en drivstoffindeks for transportør før du kjører denne håndboken. Du kan bruke veiledningen Definere transportørdrivstoffindeks til å gjøre dette. Disse oppsettoppgaver utføres vanligvis av prosjektleder logistikk. Demonstrasjonsdataene USMF brukes til å opprette denne fremgangsmåten.


## <a name="create-an-accessorial-master"></a>Opprett en tilbehørsmal
1. Gå til Transportstyring > Oppsett > Vurdering > Tilbehørsmaler.
2. Klikk på Ny.
3. Angi en verdi i Tilbehørsmal-feltet.
4. Skriv inn en verdi i Navn-feltet.
5. Klikk på Lagre.

## <a name="create-a-carrier-accessorial-charge"></a>Opprett transportørens tilbehørsgebyr
1. Gå til Transportstyring > Oppsett > Vurdering > Transportørens tilbehørsgebyr.
2. Klikk på Ny.
3. Skriv inn en verdi i feltet ID for transportørtilbehør.
4. Klikk på rullegardinknappen i feltet Transportør for å åpne oppslaget.
5. Finn og velg ønsket post i listen.
    * I dette eksemplet velger du lastebiltransportør.  
6. Klikk på koblingen i den valgte raden i listen.
7. Klikk på rullegardinknappen i feltet Transportørtjeneste for å åpne oppslaget.
8. Klikk på koblingen i den valgte raden i listen.
9. Klikk på rullegardinknappen i feltet Tilbehørsmal for å åpne oppslaget.
10. Finn og velg ønsket post i listen.
    * Velg den nyopprettede tilbehørsmalen i dette eksemplet.  
11. Klikk på Lagre.

## <a name="create-an-accessorial-assignment"></a>Opprett en tilbehørstilordning
1. Klikk på Tilbehørstilordninger.
2. Klikk på Ny.
3. Skriv inn en verdi i Navn-feltet.
4. Aktiver/deaktiver utvidelsen av Kriterier-delen.
    * I kriteriene kan du velge å alltid bruke drivstofftillegg eller for dette eksemplet velge at det bare gjelder innenfor et bestemt område.  
5. Skriv inn en verdi i feltet Postnummer fra.
6. Skriv inn en verdi i feltet Postnummer til.
7. Aktiver/deaktiver utvidelsen av Beregning-delen.
    * Du kan angi hvordan du beregner drivstofftillegg i beregningsdelen. Denne beregningen avhenger av den tilbehørsenheten som du har valgt som grunnlag for beregningen.  
8. Velg Drivstofftillegg i feltet Tilbehørsgebyrtype.
9. Velg Kilometer i feltet Tilbehørsenhet.
10. Klikk på rullegardinknappen i Område-feltet for å åpne oppslaget.
11. Klikk på koblingen i den valgte raden i listen.
12. Klikk på Lagre.

## <a name="update-the-carrier-rating-profile"></a>Oppdater vurderingsprofilen for transportør
1. Gå til Transportstyring > Oppsett > Transportører > Transportører.
2. Finn og velg ønsket post i listen.
3. Aktiver/deaktiver utvidelsen av delen Vurderingsprofiler.
4. Klikk på Rediger
5. Klikk på rullegardinknappen i feltet Drivstoffindeks for transportør for å åpne oppslaget.
6. Klikk på koblingen i den valgte raden i listen.
7. Klikk på Lagre.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]