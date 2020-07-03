---
title: Avsett permisjons- og fraværsplaner
description: Du kan avsette permisjon og fravær i Dynamics 365 Human Resources for flere ansatte eller for en enkeltperson.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f045cb7ab9f5e7aa4259f29e1b026f110425c236
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429065"
---
# <a name="accrue-leave-and-absence-plans"></a>Avsett permisjons- og fraværsplaner

Du kan avsette permisjon og fravær i Dynamics 365 Human Resources for flere ansatte eller for en enkeltperson.

## <a name="accrue-leave-and-absence-for-multiple-employees"></a>Avsette permisjon og fravær for flere ansatte

1. På siden **Permisjon og fravær** velger du **Koblinger**-fanen.

2. Under **Administrer permisjon** velger du **Avsett permisjons- og fraværsplaner**.

3. Dialogboksen **Avsett permisjons- og fraværsplaner** vises. I **Avsett per** velger du **Dagens dato**, eller du velger **Egendefinert dato** og angir en egendefinert dato.

4. Hvis du vil kjøre avsetningsprosessen i bakgrunnen, velger du **Kjør i bakgrunnen** og utfører følgende oppgaver:

   1. Angi informasjon for avsetningsprosessen.

   2. Hvis du vil definere en gjentakende jobb, velger du **Gjentakelse**, angir gjentakelsesinformasjonen og velger **OK**.

   3. Når du skal definere et jobbvarsel, velger du **Varsler**, velger varslene du vil motta, og velger deretter **OK**.

   4. Velg **OK**. Avsetningsprosessen vil kjøre med parameterne du angir.

## <a name="accrue-leave-and-absence-for-an-employee"></a>Avsette permisjon og fravær for en ansatt

1. Velg **Permisjon** i posten for den ansatte.

2. Velg **Avsett permisjon og fravær**.

3. Dialogboksen **Avsett permisjons- og fraværsplaner** vises. I **Avsett per** velger du **Dagens dato**, eller du velger **Egendefinert dato** og angir en egendefinert dato.

4. Hvis du vil kjøre avsetningsprosessen i bakgrunnen, velger du **Kjør i bakgrunnen** og utfører følgende oppgaver:

   1. Angi informasjon for avsetningsprosessen.

   2. Hvis du vil definere en gjentakende jobb, velger du **Gjentakelse**, angir gjentakelsesinformasjonen og velger **OK**.

   3. Når du skal definere et jobbvarsel, velger du **Varsler**, velger varslene du vil motta, og velger deretter **OK**.

   4. Velg **OK**. Avsetningsprosessen vil kjøre med parameterne du angir.

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a>Slette permisjons- og fraværsavsetninger for flere ansatte

Slett avsetningsposter for en spesifikk plan og et bestemt datoområde. Avsetningsdatoer må være datert i dag eller i fremtiden.

1. På siden **Permisjon og fravær** velger du **Koblinger**-fanen.

2. Under **Administrer permisjon** velger du **Slett permisjons- og fraværsplanavsetninger**.

3. I dialogboksen **Slett permisjons- og fraværsavsetninger** velger du **Permisjonsplan**. 

4. Hvis det er aktuelt , velger du **Slett saldojusteringer**.

5. Angi eller velg en **Permisjonsavsetningsdato**. Denne datoen må være enten i dag eller i fremtiden. 

6. Velg **OK**. Avsetningsprosessen sletter avsetninger med parameterne du angir. 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a>Slette permisjons- og fraværsavsetninger for én ansatt

1. Velg **Permisjon** i posten for den ansatte.

2. Velg **Slett permisjons- og fraværsplanavsetninger**.

3. I dialogboksen **Slett permisjons- og fraværsavsetninger** velger du **Permisjonsplan**. 

4. Hvis det er aktuelt , velger du **Slett saldojusteringer**.

5. Angi eller velg en **Permisjonsavsetningsdato**. Denne datoen må være enten i dag eller i fremtiden. 

6. Velg **OK**. Avsetningsprosessen sletter avsetninger med parameterne du angir. 

## <a name="review-leave-accrual-and-deletion-processes"></a>Gå gjennom prosesser for permisjonsavsetning og -sletting

**Permisjonsavsetningsrevisjon** vises hver gang du kjører eller sletter en avsetning for én ansatt eller alle ansatte. Datoen og personen som utførte handlingen, vises også.

1. På siden **Permisjon og fravær** velger du **Koblinger**-fanen.

2. Under **Administrer permisjon** velger du **Slett permisjonsavsetningsrevisjon**.

## <a name="configure-preview-features"></a>Konfigurere forhåndsversjonsfunksjoner

[!include [banner](includes/preview-feature-leave-absence.md)]

Hvis du har aktivert forhåndsversjonsfunksjoner for permisjon og fravær, må du konfigurere innstillinger for dem også.

### <a name="accrue-leave-per-company-or-per-leave-plan"></a>Avsett permisjon per firma eller per permisjonsplan

Når du avsetter permisjons- og fraværsplaner, kan du velge å avsette for alle firmaer. Hvis du velger alle firmaer, kan du ikke velge individuelle permisjonsplaner. Hvis du velger ikke å avsette for alle firmaer, kan du avsette for en bestemt permisjonsplan. 

Disse alternativene er tilgjengelige når du avsetter for alle ansatte eller enkeltansatte. 

## <a name="see-also"></a>Se også

[Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md)</br>
[Opprette en permisjons- og fraværsplan](hr-leave-and-absence-plans.md)
