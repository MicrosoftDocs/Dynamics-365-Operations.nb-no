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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bd82bef29e5d1d33c1dc1aa3a039833741c1fdaf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793639"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="694c8-103">Sende en permisjonsforespørsel til arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="694c8-103">Submit a leave request to workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="694c8-104">I Microsoft Dynamics 365 Human Resources kan du bruke API-et (Application Programming Interface) MyLeaveRequests submit() til å sende en permisjonsforespørsel til arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="694c8-104">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="694c8-105">Dette API-et vises som en handling på MyLeaveRequests OData-enheten.</span><span class="sxs-lookup"><span data-stu-id="694c8-105">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="694c8-106">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="694c8-106">Prerequisites</span></span>

<span data-ttu-id="694c8-107">Permisjonsforespørselen må være lagret i databasen og må kunne hentes via MyLeaveRequests-enheten.</span><span class="sxs-lookup"><span data-stu-id="694c8-107">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="694c8-108">Tillatelser</span><span class="sxs-lookup"><span data-stu-id="694c8-108">Permissions</span></span>

<span data-ttu-id="694c8-109">En av følgende tillatelser kreves for å kalle dette API-et.</span><span class="sxs-lookup"><span data-stu-id="694c8-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="694c8-110">Hvis du vil ha mer informasjon om tillatelser og hvordan du velger dem, kan du se [Godkjenning](hr-developer-api-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="694c8-110">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="694c8-111">Tillatelsestype</span><span class="sxs-lookup"><span data-stu-id="694c8-111">Permission type</span></span>                    | <span data-ttu-id="694c8-112">Tillatelser (fra minst privilegert til mest privilegert)</span><span class="sxs-lookup"><span data-stu-id="694c8-112">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="694c8-113">Delegert (jobb- eller skolekonto)</span><span class="sxs-lookup"><span data-stu-id="694c8-113">Delegated (work or school account)</span></span> | <span data-ttu-id="694c8-114">user\_impersonation</span><span class="sxs-lookup"><span data-stu-id="694c8-114">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="694c8-115">HTTPS-forespørsel</span><span class="sxs-lookup"><span data-stu-id="694c8-115">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="694c8-116">Forespørselen overholder OData-standarder.</span><span class="sxs-lookup"><span data-stu-id="694c8-116">The request conforms to OData standards.</span></span> <span data-ttu-id="694c8-117">Parameterne {requestId}, {leaveType}, {leaveDate} og {dataArea} refererer til feltene som utgjør den sammensatte naturlige nøkkelen for MyLeaveRequests-enheten.</span><span class="sxs-lookup"><span data-stu-id="694c8-117">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="694c8-118">Mens feltene for MyLeaveRequests-enheten refererer til en enkelt linje i permisjonsforespørselen, vil kall til Send-API-et hele sende permisjonsforespørselen (alle linjene) til arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="694c8-118">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="694c8-119">Forespørselshoder</span><span class="sxs-lookup"><span data-stu-id="694c8-119">Request headers</span></span>

