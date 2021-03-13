---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (25. juni 2020)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 23. juni 2020.
author: andreabichsel
manager: tfehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ad80e53c0a24d602ac446d3e0765f397dd0fc2d9
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127503"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (23. juni 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.3347. Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a>Når en registrering er utløpt for en avsluttet ansatt, fjernes permisjonstypen, saldoen og beløpet i Permisjonsregistreringsskjemaet (444867)

Verdier i **Permisjonstype**, **Saldo** og **Beløp** beholdes nå i stedet for å fjernes når du gjør dette valget.

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a>Feil anslått saldo ved ny funksjon (permisjonsavsetning for ett enkelt firma eller én enkelt plan) er aktivert (456553)

Riktig anslått saldo vises nå når permisjonsavsetning for ett enkelt firma eller én enkelt plan er aktivert.

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a>Enheter med relasjoner som resulterer i dupliserte navigasjonsegenskaper (456486)

Denne versjonen retter opp et problem med navigeringsegenskapene (relasjon) for flere enheter. Dupliserte relasjoner er oppdaget. Disse scenariene er rettet opp.
 
## <a name="cross-company-comments-on-performance-review-455536"></a>Kommentarer på tvers av firmaer på Medarbeidersamtale (455536)

Kommentarer på tvers av firmaer er nå synlig på medarbeidersamtaler med denne reparasjonen. Denne endringen korrigerer visningen av anmelderkommentarer som ble angitt i forskjellige firmaer for samme medarbeidersamtale.
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a>Inkonsekvens i visning av kompensasjonsstyringsdata (432562)

Det vedlikeholdes nå en konsekvent visning av kompensasjonsdata i Selvbetjening for ledere. Avhengig av hvordan du navigerer til en arbeiders **Kompensasjonsdetaljer**, viser kompensasjonsdata nå konsekvent for ledere.
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a>Kompensasjonsplanens gjeldende dato er dagens dato som standard (411994)

Startdatoen for kompensasjon er nå basert på startdatoen for stillingen som blir tilordnet den ansatte.

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a>Permisjon- og fraværsskjema Aktiver halvdagsdefinisjon deaktiveres når skjemaet åpnes (452607)

Med denne endringen blir **Aktiver halvdagsdefinisjon** aktivert til det finnes nye permisjonstransaksjoner. 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a>Kan ikke publisere til HcmDiscussionEntity via Excel. Feil i TotalRatingScore-felt (453899)

Du kan nå oppdatere **TotalRatingScore**-feltet ved hjelp av **HCMDiscussionEntity** i Excels arbeidsbokutforming.

## <a name="in-preview"></a>I forhåndsvisning

## <a name="database-logging"></a>Databaselogging

Med databaseloggføring kan du bestemme hvilke tabeller og felt som skal overvåkes. Du kan også fastslå hvilke hendelser som skal utløse endringssporing. Du kan bruke funksjonen for databaselogging for å se endringene over tid. Hvis du vil ha mer informasjon, se [Konfigurere og administrere databaselogging](hr-admin-database-logging.md).

## <a name="mandatory-fields"></a>Obligatorisk felt 

Du kan nå endre feltene ved hjelp av tilpasningsfunksjonene i Human Resources. Denne funksjonen krever **Lagrede visninger**.

## <a name="human-resources-application-in-teams"></a>Human Resources-søknad i Teams

Ansatte kan se og be om fravær fra jobb i Microsoft Teams. De kan kommunisere med en robot for å opprette permisjonsforespørsler. For mer informasjon, se [Human Resources-app i Teams](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Data Management Framework (DMF)-enheter for Fordelsbehandling
 
Enheter for fordelsstyring frigis. DMF-enheter gjør det mulig å importere og eksportere data slik at du enkelt kan konfigurere fordelsbehandling. En mal for fordelsbehandling vil være tilgjengelig for å flytte data. Malen eksporterer og importerer data på en sekvensiell måte for å respektere dataavhengigheter.

## <a name="buy-and-sell-leave"></a>Kjøp og selg permisjon 

Noen organisasjoner tilbyr en fordel som gjør det mulig for ansatte å kjøpe eller selge permisjon. Denne prosessen behandles ofte manuelt. Denne funksjonen automatiserer behandling av policyer og forespørsler for personalavdelingen. Den strømlinjeformer permisjonsstyringsprosessen og bidrar til å eliminere feil. Hvis du vil ha mer informasjon, kan du se:

- [Administrere policyer for kjøp og salg av permisjon](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Kjøp og selg permisjon](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Permisjonsavsetning for ett enkelt firma eller én enkelt plan

Kunder kan behandle avsetninger for ett enkelt firma eller en enkel permisjons- og fraværsplan. Denne muligheten gir klarhet til avsetningsprosessen for kunder med forskjellige policyer for fraværsår eller permisjonsavsetning. Hvis du vil ha mer informasjon, se [Avsett permisjon per firma eller per permisjonsplan](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Legge til vedlegg i fraværsforespørsler

Muligheten til å legge til vedlegg i godkjente permisjonsforespørsler er viktig i det gjeldende COVID-19-miljøet. Ansatte kan nå legge til disse vedleggene. De har også mer innsikt i hvordan det gjøres oppdateringer for permisjonsforespørsler. Hvis du vil ha mer informasjon, kan du se [Legge til et vedlegg i en eksisterende forespørsel](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Legge til årsakskode for avsetningsuspensjoner 

Årsakskoder er lagt til i avsetningssuspensjonen.

## <a name="carry-forward-rules"></a>Overføringsregler 

Du kan angi en type overføringspermisjon for overføringssaldoer der overføringsjusteringer overføres. Hvis en ansatt for eksempel overfører 10 dager, kan du velge en annen permisjonstype for disse 10 dagene. Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Avbryte permisjonsavsetning for angitte permisjonstyper

Du kan opprette en regel for å utsette permisjonsavsetninger for ansatte med permisjonsforespørsler som er angitt for fravær som ikke betales. Fravær som ikke betales, kan være en type, men behøver ikke å være det. Du kan stoppe enhver permisjon basert på en annen permisjonstype.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-enhet tilgjengelig for avsetningssuspensjoner 

En DMF-enhet er nå tilgjengelig for avsetningssuspensjoner.

## <a name="coming-soon"></a>Kommer snart

## <a name="configure-the-name-of-employee-self-service"></a>Konfigurere navnet på ansattselvbetjening

Et nytt alternativ vil være tilgjengelig i **Personale-parametere** for å oppdatere navnet på arbeidsområdet Ansattselvbetjening til Selvbetjening.

## <a name="checklist-entities-included-in-dataverse"></a>Sjekklisteenheter inkludert i Dataverse

Sjekklisteenheter for pålasting, avlasting, overføringer og forretningsprosesser vil snart være tilgjengelige i Dataverse.

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)