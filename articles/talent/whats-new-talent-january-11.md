---
title: Hva er nytt eller endret i Dynamics 365 Talent – Core HR (11. januar 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent – Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d49a4aca368e3de10ae37b56c6d286d78f7f369a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462133"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-11-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent – Core HR (11. januar 2019)

**Build 8.1.2100**

Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.

## <a name="changes"></a>Endringer

### <a name="validate-leave-requests-by-forecasting-available-balance"></a>Validere permisjonsforespørsler ved hjelp av prognoser for tilgjengelig saldo
Endringer i denne versjonen tillater ansatte å be om fremtidig permisjon uten å trekke fra den gjeldende saldoen. Standard arbeidsflyter brukes for eventuelle fremtidige forespørsler. Hvis du vil ha mer informasjon, les [Avsette fridager basert på arbeidstimer](leave-accrue-hours-worked.md).

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a>Vise anslått permisjonssaldo i ESS og Personer
Denne funksjonen aktiverer visning av saldoer for fremtidige permisjonsperioder for Personale, ledere og ansatte. Ansatte kan vise fremtidige saldoer i arbeidsområdet **Ansattbetjening**, og Personale har tilgang til den samme informasjon ved hjelp av **Personer**-arbeidsområdet.

### <a name="notifications-for-changing-leave-balances"></a>Varslinger for å endre lønnssaldoer
Lønnssaldoer viser den gjeldende saldoen for ansatte. Fremtidige saldoer er tilgjengelige i arbeidsområdene **Ansattselvbetjening** og **Personer** ved å angi en "per dato" for å beregne forventet saldo.

Navigasjon er lagt til for å vise prognoseberegnede saldoer på følgende områder:
  - **Fridager**-kort i arbeidsområet **Ansattselvbetjening**.
  - **Permisjon og fravær**-kort i arbeidsområdet **Lederselvbetjening** .
  - **Permisjon og fravær**-siden i **Personer**-arbeidsområdet.

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a>Tillat desimaler for variable kompensasjonsplaner (kontantplaner)
Variable kontantbelønninger og -planer har nå mer fleksibilitet for beløp og overstyringer for verdier med desimalbeløp.

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a>Kan ikke endre datoene i Variabel kompensasjonsregistrering når planen er lagret
Denne endringen fører til at sluttdatoen for planen kan oppdateres (utvidet eller utløpt) når planen er lagret. Du kan fortsatt aktivere eller deaktivere planer uavhengig av start- og sluttdatoer.

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a>Lønnsinformasjon tilgjengelig når tilordnet Lønnsadministrator-sikkerhetsrollen
Lønnsadministratorrollen er oppdatert for å få tilgang til lønnsinformasjonen under forespørselsprosessen.

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Ansattselvbetjening | Neddrilling i stillingshierarki fra flis kan ikke hente overordnet node
Endringer er gjort for å fjerne en feil som oppstod ved tillegging av stillingshierarkiet til nye arbeidsområder og navigering i organisasjonsstrukturen.

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a>Ny valideringsmelding når personellnummerserie er i bruk
En endring er gjort for å oppklare hva problemet er når du ansetter en ansatt og det neste personalnummeret er i bruk.

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a>Ansattselvbetjening-arbeidsområdet valgt som første oppstartsside
Når **Ansattselvbetjening**-arbeidsområdet er valgt som første oppstartsside for en bruker, og vedkommende ikke er tilordnet ansattrollen, vil systemet omdirigere til standard instrumentbord.

### <a name="termination-reason-code-updates-position-assignment-record"></a>Avslutningsårsakskode oppdaterer stillingstilordningspost
Avslutningsårsakskoden oppdaterer nå stillingstilordningen når en ansatt slutter og stillingen avsluttes. 
