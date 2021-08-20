---
title: Sende en permisjonsforespørsel til arbeidsflyt
description: I Microsoft Dynamics 365 Human Resources kan du bruke API-et (Application Programming Interface) MyLeaveRequests submit() til å sende en permisjonsforespørsel til arbeidsflyten.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d9a4c472868002c6cae061507bfe2f75d7f3eb86935d69acaac8cb7f2d970bfd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732063"
---
# <a name="submit-a-leave-request-to-workflow"></a>Sende en permisjonsforespørsel til arbeidsflyt

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I Microsoft Dynamics 365 Human Resources kan du bruke API-et (Application Programming Interface) MyLeaveRequests submit() til å sende en permisjonsforespørsel til arbeidsflyten. Dette API-et vises som en handling på MyLeaveRequests OData-enheten.

## <a name="prerequisites"></a>Forutsetninger

Permisjonsforespørselen må være lagret i databasen og må kunne hentes via MyLeaveRequests-enheten.

## <a name="permissions"></a>Tillatelser

En av følgende tillatelser kreves for å kalle dette API-et. Hvis du vil ha mer informasjon om tillatelser og hvordan du velger dem, kan du se [Godkjenning](hr-developer-api-authentication.md).

| Tillatelsestype                    | Tillatelser (fra minst privilegert til mest privilegert) |
|------------------------------------|--------------------------------------------------------|
| Delegert (jobb- eller skolekonto) | user\_impersonation                                    |

## <a name="https-request"></a>HTTPS-forespørsel

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

Forespørselen overholder OData-standarder. Parameterne {requestId}, {leaveType}, {leaveDate} og {dataArea} refererer til feltene som utgjør den sammensatte naturlige nøkkelen for MyLeaveRequests-enheten.

> [!NOTE]
> Mens feltene for MyLeaveRequests-enheten refererer til en enkelt linje i permisjonsforespørselen, vil kall til Send-API-et hele sende permisjonsforespørselen (alle linjene) til arbeidsflyten.

### <a name="request-headers"></a>Forespørselshoder

| Hode         | Value                     |
|----------------|---------------------------|
| Autorisasjon  | Bærer {token} (obligatorisk) |
| Innholdstype   | program/json          |

### <a name="request-body"></a>Forespørselstekst

Ikke angi en forespørselstekst for denne metoden.

### <a name="response"></a>Svar

Et vellykket svar er alltid av typen **204 uten innhold**.

Uautoriserte kallere får et svar av typen **401 uautorisert** eller **403 forbudt**.

Hvis innsendingen mislykkes (for eksempel på grunn av validering), vil svaret bli **500 serverfeil**, og svarteksten inneholder et JSON-objekt med mer informasjon.

## <a name="example"></a>Eksempel

```http
POST https://aos-rts-sf-550e5c091f6-prod-westus2.hr.talent.dynamics.com/namespaces/b2eb8003-334f-4a84-ab63-edbe23569090/data/MyLeaveRequests(RequestId='USMF-000065', LeaveType='Vacation', LeaveDate=2019-10-04T12:00:00Z, dataAreaId='USMF')/Microsoft.Dynamics.DataEntities.submit
```

```json
{
  "error": {
    "code": "",
    "message": "An error has occurred.",
    "innererror": {
      "message": "Exception occurred while executing action submit on Entity MyLeaveRequest: The request would put the 'Vacation' balance below the allowed minimum balance on 9/10/2019.",
      "type": "System.InvalidOperationException",
      "stacktrace": "   at Microsoft.Dynamics.Platform.Integration.Services.OData.Action.ActionInvokable.Invoke()   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateProcessor.ActionInvocation(ChangeOperationContext context, ActionInvokable action)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.<>c__DisplayClass13_0.<ScheduleInvokable>b__0(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActionsInCompanyContext(IEnumerable`1 actionList, ChangeOperationContext operationContext)\r\n   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActions(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.SaveChanges()   at Microsoft.Dynamics.Platform.Integration.Services.OData.AxODataDelegatingHandler.<SaveChangesAsync>d__3.MoveNext()"
    }
  }
}
```

## <a name="validation-and-error-messages"></a>Validering og feilmeldinger

Som en del av kallet til innsendings-API-et utfører Human Resources en validering av forretningslogikken før innsending, som sikrer at permisjonsforespørselen er i en gyldig tilstand for innsending. De mulige feilmeldingene du kan motta i svaret hvis valideringer mislykkes, er:

 - Forespørselen ville lagt {LeaveTypeId}-saldoen under den tillatte minimumssaldoen i {date}.
 - Fritidsforespørsel i fullført tilstand kan ikke sendes inn.
 - Kan ikke sende inn eller lagre forespørselen fordi ingen endringer er utført. Legg til eller oppdater beløpet eller permisjonstypen, og prøv på nytt.
 - Fritidsforespørselen inneholder én eller flere dager med samme dato og permisjonstype som en eksisterende ventende forespørsel. Tilbakekall den eksisterende forespørselen for å utføre endringer.
 - Årsakskoden {ReasonCodeId} gjelder ikke for noen av permisjonstypene i forespørselen.
 - Permisjonstypen {LeaveTypeId} krever en årsakskode. Velg riktig type og årsakskode.
 - Fritidsforespørselen ble ikke sendt. Fritidsforespørselen er lagret som et utkast.

## <a name="see-also"></a>Se også

- [Oversikt over MyLeaveRequests](hr-developer-api-myleaverequests-overview.md)
- [Godkjenning](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]