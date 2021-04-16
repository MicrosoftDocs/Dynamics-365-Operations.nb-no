---
title: Arkivere utskrevne kundefakturaer med hash-numre
description: Dette emnet beskriver hvordan du aktiverer arkivering for å lagre utskrevne kundefakturaer med hash-numre.
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5b0305381ee709ce52b18d171a1ea274e2126cce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827704"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a><span data-ttu-id="f7566-103">Arkivere utskrevne kundefakturaer med hash-numre</span><span class="sxs-lookup"><span data-stu-id="f7566-103">Archive printed customer invoices with hash numbers</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="f7566-104">I noen land er det et juridisk krav om å lagre beregnede hash-numre i systemet sammen med utskrifter av enkelte dokumenter.</span><span class="sxs-lookup"><span data-stu-id="f7566-104">In some countries, there is a legal requirement to store calculated hash numbers in the system together with printouts of some documents.</span></span> <span data-ttu-id="f7566-105">Hash-numrene kan brukes til rapportering til myndighetene og i løpet av revisjoner.</span><span class="sxs-lookup"><span data-stu-id="f7566-105">Hash numbers can be used for reporting to authorities and during audits.</span></span>

<span data-ttu-id="f7566-106">Dette emnet beskriver hvordan du konfigurerer arkivering for å lagre utskrevne kundefakturaer med hash-numre.</span><span class="sxs-lookup"><span data-stu-id="f7566-106">This topic explains how to configure archiving in order to store printed customer invoices with hash numbers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f7566-107">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="f7566-107">Prerequisites</span></span>

- <span data-ttu-id="f7566-108">I arbeidsområdet **Funksjonsstyring** aktiverer du funksjonen **Arkiver utskrevne kundefakturaer med hash-numre**.</span><span class="sxs-lookup"><span data-stu-id="f7566-108">In the **Feature management** workspace, turn on the feature, **Archive printed customer invoices with hash numbers**.</span></span> <span data-ttu-id="f7566-109">Hvis du vil ha mer informasjon, kan du se [Oversikt over funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f7566-109">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="f7566-110">Konfigurer de utskriftsbare formatene for de obligatoriske dokumentene i **Utskriftsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="f7566-110">Configure the printable formats of required documents in **Print management**.</span></span>

<span data-ttu-id="f7566-111">Denne funksjonaliteten gjelder for dokumentene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="f7566-111">This functionality is applicable to the following documents.</span></span>

<span data-ttu-id="f7566-112">**Kunde**</span><span class="sxs-lookup"><span data-stu-id="f7566-112">**Accounts receivable**</span></span>
- <span data-ttu-id="f7566-113">Kundefaktura</span><span class="sxs-lookup"><span data-stu-id="f7566-113">Customer invoice</span></span>
- <span data-ttu-id="f7566-114">Kundekreditnota</span><span class="sxs-lookup"><span data-stu-id="f7566-114">Customer credit note</span></span>
- <span data-ttu-id="f7566-115">Fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="f7566-115">Free text invoice</span></span>
- <span data-ttu-id="f7566-116">Fritekstkreditnota</span><span class="sxs-lookup"><span data-stu-id="f7566-116">Free text credit note</span></span>

<span data-ttu-id="f7566-117">**Prosjektstyring og regnskap**</span><span class="sxs-lookup"><span data-stu-id="f7566-117">**Project management and accounting**</span></span>
- <span data-ttu-id="f7566-118">Prosjektfaktura</span><span class="sxs-lookup"><span data-stu-id="f7566-118">Project invoice</span></span>
- <span data-ttu-id="f7566-119">Prosjektkreditnota</span><span class="sxs-lookup"><span data-stu-id="f7566-119">Project credit note</span></span>

## <a name="configure-customer-master-data"></a><span data-ttu-id="f7566-120">Konfigurere kundehoveddata</span><span class="sxs-lookup"><span data-stu-id="f7566-120">Configure customer master data</span></span>
<span data-ttu-id="f7566-121">Fullfør fremgangsmåten nedenfor for å konfigurere kundedata, og slå på muligheten til å lagre utskrevne fakturaer automatisk som vedlegg.</span><span class="sxs-lookup"><span data-stu-id="f7566-121">Complete the following steps to configure customer data and turn on the ability to automatically save printed invoices as attachments.</span></span>

1. <span data-ttu-id="f7566-122">Gå til **Kunder** > **Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="f7566-122">Go to **Accounts receivable** > **All customers**.</span></span> 
2. <span data-ttu-id="f7566-123">Velg en kunde, og velg **Ja** i feltet **Vedlegg til eFaktura** i delen **E-FAKTURA** i hurtigfanen **Faktura og levering**.</span><span class="sxs-lookup"><span data-stu-id="f7566-123">Select a customer, and on the **Invoice and delivery** FastTab, in the **E-INVOCE** section, in the **eInvoice attachment** field, select **Yes**.</span></span>

## <a name="print-invoices"></a><span data-ttu-id="f7566-124">Skriv ut fakturaer</span><span class="sxs-lookup"><span data-stu-id="f7566-124">Print invoices</span></span>
<span data-ttu-id="f7566-125">Du kan postere og skrive ut en hvilken som helst fritekst-, kunde- eller prosjektfaktura eller kreditnota for kunden som ble konfigurert i forrige fremgangsmåte.</span><span class="sxs-lookup"><span data-stu-id="f7566-125">You can post and print any free text, customer, and project invoice or credit note for the customer configured in the previous procedure.</span></span>

<span data-ttu-id="f7566-126">Åpne siden **Vedlegg** for den utskrevne fakturaen.</span><span class="sxs-lookup"><span data-stu-id="f7566-126">Open the **Attachments** page for the printed invoice.</span></span> <span data-ttu-id="f7566-127">I feltet **Hash-nummer for dokument** i gruppen **Tilleggsdetaljer** i hurtigfanen **Vedlegg** finner du det lagrede hash-nummeret beregnet for den utskrevne fakturaen.</span><span class="sxs-lookup"><span data-stu-id="f7566-127">On the **Attachment** FastTab, in the **Additional details** field group, in **Document hash number** field, find the stored hash number calculated for the printed invoice.</span></span>

![Hash-nummer for vedlegg](media/attach-hash-num.jpg)

