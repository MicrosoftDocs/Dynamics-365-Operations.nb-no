--- 
title: " Opprette tillatelsesgrupper for salgssted"
description: Denne prosedyren viser hvordan du oppretter en salgsstedstillatelsesgruppe.
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: b0c930e3722d1d0b1fff8efad7a785a153436b6d
ms.contentlocale: nb-no
ms.lasthandoff: 07/28/2017

---
# <a name="create-pos-permission-groups"></a> Opprette tillatelsesgrupper for salgssted

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne prosedyren viser hvordan du oppretter en salgsstedstillatelsesgruppe. Demonstrasjonsdatafirmaet USRT brukes til å opprette denne oppgaven. Denne oppgaven er ment for rollen Driftsleder for detaljhandel.

1. Gå til Tillatelsesgrupper.
2. Klikk Ny.
3. Skriv inn en verdi i feltet ID for salgsstedstillatelsesgruppe.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Velg Ja i feltet Vis tidsklokkeoppføringer.
    * Nå kan du aktivere eller deaktivere ulike tillatelser for salgsstedstillatelsesgruppen. For enkelte tillatelser kan du angi en verdi som skal brukes til å vurdere om salgsstedsbrukeren kan utføre handlingen.  Denne oppgaveveiledningen angir noen tillatelser som kan gis til en kasserer.  
6. Velg Ja i feltet Tillat oppretting av ordre.
7. Velg Ja i feltet Tillat redigering av ordre.
8. Velg Ja i feltet Tillat oppretting av ordre.
9. Velg Ja i feltet Tillat passordendring.
10. Velg Ja i feltet Tillat usporet lukking.
11. Klikk Lagre.
    * Når endringene er lagret, må du kjøre stabsdistribusjonsplanen for å overføre endringene til detaljhandelskanalene.  
12. Lukk siden.
13. Gå til Jobber.
    * Vi vil nå tilordne salgsstedstillatelsesgruppen til en jobb.  
14. Finn og velg ønsket post i listen.
15. Klikk koblingen i den valgte raden i listen.
16. Klikk Rediger
17. Vis delen Jobbklassifisering.
18. Angi eller velg en verdi i feltet Gruppe for salgsstedstillatelse.
    * Alle arbeidere i stillinger for denne jobben bruker salgsstedstillatelsesgruppens innstillinger med mindre arbeidernes salgsstedstillatelser har blitt overstyrt på stillingsnivået.  
19. Klikk Lagre.
    * Når endringene er lagret, må du kjøre stabsdistribusjonsplanen for å overføre endringene til detaljhandelskanalene.  


