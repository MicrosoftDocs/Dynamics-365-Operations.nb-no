---
title: Plan for den globale adresseboken og andre adressebøker
description: Dette emnet beskriver vurderingene og beslutningene som du må ta i planleggingsprosessen før du definerer og konfigurerer den globale adresseboken og eventuelle tilleggsadressebøker.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89c6e71e5f537f0f9309eca1025c8e74cdce6716
ms.sourcegitcommit: 75bbcff474cfb8d2f282be2b9d2d7984d1505fa3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2883417"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a><span data-ttu-id="0f46e-103">Planlegge den globale adresseboken og andre adressebøker</span><span class="sxs-lookup"><span data-stu-id="0f46e-103">Plan for the global address book and other address books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f46e-104">Dette emnet beskriver vurderingene og beslutningene som du må ta i planleggingsprosessen før du definerer og konfigurerer den globale adresseboken og eventuelle tilleggsadressebøker.</span><span class="sxs-lookup"><span data-stu-id="0f46e-104">This topic describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books.</span></span> <span data-ttu-id="0f46e-105">Noen av avgjørelsene krever at du bekrefter beslutningene som er gjort for andre deler av produktet, for eksempel organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="0f46e-105">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

## <a name="global-address-book"></a><span data-ttu-id="0f46e-106">Global adressebok</span><span class="sxs-lookup"><span data-stu-id="0f46e-106">Global address book</span></span>

<span data-ttu-id="0f46e-107">Før du begynner å arbeide med den globale adresseboken, må du bestemme standardverdiene for den.</span><span class="sxs-lookup"><span data-stu-id="0f46e-107">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="0f46e-108">Disse standardverdiene brukes deretter til flere adressebøker du oppretter.</span><span class="sxs-lookup"><span data-stu-id="0f46e-108">These default values are then used for any additional address books that you create.</span></span>

<span data-ttu-id="0f46e-109">**Beslutninger**</span><span class="sxs-lookup"><span data-stu-id="0f46e-109">**Decisions**</span></span>

- <span data-ttu-id="0f46e-110">Hvilken rekkefølge skal navn vises i for partsposter av typen **Person**?</span><span class="sxs-lookup"><span data-stu-id="0f46e-110">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="0f46e-111">For eksempel er én rekkefølge etternavn, mellomnavn og fornavn.</span><span class="sxs-lookup"><span data-stu-id="0f46e-111">For example, one sequence is last name, middle name, first name.</span></span>
- <span data-ttu-id="0f46e-112">Skal partsposter slettes fra adresseboken når rolleposten slettes?</span><span class="sxs-lookup"><span data-stu-id="0f46e-112">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="0f46e-113">Hvis for eksempel en kundepost slettes, skal partsposten også slettes?</span><span class="sxs-lookup"><span data-stu-id="0f46e-113">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
- <span data-ttu-id="0f46e-114">Når en ny post opprettes, skal brukere varsles hvis det finnes en lik post i den globale adresseboken?</span><span class="sxs-lookup"><span data-stu-id="0f46e-114">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
- <span data-ttu-id="0f46e-115">Skal DUNS-nummeret (Data Universal Numbering System) inkluderes i informasjonen til en partspost?</span><span class="sxs-lookup"><span data-stu-id="0f46e-115">Should the Data Universal Numbering System (DUNS) number be included in a party record's information?</span></span>
- <span data-ttu-id="0f46e-116">Hvis DUNS-nummeret er inkludert i en partspost, skal unikheten til nummeret kontrolleres?</span><span class="sxs-lookup"><span data-stu-id="0f46e-116">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
- <span data-ttu-id="0f46e-117">Når det opprettes en partspost i den globale adresseboken, vil du ha en standard partstype, person eller organisasjon?</span><span class="sxs-lookup"><span data-stu-id="0f46e-117">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
- <span data-ttu-id="0f46e-118">Hvilke brukerroller skal ha tilgang til de private adressene og kontaktinformasjonen til partsposter?</span><span class="sxs-lookup"><span data-stu-id="0f46e-118">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="0f46e-119">Flere adressebøker</span><span class="sxs-lookup"><span data-stu-id="0f46e-119">Additional address books</span></span>

<span data-ttu-id="0f46e-120">Når du oppretter den globale adresseboken, kan du opprette flere adressebøker i henhold til behovet ditt, for eksempel en egen adressebok for hvert firma i organisasjonen din eller for hver bransje.</span><span class="sxs-lookup"><span data-stu-id="0f46e-120">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="0f46e-121">Fabrikam er for eksempel en internasjonal organisasjon som har flere firmaer og flere bransjer.</span><span class="sxs-lookup"><span data-stu-id="0f46e-121">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="0f46e-122">Fabrikam planlegger å opprette en adressebok for hver bransje.</span><span class="sxs-lookup"><span data-stu-id="0f46e-122">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="0f46e-123">For bransjer som forekommer mer enn ett sted, for eksempel bransjen for pneumatiske verktøy, planlegger Fabrikam å opprette en adressebok for hver lokasjon.</span><span class="sxs-lookup"><span data-stu-id="0f46e-123">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="0f46e-124">Chris, som er IT-ansvarlig hos Fabrikam, har opprettet listen nedenfor over adressebøker som kreves.</span><span class="sxs-lookup"><span data-stu-id="0f46e-124">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="0f46e-125">Denne listen beskriver også partipostene som hver adressebok må inneholde.</span><span class="sxs-lookup"><span data-stu-id="0f46e-125">This list also describes the party records that each address book must include.</span></span>

- <span data-ttu-id="0f46e-126">**Kontrakter med offentlig sektor (PubSC)** – Partsposter for alle parter som er involvert i kontrakter med offentlig sektor som Fabrikam har inngått.</span><span class="sxs-lookup"><span data-stu-id="0f46e-126">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="0f46e-127">**Kontrakter med privat sektor (PriSC)** – Partsposter for alle parter som er involvert i kontrakter med privat sektor som Fabrikam har inngått.</span><span class="sxs-lookup"><span data-stu-id="0f46e-127">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="0f46e-128">**Elektroniske verktøy (ET)** – Partsposter for alle parter som er involvert i innkjøp eller salg av elektroniske verktøy, eller som ellers bruker elektroniske verktøy som leveres av eller kjøpes for Fabrikam i firmaet Fabrikam-Japan.</span><span class="sxs-lookup"><span data-stu-id="0f46e-128">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="0f46e-129">**Pneumatiske verktøy (PTJPN)** – Partsposter for alle parter som er involvert i innkjøp eller salg av pneumatiske verktøy, eller som ellers bruker pneumatiske verktøy som leveres av eller kjøpes for Fabrikam i firmaet Fabrikam-Japan.</span><span class="sxs-lookup"><span data-stu-id="0f46e-129">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="0f46e-130">**Pneumatiske verktøy (PTUSA)** – Partsposter for alle parter som er involvert i innkjøp eller salg av pneumatiske verktøy, eller som ellers bruker pneumatiske verktøy som leveres av eller kjøpes for Fabrikam i firmaet Fabrikam-USA.</span><span class="sxs-lookup"><span data-stu-id="0f46e-130">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="0f46e-131">**Beslutning:**</span><span class="sxs-lookup"><span data-stu-id="0f46e-131">**Decision:**</span></span>

- <span data-ttu-id="0f46e-132">Hvor mange flere adressebøker vil du opprette?</span><span class="sxs-lookup"><span data-stu-id="0f46e-132">How many additional address books will you create?</span></span>
