---
title: Avsett permisjons- og fraværsplaner
description: Du kan avsette permisjon og fravær i Dynamics 365 Human Resources for flere ansatte eller for en enkeltperson.
author: andreabichsel
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ddd4c55f6ebfbe91fb949a92cb379f51d826c465
ms.sourcegitcommit: cee7887282d372c756c5c11f76684315f249bba5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/24/2021
ms.locfileid: "6303470"
---
# <a name="accrue-leave-and-absence-plans"></a>Avsett permisjons- og fraværsplaner

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan avsette permisjon og fravær i Dynamics 365 Human Resources for flere ansatte eller for en enkeltperson.

## <a name="accrue-leave-and-absence-for-multiple-employees"></a>Avsette permisjon og fravær for flere ansatte

1. På siden **Permisjon og fravær** velger du **Koblinger**-fanen.

2. Under **Administrer permisjon** velger du **Avsett permisjons- og fraværsplaner**.

3. Dialogboksen **Avsett permisjons- og fraværsplaner** vises. I **Avsett per** velger du **Dagens dato**, eller du velger **Egendefinert dato** og angir en egendefinert dato.

4. Hvis du vil kjøre avsetninger for alle firmaer, velger du **Alle selskaper**. Hvis du vil behandle avsetninger for en enkelt permisjonsplan, velger du **Nei** for **Alle planer**, og deretter velger du en **Permisjonsplan**. Hvis du velger alle firmaer, kan du ikke velge en individuell permisjonsplan.

5. Hvis du vil kjøre avsetningsprosessen i bakgrunnen, velger du **Kjør i bakgrunnen** og utfører følgende oppgaver:

    1. Angi informasjon for avsetningsprosessen.
    2. Hvis du vil definere en gjentakende jobb, velger du **Gjentakelse**, angir gjentakelsesinformasjonen og velger deretter **OK**.
    3. Når du skal definere et jobbvarsel, velger du **Varsler**, velger varslene du vil motta, og velger deretter **OK**.
    4. Velg **OK**. Avsetningsprosessen vil kjøre med parameterne du angir. 

## <a name="accrue-leave-and-absence-for-an-employee"></a>Avsette permisjon og fravær for en ansatt

1. Velg **Permisjon** i posten for den ansatte.

2. Velg **Avsett permisjon og fravær**.

3. Dialogboksen **Avsett permisjons- og fraværsplaner** vises. I **Avsett per** velger du **Dagens dato**, eller du velger **Egendefinert dato** og angir en egendefinert dato.

4. Hvis du vil kjøre avsetninger for alle firmaer, velger du **Alle selskaper**. Hvis du vil behandle avsetninger for en enkelt permisjonsplan, velger du **Nei** for **Alle planer**, og deretter velger du en **Permisjonsplan**. Hvis du velger alle firmaer, kan du ikke velge en individuell permisjonsplan.

5. Hvis du vil kjøre avsetningsprosessen i bakgrunnen, velger du **Kjør i bakgrunnen** og utfører følgende oppgaver:

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

## <a name="leave-accrual-transaction-auditing"></a>Overvåking av permisjonsavsetningstransaksjon

Ved hjelp av denne funksjonen kan permisjons- og fraværsledere forstå avsetningstransaksjonene for permisjon og fravær som er knyttet til en ansatts fraværssaldoer for en bestemt permisjonstype.

Slik viser du transaksjonsdetaljer:

1. Velg **Permisjon** i posten for den ansatte.

2. Velg **Vis fravær**, og velg deretter kategorien **Saldoer**.

Hvis du vil vise avsetningstransaksjonene som er knyttet til en bestemt permisjonstype, velger du den numeriske verdien i kolonnen **Gjeldende saldo**.

Hvis du vil vise transaksjonsdetaljene for et bestemt avsetningsbeløp, velger du en avsetningsrad, åpner **Beslektet informasjon**-panelet til høyre og åpner deretter **Transaksjonsdetaljer**-delen. Delen Transaksjonsdetaljer viser:

- Endringer i saldoen for permisjonstype for en ansatt
- Ansattdetaljer for den angitte avsetningsperioden
- Detaljer om avsetningsperioden og -satsene
- Eventuelle endringer som er gjort for permisjonsplankonfigurasjoner

![Vise overvåking av permisjonsavsetningstransaksjon](media/hr-leave-and-absence-accrue-audit.png)

## <a name="see-also"></a>Se også

[Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md)</br>
[Opprette en permisjons- og fraværsplan](hr-leave-and-absence-plans.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
