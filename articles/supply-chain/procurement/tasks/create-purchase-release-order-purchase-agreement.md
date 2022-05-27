---
title: Bruk en kjøpsavtale ved oppretting av en bestilling
description: Denne fremgangsmåten viser hvordan du bruker en kjøpsavtale når du oppretter en bestilling.
author: GalynaFedorova
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a21821d75be2d5340cd418c12be39431870d2779
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678750"
---
# <a name="apply-a-purchase-agreement-when-creating-a-purchase-order"></a>Bruk en kjøpsavtale ved oppretting av en bestilling

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du bruker en kjøpsavtale når du oppretter en bestilling. Kjøpsavtalen må brukes når du oppretter bestillingen, fordi det finnes generelle vilkår som bør kopieres til bestillingshodet. Denne oppgaven vil vanligvis utføres av en innkjøpsagent. Som en forutsetning for denne veiledningen må du ha en gyldig kjøpsavtale med en produktantallsforpliktelse for en leverandør og varer. Den samme fremgangsmåten kan brukes hvis du har en kjøpsavtale med andre former for forpliktelser.

## <a name="create-a-purchase-order"></a>Opprette en bestilling

1. Gå til **Produksjon og leverandører \> Arbeidsområder \> Bestillingsklargjøring**.
1. Velg **Ny bestilling** i handlingsruten.
1. Dialogboksen **Opprett bestilling** åpnes. Velg en **leverandørkonto**. Undersøk og juster de andre adressefeltene etter behov.
1. Vis hurtigfanen **Generelt**.
1. I **Kjøpsavtale**-feltet finner og velger du den gjeldende avtalen du vil bruke. Alle tilgjengelige avtaler for leverandøren vises her.  
1. Velg **Ja**.
1. Velg **OK**.

## <a name="add-a-line"></a>Legg til en linje

1. Skriv inn en verdi i **Varenummer**-feltet. Hvis det finnes bestemte dimensjoner for lager eller lokasjon for forpliktelsen, må du angi de samme verdiene på bestillingslinjen for å ta i bruk avtalen.
1. Velg rullegardinknappen i **Område**-feltet for å åpne oppslaget. Området kan allerede være fylt ut med standardverdien fra bestillingen, eller fra leverandøren. Hvis dette er tilfelle, kan du hoppe over dette trinnet.  
1. Finn og velg ønsket post i listen.
1. Velg koblingen i den valgte raden i listen.
1. Angi et tall i **Antall**-feltet. Valider at prisen er kopiert fra forpliktelsen.  

## <a name="look-up-the-commitment"></a>Slå opp forpliktelsen

1. Velg **Oppdater linje**.
1. Velg **Vedlagt**. Her finner du detaljer for kjøpsavtalen. Du kan for eksempel se prisen og om prisen og rabatten er fast, noe som betyr at hvis du endrer prisen eller rabatten i bestillingen til en annen verdi enn i forpliktelsen, fjernes koblingen slik at bestillingslinjen ikke oppfyller forpliktelsen. Du kan også se om Maks. håndheves-alternativet er valgt, noe som betyr at antallet på forpliktelsen ikke kan overskrides ved å summere alle kjøpene som oppfyller forpliktelsen.  
1. Lukk siden.

## <a name="look-up-the-purchase-agreement"></a>Slå opp kjøpsavtalen

1. Klikk på **Generelt** i **handlingsruten**.
1. Velg **Kjøpsavtale**.
1. Lukk siden.
1. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]