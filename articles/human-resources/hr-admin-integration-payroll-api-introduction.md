---
title: Innføring i API for lønnsintegrering
description: Dette emnet beskriver API-en for lønnsintegrering i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4c71d31d7045c73097b81671793181a29dcac3b5
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8064947"
---
# <a name="payroll-integration-api-introduction"></a>Innføring i API for lønnsintegrering


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette dokumentet beskriver API-en for lønnsintegrering i Dynamics 365 Human Resources. API-en gjør det mulig å strømlinjeforme ende-til-ende-integrasjoner mellom Human Resources og partnerlønnssystemer. Den integrerte opplevelsen begynner i Human Resources med ansattprofilen, lønn og fradrag og bidragsinformasjon. Når du ansetter en ansatt og angir den nødvendige profilen og lønnsinformasjon i Human Resources, henter lønnssystemet denne informasjonen som skal brukes ved behandling av lønn. Eventuelle oppdateringer som gjøres til den ansatte eller lønnsinformasjonen, trekkes også for bruk i senere lønnsutbetalinger.

[![Flyten i lønnsintegrering.](media/hr-admin-integration-payroll-api-introduction-flow.png)](media/hr-admin-integration-payroll-api-introduction-flow-2.png#lightbox)

Human Resources inkluderer følgende komponenter for å aktivere integreringen:

- [Funksjonalitet for å merke en ansatt som klar til å betale.](hr-compensation-payroll.md)
- En integrerings-API som åpner opp den nye funksjonaliteten for integrering av programmer.

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Denne API-en er bygd på Microsoft Dataverse (tidligere kalt Common Data Service). All RESTful-samhandling med denne API-en gjøres via web-API-en for Microsoft Dataverse, som bruker OData. Denne API-en er et delsett av Dataverse-web-API-en. Dataverse-web-API-en definerer egenskaper som godkjenning, SLA-er, parti, samtidighetskontroll og feilhåndtering.

Hvis du vil ha mer generell informasjon om Microsoft Dataverse-web-API-en, kan du se:

- [Hva er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)
- [Bruke Microsoft Dataverse-web-API-en](/powerapps/developer/data-platform/webapi/overview)
- [Utviklerveiledning for Microsoft Dataverse](/powerapps/developer/data-platform)

Denne dokumentasjonen inneholder detaljer og utviklerveiledning for bruk av Dataverse Web-API, inkludert følgende emner:

- [Godkjenn til Microsoft Dataverse med nett-API](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [Utfør operasjoner ved hjelp av nett-API](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [Bruk Postman med nett-API](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [Bruk endringssporing til å synkronisere data med eksterne systemer](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Virtuelle tabeller for Human Resources i Dataverse

Sluttpunktene for API-en for lønnsintegrering bruker de virtuelle tabellplattformfunksjonene i Microsoft Dataverse. Som standard distribueres ikke de virtuelle tabellene og de tilknyttede API-sluttpunktene for Human Resources-miljøene, som gjør det mulig for organisasjoner å fastslå hvilke OData-sluttpunkter som vises for miljøet. For å kunne bruke API-en må de virtuelle tabellene for Human Resources-enhetene genereres for miljøet.

Hvis du vil ha informasjon om generering av de virtuelle tabellene for API, kan du se [Konfigurere virtuelle Dataverse-tabeller](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>Datamodell

Diagrammet nedenfor illustrerer relasjonen med API-en. Flere typer har sekundærnøkler til andre, eksisterende enheter i Human Resources som ikke illustreres her. Dette dokumentet inneholder informasjon om enheter som er spesifikke for lønnsintegrasjonsscenarier. Det er imidlertid mange andre enheter i Dataverse Web-API for Human Resources som også kan være relevante for integreringen. Enkelte av disse enhetene refereres til i sekundærnøkkelrelasjoner eller navigasjonsegenskaper.

[![Lønnsintegrering, API-datamodell.](media/hr-admin-payroll-api-data-model.png)](media/hr-admin-payroll-api-data-model.png#lightbox)

## <a name="payroll-employee-and-related-entities"></a>Lønnsansatt og relaterte enheter

Enheter:

- [Lønnsansatt](hr-admin-integration-payroll-api-payroll-employee.md)
- [Adresse til lønnsarbeider](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [Fast kompensasjonsplan for lønn](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md)
- [Variabel kompensasjonsplan for lønn](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md)
- [Lønnsstillingsjobb](hr-admin-integration-payroll-api-payroll-position-job.md)
- [Lønnsstilling](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a>Se også

[Generer og gå gjennom lønnsenheter](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[Konfigurere parametere for Human Resources](hr-setup-parameters.md)<br>
[Konfigurere delte parametere for Human Resources](hr-setup-shared-parameters.md)<br>
[Hva er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Bruke Microsoft Dataverse-web-API-en](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
