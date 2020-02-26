---
title: Registrere en ansatt i en fast kompensasjonsplan
description: Kompensasjons- og fordelsansvarlig kan knytte ansatte til faste kompensasjonsplaner for å administrere deres grunnlønn.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 843db6bc133382a701d4b25b164794e57df152c7
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010146"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>Registrere en ansatt i en fast kompensasjonsplan

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

