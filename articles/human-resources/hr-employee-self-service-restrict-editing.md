---
title: Begrense redigering av personlige opplysninger
description: Du kan hindre at ansatte redigerer kontaktdetaljer i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e43b9127b247fa618558b725837d12bf290662f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052031"
---
# <a name="restrict-editing-of-personal-information"></a><span data-ttu-id="79661-103">Begrense redigering av personlige opplysninger</span><span class="sxs-lookup"><span data-stu-id="79661-103">Restrict editing of personal information</span></span>

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="79661-104">Dette emnet beskriver hvordan du begrenser ansatte fra å redigere kontaktdetaljer i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="79661-104">This topic describes how to restrict employees from editing contact details in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="79661-105">Det kan hende at du vil hindre at ansatte redigerer bestemte kontaktdetaljer, for eksempel forretningslokasjonen eller e-postadressen.</span><span class="sxs-lookup"><span data-stu-id="79661-105">You might want to prevent employees from editing certain contact details, such as their business location or email address.</span></span>

> [!NOTE]
> <span data-ttu-id="79661-106">Hvis du vil bruke denne funksjonen, må du først aktivere **(Forhåndsvis) Hindre ansatte i å legge til eller redigere adresse- og kontaktinformasjon for utvalgte formål** i Funksjonsstyring.</span><span class="sxs-lookup"><span data-stu-id="79661-106">To use this feature, you must first enable **(Preview) Restrict employees from adding or editing address and contact information for select purposes** in Feature management.</span></span> <span data-ttu-id="79661-107">Hvis du vil ha mer informasjon om hvordan du aktiverer forhåndsvisningsfunksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="79661-107">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="79661-108">![Aktiver forhåndsvisningsfunksjon](./media/hr-employee-self-service-restrict-enable.png)</span><span class="sxs-lookup"><span data-stu-id="79661-108">![Enable preview feature](./media/hr-employee-self-service-restrict-enable.png)</span></span>

## <a name="choose-the-information-an-employee-can-add-or-edit"></a><span data-ttu-id="79661-109">Velge informasjonen som en ansatt kan legge til eller redigere</span><span class="sxs-lookup"><span data-stu-id="79661-109">Choose the information an employee can add or edit</span></span>

1. <span data-ttu-id="79661-110">I Human Resources velger du **Personaladministrasjon**, **Koblinger** og deretter **Personalparametere**.</span><span class="sxs-lookup"><span data-stu-id="79661-110">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

   ![Gå til Human Resources-parametere](./media/hr-employee-self-service-human-resources-parameters.png)

2. <span data-ttu-id="79661-112">Velg fanen **Selvbetjening for ansatte** på siden **Parametere for Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="79661-112">On the **Human resources parameters** page, select the **Employee self service** tab.</span></span>

   ![Velg Selvbetjening for ansatte](./media/hr-employee-self-service-tab.png)

3. <span data-ttu-id="79661-114">I fanen **Selvbetjening for ansatte** fjerner du merket for all informasjon i delen **Adresse- og kontaktinformasjon** som du ikke vil at ansatte skal legge til eller redigere.</span><span class="sxs-lookup"><span data-stu-id="79661-114">On the **Employee self service** tab, uncheck all information in the **Address and contact information** section that you don't want employees to add or edit.</span></span> <span data-ttu-id="79661-115">I dette eksemplet er det ikke merket av for kontaktinformasjonen for **Virksomhet**.</span><span class="sxs-lookup"><span data-stu-id="79661-115">In this example, we've unchecked **Business** contact information.</span></span>

   ![Begrense redigering av forretningskontaktinformasjon](./media/hr-employee-self-service-restrict-business.png)

4. <span data-ttu-id="79661-117">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="79661-117">Select **Save**.</span></span>

   ![Lagre endringer](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a><span data-ttu-id="79661-119">Ansatterfaring</span><span class="sxs-lookup"><span data-stu-id="79661-119">Employee experience</span></span>

<span data-ttu-id="79661-120">Når du har begrenset ansatte fra å legge til eller redigere kontaktdetaljer, kan de se informasjonen, men kan ikke endre den.</span><span class="sxs-lookup"><span data-stu-id="79661-120">After you've restricted employees from adding or editing contact details, they can see the information, but can't change it.</span></span>

<span data-ttu-id="79661-121">I dette eksemplet hvor ansatte er begrenset fra å redigere kontaktdetaljer for **Virksomhet**, kan de likevel se informasjonen i Selvbetjening for ansatte:</span><span class="sxs-lookup"><span data-stu-id="79661-121">In this example, where employees are restricted from editing **Business** contact details, they can still see the information in Employee self service:</span></span>

![Vise detaljer for forretningskontakter](./media/hr-employee-self-service-restrict-view.png)

<span data-ttu-id="79661-123">Når de velger forretningskontaktdetaljene, vises imidlertid ruten **Rediger adresse** som skrivebeskyttet, og de kan ikke endre noen av feltene.</span><span class="sxs-lookup"><span data-stu-id="79661-123">However, when they select the business contact details, the **Edit address** pane appears as read-only, and they can't change any of the fields.</span></span>

![Forretningskontaktdetaljer vises som skrivebeskyttet](./media/hr-employee-self-service-restrict-read-only.png)

<span data-ttu-id="79661-125">Hvis de i tillegg velger **Legg til** for å legge til en ny adresse, kan de ikke velge **Virksomhet** fra rullegardinlisten **Formål**.</span><span class="sxs-lookup"><span data-stu-id="79661-125">In addition, if they select **Add** to add a new address, they can't select **Business** from the **Purpose** dropdown box.</span></span>

![Den ansatte kan ikke legge til en forretningsadresse](./media/hr-employee-self-service-restrict-add.png)

<span data-ttu-id="79661-127">Ansatte får samme erfaring når de velger **Kontaktdetaljer** på siden **Personalinformasjon** og legger til en ny adresse.</span><span class="sxs-lookup"><span data-stu-id="79661-127">Employees get the same experience when they select **Contact details** on the **Personal information** page and add a new address.</span></span> <span data-ttu-id="79661-128">Rullegardinlisten **Formål** viser bare informasjonstypene de kan legge til.</span><span class="sxs-lookup"><span data-stu-id="79661-128">The **Purpose** dropdown box only displays the types of information they can add.</span></span> 

![Den ansatte kan ikke velge rullegardinlisten Virksomhet i Formål](./media/hr-employee-self-service-restrict-purpose.png)

<span data-ttu-id="79661-130">**Kontaktdetaljer** viser nå **Formål** i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="79661-130">**Contact details** now shows **Purpose** in the grid.</span></span>

![Formål vises i Rutenett for kontaktdetaljer](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a><span data-ttu-id="79661-132">Se også</span><span class="sxs-lookup"><span data-stu-id="79661-132">See also</span></span>

[<span data-ttu-id="79661-133">Oversikt over selvbetjening for ansatte og ledere</span><span class="sxs-lookup"><span data-stu-id="79661-133">Employee and Manager self service overview</span></span>](hr-employee-manager-self-service-overview.md)<br>
[<span data-ttu-id="79661-134">Konfigurere parametere for Human Resources</span><span class="sxs-lookup"><span data-stu-id="79661-134">Configure Human resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="79661-135">Rediger personlige opplysninger</span><span class="sxs-lookup"><span data-stu-id="79661-135">Edit personal information</span></span>](hr-employee-manager-self-service-edit-personal-information.md)