---
title: Klassifiser anleggsmidler på nytt
description: Denne artikkelen forklarer prosessen med å omklassifisere anleggsmidler. Hvis du vil omklassifisere et anleggsmiddel, må du overføre det til den nye anleggsmiddelgruppen, eller gi det et nytt anleggsmiddelnummer i samme gruppe.
author: moaamer
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89c046b131afd1728b26465816eee98ee1898e49
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861394"
---
# <a name="reclassify-fixed-assets"></a>Klassifiser anleggsmidler på nytt

[!include [banner](../../includes/banner.md)]

Hvis du vil omklassifisere et anleggsmiddel, må du overføre det til den nye anleggsmiddelgruppen, eller gi det et nytt anleggsmiddelnummer i samme gruppe. 

Når et anleggsmiddel er omklassifisert:

- Alle tablåer for det eksisterende anleggsmiddelet opprettes for det nye anleggsmiddelet. All informasjon som ble definert for det originale anleggsmiddelet, kopieres til det nye anleggsmiddelet. Statusen til tablåene til det originale anleggsmiddelet er Lukket. 

- De nye tablåene for det nye anleggsmiddelet inneholder omklassifiseringsdatoen i **Anskaffelsesdato**-feltet. Datoen i feltet **Startdato for avskrivning** kopieres fra den opprinnelige anleggsmiddelinformasjonen. Hvis avskrivningen allerede har begynt, viser feltet **Datoen da avskrivningen sist ble kjørt** omklassifiseringsdatoen. 

- De eksisterende anleggsmiddeltransaksjonene for det originale anleggsmiddelet avlyses og genereres på nytt for det nye anleggsmiddelet.

- Når et anleggsmiddel som har en overføringstransaksjon er omklassifisert, viser systemet en melding i **handlingssenteret** for å angi at en overføringstransaksjon ikke ble fullført under omklassifiseringsprosessen. Det er nødvendig å fullføre en overføringstransaksjon for å flytte de eksisterende omklassifiseringstransaksjonene til de riktige finansdimensjonene. 

   Under omklassifiseringsprosessen kjører systemet følgende handlinger for å omklassifisere anleggsmiddelsaldoen fra det opprinnelige anleggsmiddelet til det nye anleggsmiddelet. 
   
   - Omklassifiseringsprosessen kopierer dataene fra det opprinnelige anleggsmiddeltablået til det nye anleggsmiddeltablået.

   - Omklassifiseringstransaksjonen bruker informasjon fra den opprinnelige posterte anskaffelsen, som omfatter finansdimensjonsinformasjon som er inkludert i anskaffelsestransaksjonen.  
   
   - Samtidig tilbakefører omklassifiseringsprosessen den opprinnelige anleggsmiddelanskaffelsen og anleggsmiddeloverføringstransaksjonen. 

Diagrammet og fremgangsmåten nedenfor gir et eksempel på omklassifiseringsprosessen. 

[![Diagram som viser omklassifiseringsprosessen.](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)

Følg disse trinnene for å omklassifisere et anleggsmiddel:

1. Gå til **Anleggsmidler > Periodiske oppgaver > Omklassifisering**.
2. I feltet **Anleggsmiddelgruppe** velger du gruppen som skal omklassifiseres.
3. I feltet **Anleggsmiddelnummer** velger du anleggsmidlet som skal omklassifiseres.
4. Velg en gruppe som anleggsmidlet skal overføres til, i feltet **Ny anleggsmiddelgruppe**.
    * Hvis den nye anleggsmiddelgruppen er knyttet til en nummerserie, oppdateres feltet **Nytt anleggsmiddelnummer** med nummeret fra nummerserien til den nye anleggsmiddelgruppen. Ellers oppdateres feltet **Nytt anleggsmiddelnummer** med nummeret fra nummerserien som er definert på siden **Parametere for anleggsmidler**. Hvis en nummerserie ikke er definert på siden **Parametere for anleggsmidler**, angir du et nummer i feltet **Nytt anleggsmiddelnummer**.  
5. Angi en dato i feltet **Omklassifiseringsdato**.
6. Angi eller velg en verdi i feltet **Bilagsserie**.
7. Velg **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
