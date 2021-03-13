---
title: Tilgang til private adresser etter sikkerhetsrolle
description: Denne artikkelen forklarer hvordan du løser problemet der en kunde ikke får tilgang til private adresser.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 6598094e7877a30c35e1b03794f82c8a4ec001a7
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113677"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="1fb82-103">Tilgang til private adresser etter sikkerhetsrolle</span><span class="sxs-lookup"><span data-stu-id="1fb82-103">Access to private addresses by security role</span></span>

<span data-ttu-id="1fb82-104">**Utstede**</span><span class="sxs-lookup"><span data-stu-id="1fb82-104">**Issue**</span></span>

<span data-ttu-id="1fb82-105">Når en kunde dupliserer en sikkerhetsrolle og logger på som den nye rollen, kan ikke kunden se adresser som er merket som private.</span><span class="sxs-lookup"><span data-stu-id="1fb82-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="1fb82-106">**Oppløsning**</span><span class="sxs-lookup"><span data-stu-id="1fb82-106">**Resolution**</span></span>

<span data-ttu-id="1fb82-107">For å løse problemet må kunden følge denne fremgangsmåten for den dupliserte sikkerhetsrollen.</span><span class="sxs-lookup"><span data-stu-id="1fb82-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="1fb82-108">Gå til **Organisasjonsstyring \> Global adressebok \> Parametere for global adressebok**.</span><span class="sxs-lookup"><span data-stu-id="1fb82-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="1fb82-109">På fanen **Sikkerhet for privat lokasjon** flytter du den nye sikkerhetsrollen fra listen **Tilgjengelige roller** til listen **Valgte roller**.</span><span class="sxs-lookup"><span data-stu-id="1fb82-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="1fb82-110">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="1fb82-110">Select **Save**.</span></span>

![Siden for parametere for global adressebok](media/GAD-parameters.png)
