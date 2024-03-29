---
title: Registrere en ansatt i en fast kompensasjonsplan
description: Kompensasjons- og fordelsansvarlig kan knytte ansatte til faste kompensasjonsplaner for å administrere deres grunnlønn.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d611f2631a59fbe1e131e82ca9937a5adaaf2ebd
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688748"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>Registrere en ansatt i en fast kompensasjonsplan


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kompensasjons- og fordelsansvarlig kan knytte ansatte til faste kompensasjonsplaner for å administrere deres grunnlønn. Denne fremgangsmåten forutsetter at en fast plan er opprettet og er aktiv, og at det er angitt rettighetsregler for planen. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Hvis du vil starte fremgangsmåten, kan du gå til **Personale** > **Arbeidere** > **Ansatte** > **Kompensasjon** > **Fast plan**.

1. Klikk på **Ny**.
2. I **Handling**-feltet velger du en fast kompensasjonshandling av typen **Ansette/ansette på nytt** for å beskrive endringen i den ansattes kompensasjon.
3. Klikk koblingen i den valgte raden i listen.
4. Klikk på rullegardinknappen i **Stilling**-feltet for å åpne oppslaget.
5. Klikk på koblingen i den valgte raden i listen.
    * Nivået som vises, er fra hurtigfanen **Kompensasjon** > **Nivå**-feltet fra **jobben** som er tilordnet til **stillingen**. Nivået må angis for jobben før kompensasjon kan tilordnes til ansatt.  
6. I **Plan**-feltet velger du den faste kompensasjonsplanen for den ansatte. **Plan**-oppslaget er filtrert for bare å vise planene som den ansatte er kvalifisert for basert på **rettighetsreglene**.
7. Finn og velg ønsket post i listen.
    * Datoene **Effektiv** og **Utløp** for kompensasjon hentes fra start- og sluttdatoene for arbeiderens stillingstilordning. Du kan endre disse datoene etter behov.  
    * Hvis den faste kompensasjonsplanen er en trinnplan, velger du trinnet som inneholder den riktige lønnssatsen for den ansatte. Hvis den faste kompensasjonsplanen er en klasse- eller segmentplan, angir du lønnssatsen for den ansatte. Lønnssatsen blir validert mot toleranseinnstillinger for planen, og minimum og maksimum referansepunkt for jobbens kompensasjonsnivå.  
8. Klikk på **OK**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
