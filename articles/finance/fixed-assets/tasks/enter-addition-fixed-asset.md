---
title: Legge inn et tillegg til et anleggsmiddel
description: Denne fremgangsmåten viser hvordan du legger til et tillegg i et eksisterende anleggsmiddel.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: baac842660b6231529349ec97bcdbcdb971a0ac0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975972"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a>Legge inn et tillegg til et anleggsmiddel

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du legger til et tillegg i et eksisterende anleggsmiddel. Formålet med Anleggsmiddeltillegg brukes til å spore varetillegg, vedlikehold eller forbedringer for aktiva, og er kun til informasjon. Eventuelle endringer i verdien eller levetiden til anleggsmidlet må gjøres hver for seg.   

Fremgangsmåten bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.

1. I navigasjonsruten går du til **Moduler > Anleggsmidler > Anleggsmidler > Anleggsmidler**.
2. I listen finner og merker du anleggsmidlet for tillegget.
3. Klikk koblingen i den valgte raden i listen.
4. Klikk på **Anleggsmiddel** i handlingsruten.
5. Klikk på **Anleggsmiddeltillegg**.
6. Klikk på **Ny**.
7. Skriv inn en verdi i **Navn**-feltet.
8. Angi datoen for tilleggsinnkjøpet eller -servicen i feltet **Anskaffelsesdato**.
9. Angi kostnad for vare, vedlikehold eller andre forbedringer for aktivumet i feltet **Enhetskostnad**.
10. Angi et tall i **Antall**-feltet. Den totale kostnaden har ingen innvirkning på verdien til anleggsmidlet og er bare til sporings- og informasjonsformål. Hvis kostnaden skal kapitaliseres, må en oppskrivingsjusteringstransaksjon posteres separat.  
11. Klikk kategorien **Generelt**.

    * Angi **Øker levetiden** til **Ja** hvis tillegget øker levetiden for anleggsmidlet.  
    * Dette feltet er kun veiledende. Hvis du vil øke levetiden, kan du endre levetiden for verdimodeller og/eller avskrivningstablåene for aktivaet.  

