--- 
title: Registrere en ansatt i en fast kompensasjonsplan
description: "Kompensasjons- og fordelsansvarlig kan knytte ansatte til faste kompensasjonsplaner for å administrere deres grunnlønn."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 0f4756b45e750fabf0f88b10db417819380603c1
ms.contentlocale: nb-no
ms.lasthandoff: 07/28/2017

---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>Registrere en ansatt i en fast kompensasjonsplan

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kompensasjons- og fordelsansvarlig kan knytte ansatte til faste kompensasjonsplaner for å administrere deres grunnlønn. Denne fremgangsmåten forutsetter at en fast plan er opprettet og er aktiv, og at det er angitt rettighetsregler for planen. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Hvis du vil starte fremgangsmåten, kan du gå til Personale > Arbeidere > Ansatte > Kompensasjon > Fast plan

1. Klikk Ny.
2. I Handling-feltet velger du en fast kompensasjonshandling av typen Ansette/ansette på nytt for å beskrive endringen i den ansattes kompensasjon.
3. Klikk koblingen i den valgte raden i listen.
4. Klikk rullegardinknappen i Stilling-feltet for å åpne oppslaget.
5. Klikk koblingen i den valgte raden i listen.
    * Nivået som vises er fra kompensasjonsnivået for jobben på stillingen. Nivået må angis for jobben før kompensasjon kan tilordnes til ansatt.  
6. I Plan-feltet velger du den faste kompensasjonsplanen for den ansatte. Plan-oppslaget er filtrert for bare å vise planene som den ansatte er kvalifisert for basert på rettighetsreglene.
7. Finn og velg ønsket post i listen.
    * De effektive datoene og utløpsdatoene for kompensasjon hentes fra start- og sluttdatoene for arbeiderens stillingstilordning. Du kan endre disse datoene etter behov.  
    * Hvis den faste kompensasjonsplanen er en trinnplan, velger du trinnet som inneholder den riktige lønnssatsen for den ansatte. Hvis den faste kompensasjonsplanen er en klasse- eller segmentplan, angir du lønnssatsen for den ansatte. Lønnssatsen blir validert mot toleranseinnstillinger for planen, og minimum og maksimum referansepunkt for jobbens kompensasjonsnivå.  
8. Klikk OK.


