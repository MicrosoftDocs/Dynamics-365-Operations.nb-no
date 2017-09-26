--- 
title: "Overføre et anleggsmiddel"
description: "Denne oppgaveveiledningen overfører den økonomiske informasjonen for et anleggsmiddeltablå fra én finansdimensjon som er satt til et nytt sett med finansdimensjoner."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ebde1e8bd8a87b44dd77b9050d05d6c2f4774ef2
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="transfer-a-fixed-asset"></a>Overføre et anleggsmiddel

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaveveiledningen overfører den økonomiske informasjonen for et anleggsmiddeltablå fra én finansdimensjon som er satt til et nytt sett med finansdimensjoner.  Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.

1. Gå til Anleggsmidler > Anleggsmidler > Anleggsmidler.
2. I listen finner og merker du anleggsmidlet som skal overføres.
3. Klikk Anleggsmiddel i handlingsruten.
4. Klikk Overfør anleggsmidler.
5. Angi en dato i feltet Overføringsdato.
6. Angi kommentarer for å beskrive overføringen.
    * Denne listen viser alle tablåene for anleggsmidlet.  
7. Merk tablåene du vil overføre til et nytt sett med finansdimensjoner.
    * Denne listen viser de eksisterende finansdimensjonsverdiene for det valgte tablået.  
    * Velg finansdimensjonen du vil oppdatere for det valgte anleggsmiddeltablået.  
8. Klikk rullegardinknappen i feltet Finansdimensjon for å åpne oppslaget.
    * Angi andre verdier for finansdimensjonen etter behov.  
    * Alle finansdimensjonsverdier endres når det oppstår en overføring, enten en verdi er angitt eller står tom. Hvis du for eksempel har angitt en verdi for BusinessUnit og latt finansdimensjonene CostCenter og Avdeling stå tom. Hvis kontostrukturen tillater tomme verdier for CostCenter og Avdeling, fører overføringen til at hver verdimodell får den nye verdien for BusinessUnit og en tom verdi for CostCenter og Avdeling.  
9. Klikk Oppdater.
    * Du har muligheten til å forhåndsvise endringene før du fullfører overføringen.  
    * Se gjennom resultatene før du overfører anleggsmiddeltablåene.  
10. Klikk Overfør.


