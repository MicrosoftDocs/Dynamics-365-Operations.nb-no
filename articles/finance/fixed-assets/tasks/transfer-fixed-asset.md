---
title: Overføre et anleggsmiddel
description: Denne oppgaveveiledningen overfører den økonomiske informasjonen for et anleggsmiddeltablå fra én finansdimensjon som er satt til et nytt sett med finansdimensjoner.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0770011a76b1e4cc8b4d13e54fab2d0fba43f8a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975922"
---
# <a name="transfer-a-fixed-asset"></a>Overføre et anleggsmiddel

[!include [banner](../../includes/banner.md)]

Denne oppgaveveiledningen overfører den økonomiske informasjonen for et anleggsmiddeltablå fra én finansdimensjon som er satt til et nytt sett med finansdimensjoner.  Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.

1. I navigasjonsruten går du til **Moduler > Anleggsmidler > Anleggsmidler > Anleggsmidler**.
2. I listen finner og merker du anleggsmidlet som skal overføres.
3. Klikk på **Anleggsmiddel** i handlingsruten.
4. Klikk på **Overfør anleggsmidler**.
5. Angi en dato i feltet **Overføringsdato**.
6. Angi kommentarer for å beskrive overføringen.
    
    Denne listen viser alle tablåene for anleggsmidlet.  
7. Merk tablåene du vil overføre til et nytt sett med finansdimensjoner.
    * Denne listen viser de eksisterende finansdimensjonsverdiene for det valgte tablået.  
    * Velg finansdimensjonen du vil oppdatere for det valgte anleggsmiddeltablået.  
8. Klikk rullegardinknappen i feltet **Finansdimensjon** for å åpne oppslaget.
    * Angi andre verdier for finansdimensjonen etter behov.  
    * Alle finansdimensjonsverdier endres når det oppstår en overføring, enten en verdi er angitt eller står tom. Hvis du for eksempel har angitt en verdi for BusinessUnit og latt finansdimensjonene CostCenter og Avdeling stå tom. Hvis kontostrukturen tillater tomme verdier for CostCenter og Avdeling, fører overføringen til at hver verdimodell får den nye verdien for BusinessUnit og en tom verdi for CostCenter og Avdeling.  
9. Klikk på **Oppdater**.
    * Du har muligheten til å forhåndsvise endringene før du fullfører overføringen.  
    * Se gjennom resultatene før du overfører anleggsmiddeltablåene.  
10. Klikk på **Overfør**.

