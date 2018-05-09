---
title: "Endre et format for elektronisk rapportering ved å bruke en Microsoft Excel-mal på nytt"
description: "Dette emnet inneholder informasjon om hvordan du kan endre formatet for elektronisk rapportering (ER) som brukes til å generere forretningsdokumenter ved å bruke en endret Excel-mal."
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7df2c6e86975a35cd97fabad4d96fb1319d2b6ce
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="modify-an-electronic-reporting-format-by-reapplying-a-microsoft-excel-template"></a><span data-ttu-id="b22e8-103">Endre et format for elektronisk rapportering ved å bruke en Microsoft Excel-mal på nytt</span><span class="sxs-lookup"><span data-stu-id="b22e8-103">Modify an Electronic reporting format by reapplying a Microsoft Excel template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b22e8-104">Verktøyet for elektronisk rapportering (ER) brukes til å generere forretningsdokumenter i et elektronisk format.</span><span class="sxs-lookup"><span data-stu-id="b22e8-104">The Electronic reporting (ER) tool is used to generate business documents in an electronic format.</span></span> <span data-ttu-id="b22e8-105">For å generere et forretningsdokument må du opprette et ER-format og deretter bruke ER-utforming til å definere oppsettet for forretningsdokumentet og angi hvilke data som skal inkluderes i det.</span><span class="sxs-lookup"><span data-stu-id="b22e8-105">To generate a business document, you must create an ER format, and then use the ER designer to define the layout of the business document and specify the data that should be included in it.</span></span> <span data-ttu-id="b22e8-106">Du kan deretter kjøre ER-formatet for å generere forretningsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="b22e8-106">You can then run the ER format to generate the business document.</span></span>

<span data-ttu-id="b22e8-107">ER-verktøyet kan brukes til å generere forretningsdokumenter som Microsoft Excel-filer.</span><span class="sxs-lookup"><span data-stu-id="b22e8-107">The ER tool can be used to generate business documents as Microsoft Excel files.</span></span> <span data-ttu-id="b22e8-108">Du kan bruke et Excel-dokument som en mal for disse dokumentene.</span><span class="sxs-lookup"><span data-stu-id="b22e8-108">You can use an Excel document as a template for these documents.</span></span> <span data-ttu-id="b22e8-109">Hvis du vil definere oppsettet for dokumentet i ER-utformingen, kan du importere innholdet i Excel-dokumentet du vil bruke som mal i det definerte ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="b22e8-109">To define the document layout in the ER designer, you can import the contents of the Excel document that you want to use as a template into the defined ER format.</span></span> <span data-ttu-id="b22e8-110">Hvis du vil ha mer informasjon og prøve dette scenariet, spiller du av oppgaveveiledningen **ER Utforme en konfigurasjon for generering av rapporter i OPENXML-format** (en del av forretningsprosessen 7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)) .</span><span class="sxs-lookup"><span data-stu-id="b22e8-110">For more details, and to practice this scenario, play the task guide **ER Design a configuration for generating reports in OPENXML format** (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span>

<span data-ttu-id="b22e8-111">Hvis du redigerer Excel-dokumentet som brukes som en mal for et forretningsdokument, kan du bruke ny ER-funksjonalitet til å bruke den oppdaterte malen på nytt i ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="b22e8-111">If you edit the Excel document that is used as a template for a business document, new ER functionality lets you reapply the updated template to the ER format.</span></span> <span data-ttu-id="b22e8-112">ER-formatet blir da oppdatert, slik at det samsvarer med den oppdaterte malen.</span><span class="sxs-lookup"><span data-stu-id="b22e8-112">The ER format is then updated so that it adheres to the updated template.</span></span> <span data-ttu-id="b22e8-113">hvis du vil ha mer informasjon om denne funksjonen, kan du spille av oppgaveveiledningen **ER Endre et format for elektronisk rapportering ved å bruke en Microsoft Excel-mal på nytt** (del av forretningsprosessene for 7.5.5.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10683)).</span><span class="sxs-lookup"><span data-stu-id="b22e8-113">For more details about this functionality, play the task guide **ER Modify a format by reapplying an Excel template** (part of the 7.5.5.3 Acquire/Develop IT service/solution components (10683) business process).</span></span> <span data-ttu-id="b22e8-114">I trinnet i oppgaveveiledningen der du importerte en oppdatert mal, kan du bruke den endrede malen for Excel-filen for Betalingsrapport, SampleVendPaymWsReport2, som mal.</span><span class="sxs-lookup"><span data-stu-id="b22e8-114">In the task guide step where you import an updated template, use the modified template of the Payment Report Excel file, SampleVendPaymWsReport2, as a template.</span></span>

