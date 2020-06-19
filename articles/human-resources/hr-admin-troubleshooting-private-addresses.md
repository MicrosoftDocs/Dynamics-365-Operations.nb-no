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
ms.openlocfilehash: fbe0e8acc1b879e4d7982b33413236432f25f630
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431044"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="3e251-103">Tilgang til private adresser etter sikkerhetsrolle</span><span class="sxs-lookup"><span data-stu-id="3e251-103">Access to private addresses by security role</span></span>

<span data-ttu-id="3e251-104">**Utstede**</span><span class="sxs-lookup"><span data-stu-id="3e251-104">**Issue**</span></span>

<span data-ttu-id="3e251-105">Når en kunde dupliserer en sikkerhetsrolle og logger på som den nye rollen, kan ikke kunden se adresser som er merket som private.</span><span class="sxs-lookup"><span data-stu-id="3e251-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="3e251-106">**Oppløsning**</span><span class="sxs-lookup"><span data-stu-id="3e251-106">**Resolution**</span></span>

<span data-ttu-id="3e251-107">For å løse problemet må kunden følge denne fremgangsmåten for den dupliserte sikkerhetsrollen.</span><span class="sxs-lookup"><span data-stu-id="3e251-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="3e251-108">Gå til **Organisasjonsstyring \> Global adressebok \> Parametere for global adressebok**.</span><span class="sxs-lookup"><span data-stu-id="3e251-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="3e251-109">På fanen **Sikkerhet for privat lokasjon** flytter du den nye sikkerhetsrollen fra listen **Tilgjengelige roller** til listen **Valgte roller**.</span><span class="sxs-lookup"><span data-stu-id="3e251-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="3e251-110">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3e251-110">Select **Save**.</span></span>

![Siden for parametere for global adressebok](media/GAD-parameters.png)
