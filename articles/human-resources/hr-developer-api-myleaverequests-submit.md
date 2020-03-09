---
title: Sende en permisjonsforespørsel til arbeidsflyt
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 008ee231ca9f0459e332b17cea9f2a3f3e3cc2a5
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010118"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="29fbd-102">Sende en permisjonsforespørsel til arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="29fbd-102">Submit a leave request to workflow</span></span>

<span data-ttu-id="29fbd-103">I Microsoft Dynamics 365 Human Resources kan du bruke API-et (Application Programming Interface) MyLeaveRequests submit() til å sende en permisjonsforespørsel til arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="29fbd-103">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="29fbd-104">Dette API-et vises som en handling på MyLeaveRequests OData-enheten.</span><span class="sxs-lookup"><span data-stu-id="29fbd-104">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="29fbd-105">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="29fbd-105">Prerequisites</span></span>

<span data-ttu-id="29fbd-106">Permisjonsforespørselen må være lagret i databasen og må kunne hentes via MyLeaveRequests-enheten.</span><span class="sxs-lookup"><span data-stu-id="29fbd-106">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="29fbd-107">Tillatelser</span><span class="sxs-lookup"><span data-stu-id="29fbd-107">Permissions</span></span>

<span data-ttu-id="29fbd-108">En av følgende tillatelser kreves for å kalle dette API-et.</span><span class="sxs-lookup"><span data-stu-id="29fbd-108">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="29fbd-109">Hvis du vil ha mer informasjon om tillatelser og hvordan du velger dem, kan du se [Godkjenning](hr-developer-api-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="29fbd-109">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="29fbd-110">Tillatelsestype</span><span class="sxs-lookup"><span data-stu-id="29fbd-110">Permission type</span></span>                    | <span data-ttu-id="29fbd-111">Tillatelser (fra minst privilegert til mest privilegert)</span><span class="sxs-lookup"><span data-stu-id="29fbd-111">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="29fbd-112">Delegert (jobb- eller skolekonto)</span><span class="sxs-lookup"><span data-stu-id="29fbd-112">Delegated (work or school account)</span></span> | <span data-ttu-id="29fbd-113">user\_impersonation</span><span class="sxs-lookup"><span data-stu-id="29fbd-113">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="29fbd-114">HTTPS-forespørsel</span><span class="sxs-lookup"><span data-stu-id="29fbd-114">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="29fbd-115">Forespørselen overholder OData-standarder.</span><span class="sxs-lookup"><span data-stu-id="29fbd-115">The request conforms to OData standards.</span></span> <span data-ttu-id="29fbd-116">Parameterne {requestId}, {leaveType}, {leaveDate} og {dataArea} refererer til feltene som utgjør den sammensatte naturlige nøkkelen for MyLeaveRequests-enheten.</span><span class="sxs-lookup"><span data-stu-id="29fbd-116">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="29fbd-117">Mens feltene for MyLeaveRequests-enheten refererer til en enkelt linje i permisjonsforespørselen, vil kall til Send-API-et hele sende permisjonsforespørselen (alle linjene) til arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="29fbd-117">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="29fbd-118">Forespørselshoder</span><span class="sxs-lookup"><span data-stu-id="29fbd-118">Request headers</span></span>

| <span data-ttu-id="29fbd-119">Hode</span><span class="sxs-lookup"><span data-stu-id="29fbd-119">Header</span></span>         | <span data-ttu-id="29fbd-120">Value</span><span class="sxs-lookup"><span data-stu-id="29fbd-120">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="29fbd-121">Autorisasjon</span><span class="sxs-lookup"><span data-stu-id="29fbd-121">Authorization</span></span>  | <span data-ttu-id="29fbd-122">Bærer {token} (obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="29fbd-122">Bearer {token} (required)</span></span> |
| <span data-ttu-id="29fbd-123">Innholdstype</span><span class="sxs-lookup"><span data-stu-id="29fbd-123">Content-Type</span></span>   | <span data-ttu-id="29fbd-124">program/json</span><span class="sxs-lookup"><span data-stu-id="29fbd-124">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="29fbd-125">Forespørselstekst</span><span class="sxs-lookup"><span data-stu-id="29fbd-125">Request body</span></span>

<span data-ttu-id="29fbd-126">Ikke angi en forespørselstekst for denne metoden.</span><span class="sxs-lookup"><span data-stu-id="29fbd-126">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="29fbd-127">Svar</span><span class="sxs-lookup"><span data-stu-id="29fbd-127">Response</span></span>

<span data-ttu-id="29fbd-128">Et vellykket svar er alltid av typen **204 uten innhold**.</span><span class="sxs-lookup"><span data-stu-id="29fbd-128">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="29fbd-129">Uautoriserte kallere får et svar av typen **401 uautorisert** eller **403 forbudt**.</span><span class="sxs-lookup"><span data-stu-id="29fbd-129">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="29fbd-130">Hvis innsendingen mislykkes (for eksempel på grunn av validering), vil svaret bli **500 serverfeil**, og svarteksten inneholder et JSON-objekt med mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="29fbd-130">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="29fbd-131">Eksempel</span><span class="sxs-lookup"><span data-stu-id="29fbd-131">Example</span></span>

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

## <a name="validation-and-error-messages"></a><span data-ttu-id="29fbd-132">Validering og feilmeldinger</span><span class="sxs-lookup"><span data-stu-id="29fbd-132">Validation and error messages</span></span>

<span data-ttu-id="29fbd-133">Som en del av kallet til innsendings-API-et utfører Human Resources en validering av forretningslogikken før innsending, som sikrer at permisjonsforespørselen er i en gyldig tilstand for innsending.</span><span class="sxs-lookup"><span data-stu-id="29fbd-133">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="29fbd-134">De mulige feilmeldingene du kan motta i svaret hvis valideringer mislykkes, er:</span><span class="sxs-lookup"><span data-stu-id="29fbd-134">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="29fbd-135">Forespørselen ville lagt {LeaveTypeId}-saldoen under den tillatte minimumssaldoen i {date}.</span><span class="sxs-lookup"><span data-stu-id="29fbd-135">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="29fbd-136">Fritidsforespørsel i fullført tilstand kan ikke sendes inn.</span><span class="sxs-lookup"><span data-stu-id="29fbd-136">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="29fbd-137">Kan ikke sende inn eller lagre forespørselen fordi ingen endringer er utført.</span><span class="sxs-lookup"><span data-stu-id="29fbd-137">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="29fbd-138">Legg til eller oppdater beløpet eller permisjonstypen, og prøv på nytt.</span><span class="sxs-lookup"><span data-stu-id="29fbd-138">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="29fbd-139">Fritidsforespørselen inneholder én eller flere dager med samme dato og permisjonstype som en eksisterende ventende forespørsel.</span><span class="sxs-lookup"><span data-stu-id="29fbd-139">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="29fbd-140">Tilbakekall den eksisterende forespørselen for å utføre endringer.</span><span class="sxs-lookup"><span data-stu-id="29fbd-140">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="29fbd-141">Årsakskoden {ReasonCodeId} gjelder ikke for noen av permisjonstypene i forespørselen.</span><span class="sxs-lookup"><span data-stu-id="29fbd-141">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="29fbd-142">Permisjonstypen {LeaveTypeId} krever en årsakskode.</span><span class="sxs-lookup"><span data-stu-id="29fbd-142">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="29fbd-143">Velg riktig type og årsakskode.</span><span class="sxs-lookup"><span data-stu-id="29fbd-143">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="29fbd-144">Fritidsforespørselen ble ikke sendt.</span><span class="sxs-lookup"><span data-stu-id="29fbd-144">The time off was not submitted successfully.</span></span> <span data-ttu-id="29fbd-145">Fritidsforespørselen er lagret som et utkast.</span><span class="sxs-lookup"><span data-stu-id="29fbd-145">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="29fbd-146">Se også</span><span class="sxs-lookup"><span data-stu-id="29fbd-146">See also</span></span>

- [<span data-ttu-id="29fbd-147">Oversikt over MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="29fbd-147">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="29fbd-148">Godkjenning</span><span class="sxs-lookup"><span data-stu-id="29fbd-148">Authentication</span></span>](hr-developer-api-authentication.md)