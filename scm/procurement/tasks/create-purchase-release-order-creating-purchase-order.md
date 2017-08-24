--- 
title: "Opprette en frigivelsesordre for innkjøp ved oppretting av bestillingen"
description: "Denne fremgangsmåten viser hvordan du bruker en kjøpsavtale når du oppretter en bestilling."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 9f7407ca1d42eb24b5a6df90f659bc850ced414b
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a>Opprette en frigivelsesordre for innkjøp ved oppretting av bestillingen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du bruker en kjøpsavtale når du oppretter en bestilling. Kjøpsavtalen må brukes når du oppretter bestillingen, fordi det finnes generelle vilkår som bør kopieres til bestillingshodet. Denne oppgaven vil vanligvis utføres av en innkjøpsagent. Som en forutsetning for denne veiledningen må du ha en gyldig kjøpsavtale med en produktantallsforpliktelse for en leverandør og varer. Den samme fremgangsmåten kan brukes hvis du har en kjøpsavtale med andre former for forpliktelser. Du kan bruke denne veiledningen i USMF-demodatafirmaet. Hvis du bruker USMF, kan du kjøre veiledningen Opprette en kjøpsavtale først for å definere de nødvendig forutsetningene for denne veiledningen.


## <a name="create-a-purchase-order"></a>Opprette en bestilling
1. Åpne arbeidsområdet for bestillingsklargjøring.
2. Klikk Ny bestilling.
3. Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.
4. Finn og velg ønsket post i listen.
5. Klikk koblingen i den valgte raden i listen.
6. Aktiver/deaktiver utvidelsen av delen Generelt.
7. Klikk rullegardinknappen i feltet Kjøpsavtale for å åpne oppslaget.
    * Alle tilgjengelige avtaler for leverandøren vises her. Finn den gyldige avtalen du vil bruke.  
8. Klikk koblingen i den valgte raden i listen.
9. Klikk Ja.
10. Klikk OK.

## <a name="add-a-line"></a>Legge til en linje
1. Skriv inn en verdi i Varenummer-feltet.
    * Hvis det finnes bestemte dimensjoner for lager eller lokasjon for forpliktelsen, må du angi de samme verdiene på bestillingslinjen for å ta i bruk avtalen.  
2. Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.
    * Området kan allerede være fylt ut med standardverdien fra bestillingen, eller fra leverandøren. Hvis dette er tilfelle, kan du hoppe over dette trinnet.  
3. Finn og velg ønsket post i listen.
4. Klikk koblingen i den valgte raden i listen.
5. Angi et tall i feltet Antall.
    * Valider at prisen er kopiert fra forpliktelsen.  

## <a name="look-up-the-commitment"></a>Slå opp forpliktelsen
1. Klikk Oppdater linje.
2. Klikk Vedlagt.
    * Her finner du detaljer for kjøpsavtalen. Du kan for eksempel se prisen og om prisen og rabatten er fast, noe som betyr at hvis du endrer prisen eller rabatten i bestillingen til en annen verdi enn i forpliktelsen, fjernes koblingen slik at bestillingslinjen ikke oppfyller forpliktelsen. Du kan også se om Maks. håndheves-alternativet er valgt, noe som betyr at antallet på forpliktelsen ikke kan overskrides ved å summere alle kjøpene som oppfyller forpliktelsen.  
3. Lukk siden.

## <a name="look-up-the-purchase-agreement"></a>Slå opp kjøpsavtalen
1. Klikk Generelt i handlingsruten.
2. Klikk Kjøpsavtale.
3. Lukk siden.
4. Lukk siden.