| <span data-ttu-id="694c8-120">Hode</span><span class="sxs-lookup"><span data-stu-id="694c8-120">Header</span></span>         | <span data-ttu-id="694c8-121">Value</span><span class="sxs-lookup"><span data-stu-id="694c8-121">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="694c8-122">Autorisasjon</span><span class="sxs-lookup"><span data-stu-id="694c8-122">Authorization</span></span>  | <span data-ttu-id="694c8-123">Bærer {token} (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="694c8-123">Bearer {token} (required)</span></span> |
| <span data-ttu-id="694c8-124">Innholdstype</span><span class="sxs-lookup"><span data-stu-id="694c8-124">Content-Type</span></span>   | <span data-ttu-id="694c8-125">program/json</span><span class="sxs-lookup"><span data-stu-id="694c8-125">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="694c8-126">Forespørselstekst</span><span class="sxs-lookup"><span data-stu-id="694c8-126">Request body</span></span>

<span data-ttu-id="694c8-127">Ikke angi en forespørselstekst for denne metoden.</span><span class="sxs-lookup"><span data-stu-id="694c8-127">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="694c8-128">Svar</span><span class="sxs-lookup"><span data-stu-id="694c8-128">Response</span></span>

<span data-ttu-id="694c8-129">Et vellykket svar er alltid av typen **204 uten innhold**.</span><span class="sxs-lookup"><span data-stu-id="694c8-129">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="694c8-130">Uautoriserte kallere får et svar av typen **401 uautorisert** eller **403 forbudt**.</span><span class="sxs-lookup"><span data-stu-id="694c8-130">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="694c8-131">Hvis innsendingen mislykkes (for eksempel på grunn av validering), vil svaret bli **500 serverfeil**, og svarteksten inneholder et JSON-objekt med mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="694c8-131">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="694c8-132">Eksempel</span><span class="sxs-lookup"><span data-stu-id="694c8-132">Example</span></span>

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

## <a name="validation-and-error-messages"></a><span data-ttu-id="694c8-133">Validering og feilmeldinger</span><span class="sxs-lookup"><span data-stu-id="694c8-133">Validation and error messages</span></span>

<span data-ttu-id="694c8-134">Som en del av kallet til innsendings-API-et utfører Human Resources en validering av forretningslogikken før innsending, som sikrer at permisjonsforespørselen er i en gyldig tilstand for innsending.</span><span class="sxs-lookup"><span data-stu-id="694c8-134">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="694c8-135">De mulige feilmeldingene du kan motta i svaret hvis valideringer mislykkes, er:</span><span class="sxs-lookup"><span data-stu-id="694c8-135">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="694c8-136">Forespørselen ville lagt {LeaveTypeId}-saldoen under den tillatte minimumssaldoen i {date}.</span><span class="sxs-lookup"><span data-stu-id="694c8-136">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="694c8-137">Fritidsforespørsel i fullført tilstand kan ikke sendes inn.</span><span class="sxs-lookup"><span data-stu-id="694c8-137">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="694c8-138">Kan ikke sende inn eller lagre forespørselen fordi ingen endringer er utført.</span><span class="sxs-lookup"><span data-stu-id="694c8-138">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="694c8-139">Legg til eller oppdater beløpet eller permisjonstypen, og prøv på nytt.</span><span class="sxs-lookup"><span data-stu-id="694c8-139">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="694c8-140">Fritidsforespørselen inneholder én eller flere dager med samme dato og permisjonstype som en eksisterende ventende forespørsel.</span><span class="sxs-lookup"><span data-stu-id="694c8-140">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="694c8-141">Tilbakekall den eksisterende forespørselen for å utføre endringer.</span><span class="sxs-lookup"><span data-stu-id="694c8-141">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="694c8-142">Årsakskoden {ReasonCodeId} gjelder ikke for noen av permisjonstypene i forespørselen.</span><span class="sxs-lookup"><span data-stu-id="694c8-142">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="694c8-143">Permisjonstypen {LeaveTypeId} krever en årsakskode.</span><span class="sxs-lookup"><span data-stu-id="694c8-143">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="694c8-144">Velg riktig type og årsakskode.</span><span class="sxs-lookup"><span data-stu-id="694c8-144">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="694c8-145">Fritidsforespørselen ble ikke sendt.</span><span class="sxs-lookup"><span data-stu-id="694c8-145">The time off was not submitted successfully.</span></span> <span data-ttu-id="694c8-146">Fritidsforespørselen er lagret som et utkast.</span><span class="sxs-lookup"><span data-stu-id="694c8-146">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="694c8-147">Se også</span><span class="sxs-lookup"><span data-stu-id="694c8-147">See also</span></span>

- [<span data-ttu-id="694c8-148">Oversikt over MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="694c8-148">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="694c8-149">Godkjenning</span><span class="sxs-lookup"><span data-stu-id="694c8-149">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]