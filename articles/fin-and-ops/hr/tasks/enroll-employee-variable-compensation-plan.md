--- 
title: Registrere en ansatt i en fast kompensasjonsplan
description: "Kompensasjons- og fordelslederen kan registrere ansatte i variable kompensasjonsplaner for å beregne kontant- og ikke-kontantbonuser for ansatte."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 63a02a64ff28531bae950f1b61d9167eaa0b0373
ms.openlocfilehash: ebb92d5ce05f2891d25fb38f6200a10f02bcc948
ms.contentlocale: nb-no
ms.lasthandoff: 11/01/2017

---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a>Registrere en ansatt i en fast kompensasjonsplan

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kompensasjons- og fordelslederen kan registrere ansatte i variable kompensasjonsplaner for å beregne kontant- og ikke-kontantbonuser for ansatte. Denne fremgangsmåten forutsetter at en variabel kompensasjonsplan er opprettet med Aktiver registrering-feltet satt til Ja, og at det er opprettet rettighetsregler for den variable kompensasjonsplanen. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Hvis du vil starte fremgangsmåten, kan du gå til Personale > Arbeidere > Ansatte > Kompensasjon > Registrering av variabel plan

1. Klikk Ny.
2. Klikk rullegardinknappen i Plan-feltet for å åpne oppslaget.
    * Plan-oppslaget filtreres for bare å vise de variable kompensasjonsplanene som den ansatte er kvalifisert for basert på rettighetsreglene.  
3. Klikk koblingen i den valgte raden i listen.
4. Aktiver/deaktiver utvidelsen av delen Generelt.
5. Angi en dato i feltet Gyldighetsdato.
6. Klikk Lagre.
7. Aktiver/deaktiver utvidelsen av delen Overstyringer.
    * Du kan også angi en ansettelsesregeldato til å overstyre ansettelsesdatoen for en ansatt når ansettelsesregelen angitt for den valgte variable planen, er Prosent.  
    * Hvis den variable planen er en prosent av grunnplanen, kan belønningsprosenten overstyres for den ansatte. Hvis den variable kompensasjonsplanen er et nummer for enhetsplan, kan antall enheter overstyres for den ansatte.  
    * Hvis den ansatte skal gis et flatt beløp for sin bonus, kan beløpet angis her.  
8. Aktiver/deaktiver utvidelsen av delen Organisasjonsmessige overstyringer.
    * Hvis den ansattes ytelse bør ta i betraktning ytelsen til ulike avdelinger eller en annen avdeling enn den som er tilordnet på den ansattes stilling, kan avdelingen overstyres. Prosent-kolonnen skal være 100 totalt.  


