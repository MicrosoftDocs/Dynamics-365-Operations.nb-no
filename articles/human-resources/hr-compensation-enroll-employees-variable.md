---
title: Registrere en ansatt i en fast kompensasjonsplan
description: Kompensasjons- og fordelslederen kan registrere ansatte i variable kompensasjonsplaner for å beregne kontant- og ikke-kontantbonuser for ansatte.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67b3cd95276b9e59e794583fa51ddbcec4c43b1e
ms.sourcegitcommit: a8ac6d9b63eb67d14dd17a086ef4f1eccd7f9fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/27/2021
ms.locfileid: "7431320"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a>Registrere en ansatt i en fast kompensasjonsplan

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kompensasjons- og fordelslederen kan registrere ansatte i variable kompensasjonsplaner for å beregne kontant- og ikke-kontantbonuser for ansatte. Denne fremgangsmåten forutsetter at en variabel kompensasjonsplan er opprettet med **Aktiver registrering**-feltet satt til Ja, og at det er opprettet rettighetsregler for den variable kompensasjonsplanen. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Hvis du vil starte fremgangsmåten, kan du gå til **Personale** > **Arbeidere** > **Ansatte** > **Kompensasjon** > **Registrering av variabel plan**.

1. Klikk på **Ny**.
2. Klikk på rullegardinknappen i **Plan**-feltet for å åpne oppslaget.
    * Plan-oppslaget filtreres for bare å vise de variable kompensasjonsplanene som den ansatte er kvalifisert for basert på rettighetsreglene.  
3. Klikk koblingen i den valgte raden i listen.
4. Aktiver/deaktiver utvidelsen av delen Generelt.
5. Angi en dato i feltet **Gyldighetsdato**.
6. Klikk på **Lagre**.
7. Aktiver/deaktiver utvidelsen av delen **Overstyringer**.
    * Du kan også angi en ansettelsesregeldato til å overstyre ansettelsesdatoen for en ansatt når ansettelsesregelen angitt for den valgte variable planen, er Prosent.  
    * Hvis den variable planen er en prosent av grunnplanen, kan belønningsprosenten overstyres for den ansatte. Hvis den variable kompensasjonsplanen er et nummer for enhetsplan, kan antall enheter overstyres for den ansatte.  
    * Hvis den ansatte skal gis et flatt beløp for sin bonus, kan beløpet angis her.  
8. Aktiver/deaktiver utvidelsen av delen **Organisasjonsmessige overstyringer**.
    * Hvis den ansattes ytelse bør ta i betraktning ytelsen til ulike avdelinger eller en annen avdeling enn den som er tilordnet på den ansattes stilling, kan avdelingen overstyres. **Prosent**-kolonnen skal være 100 totalt.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
