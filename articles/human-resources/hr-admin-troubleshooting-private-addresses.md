---
title: Tilgang til private adresser etter sikkerhetsrolle
description: Denne artikkelen forklarer hvordan du løser problemet der en kunde ikke får tilgang til private adresser.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: facfd17f007b2c9e6f068d0ec4c5ce45b85a1b78
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010094"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="e48b6-103">Tilgang til private adresser etter sikkerhetsrolle</span><span class="sxs-lookup"><span data-stu-id="e48b6-103">Access to private addresses by security role</span></span>

<span data-ttu-id="e48b6-104">**Utstede**</span><span class="sxs-lookup"><span data-stu-id="e48b6-104">**Issue**</span></span>

<span data-ttu-id="e48b6-105">Når en kunde dupliserer en sikkerhetsrolle og logger på som den nye rollen, kan ikke kunden se adresser som er merket som private.</span><span class="sxs-lookup"><span data-stu-id="e48b6-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="e48b6-106">**Oppløsning**</span><span class="sxs-lookup"><span data-stu-id="e48b6-106">**Resolution**</span></span>

<span data-ttu-id="e48b6-107">For å løse problemet må kunden følge denne fremgangsmåten for den dupliserte sikkerhetsrollen.</span><span class="sxs-lookup"><span data-stu-id="e48b6-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="e48b6-108">Gå til **Organisasjonsstyring \> Global adressebok \> Parametere for global adressebok**.</span><span class="sxs-lookup"><span data-stu-id="e48b6-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="e48b6-109">På fanen **Sikkerhet for privat lokasjon** flytter du den nye sikkerhetsrollen fra listen **Tilgjengelige roller** til listen **Valgte roller**.</span><span class="sxs-lookup"><span data-stu-id="e48b6-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="e48b6-110">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e48b6-110">Select **Save**.</span></span>

![Siden for parametere for global adressebok](media/GAD-parameters.png)