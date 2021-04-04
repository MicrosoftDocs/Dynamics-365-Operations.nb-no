---
title: Vise og evaluere resultatene i spørreskjemaer
description: Denne artikkelen forklarer hvordan du kan vise og evaluere resultatene av spørreskjemaer som respondenter fyller ut.
author: andreabichsel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 54530a8735cb8ce4b21688eae86fda83035133ed
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464964"
---
# <a name="view-and-evaluate-the-results-of-questionnaires"></a><span data-ttu-id="f941e-103">Vise og evaluere resultatene i spørreskjemaer</span><span class="sxs-lookup"><span data-stu-id="f941e-103">View and evaluate the results of questionnaires</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f941e-104">Denne artikkelen forklarer hvordan du kan vise og evaluere resultatene av spørreskjemaer som respondenter fyller ut.</span><span class="sxs-lookup"><span data-stu-id="f941e-104">This article explains how you can view and evaluate the results of questionnaires that respondents complete.</span></span> 

<span data-ttu-id="f941e-105">Etter at respondentene har fylt ut et spørreskjema, kan du vise og evaluere spørreskjemaresultatene på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="f941e-105">After respondents complete a questionnaire, you can view and evaluate the questionnaire results in the following ways:</span></span>

-   <span data-ttu-id="f941e-106">**Fullførte svarøkter** – Vis informasjon om spørreskjemaene som respondentene har fylt ut, og generer rapporter for å oppsummere svar og eventuelle poeng de har fått.</span><span class="sxs-lookup"><span data-stu-id="f941e-106">**Completed answer sessions** – View details about the questionnaires that respondents have completed, and generate reports to summarize answers and any points that were earned.</span></span>
-   <span data-ttu-id="f941e-107">**Resultatgrupper** – Vis resultatgruppedetaljer og -statistikk for spørreskjemaer.</span><span class="sxs-lookup"><span data-stu-id="f941e-107">**Result groups** – View result group details and statistics for questionnaires.</span></span> <span data-ttu-id="f941e-108">Resultatgruppestatistikk kan genereres for én svarøkt i et spørreskjema eller alle svarøkter.</span><span class="sxs-lookup"><span data-stu-id="f941e-108">Result group statistics can be generated for either a single answer session  of a questionnaire or all answer sessions.</span></span>
-   <span data-ttu-id="f941e-109">**Spørreskjemastatistikk** – Angi vilkår for å beregne statistikk for en bestemt gruppe med respondenter.</span><span class="sxs-lookup"><span data-stu-id="f941e-109">**Questionnaire statistics** – Specify criteria to calculate statistics for a specific group of respondents.</span></span>

<span data-ttu-id="f941e-110">Du kan også generere ulike rapporter for å vise resultater som er sortert etter person, svarøkt eller resultatgruppe.</span><span class="sxs-lookup"><span data-stu-id="f941e-110">You can also generate various reports to view results that are sorted by person, answer session, or result group.</span></span> <span data-ttu-id="f941e-111">Følgende rapporter som er knyttet til utfylte spørreskjemaer, er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="f941e-111">The following reports that are related to completed questionnaires are available:</span></span>

-   <span data-ttu-id="f941e-112">Svar</span><span class="sxs-lookup"><span data-stu-id="f941e-112">Answers</span></span>
-   <span data-ttu-id="f941e-113">Svar per spørreskjema</span><span class="sxs-lookup"><span data-stu-id="f941e-113">Answers per questionnaire</span></span>
-   <span data-ttu-id="f941e-114">Svar per person</span><span class="sxs-lookup"><span data-stu-id="f941e-114">Answers per person</span></span>
-   <span data-ttu-id="f941e-115">Tilbakemeldingsanalyse</span><span class="sxs-lookup"><span data-stu-id="f941e-115">Feedback analysis</span></span>

## <a name="answer-session-results"></a><span data-ttu-id="f941e-116">Resultater fra svarøkt</span><span class="sxs-lookup"><span data-stu-id="f941e-116">Answer session results</span></span>

<span data-ttu-id="f941e-117">Etter at respondentene har fylt ut et spørreskjema, kan du vise resultatene fra de fullførte svarøktene.</span><span class="sxs-lookup"><span data-stu-id="f941e-117">After respondents complete a questionnaire, you can view the results of the completed answer sessions.</span></span> <span data-ttu-id="f941e-118">En svarøkt er én brukers svar på et spørreskjema.</span><span class="sxs-lookup"><span data-stu-id="f941e-118">An answer session is one user’s response to a questionnaire.</span></span> <span data-ttu-id="f941e-119">Du kan vise detaljer om fullførte svarøkter på **Svar**-siden.</span><span class="sxs-lookup"><span data-stu-id="f941e-119">You can view details about completed answer sessions on the **Answers** page.</span></span> <span data-ttu-id="f941e-120">Svarøktene som er inkludert på **Svar**-siden, filtreres på ulike måter avhengig av hvordan du åpner siden:</span><span class="sxs-lookup"><span data-stu-id="f941e-120">The answer sessions that are included on the **Answers** page are filtered in various ways, depending on how you open the page:</span></span>

-   <span data-ttu-id="f941e-121">Alle spørreskjemaer</span><span class="sxs-lookup"><span data-stu-id="f941e-121">All questionnaires</span></span>
-   <span data-ttu-id="f941e-122">Et bestemt spørreskjema</span><span class="sxs-lookup"><span data-stu-id="f941e-122">A specific questionnaire</span></span>
-   <span data-ttu-id="f941e-123">En bestemt person</span><span class="sxs-lookup"><span data-stu-id="f941e-123">A specific person</span></span>

<span data-ttu-id="f941e-124">På **Svar**-siden kan du vise detaljer om svar, poeng respondenten har fått, svar fra en respondent i hver resultatgruppe og spørsmålshierarkiet som ble brukt på det valgte spørreskjemaet, hvis et spørsmålshierarki ble brukt.</span><span class="sxs-lookup"><span data-stu-id="f941e-124">From the **Answers** page, you can view details about answers, points that were earned, a respondent’s responses in each result group, and the question hierarchy that was used on the selected questionnaire, if a question hierarchy was used.</span></span> <span data-ttu-id="f941e-125">Du kan også generere og skrive ut følgende rapporter:</span><span class="sxs-lookup"><span data-stu-id="f941e-125">You can also generate and print the following reports:</span></span>

-   <span data-ttu-id="f941e-126">**Resultatrapport** – Denne rapporten viser en grafisk representasjon av poengene som ble oppnådd per resultatgruppe for den valgte svarøkten.</span><span class="sxs-lookup"><span data-stu-id="f941e-126">**Results report** – This report shows a graphical representation of the points that were earned per result group for the selected answer session.</span></span>
-   <span data-ttu-id="f941e-127">**Svarrapport** – Denne rapporten viser svarene som respondenten valgte for hvert spørsmål i spørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="f941e-127">**Answer report** – This report shows the answers that the respondent selected for each question on the questionnaire.</span></span>
-   <span data-ttu-id="f941e-128">**Feil svar** – Denne rapporten viser informasjon som er knyttet til de uriktige svarene som respondenten har valgt.</span><span class="sxs-lookup"><span data-stu-id="f941e-128">**Incorrect answers** – This report shows information that is related to the incorrect answers that the respondent selected.</span></span>

> [!NOTE]
> <span data-ttu-id="f941e-129">**Resultater**-rapporten er bare tilgjengelig hvis du bruker resultatgrupper i spørreskjemaet, og hvis du har valgt **Resultatside** på **Spørreskjemaer**-siden.</span><span class="sxs-lookup"><span data-stu-id="f941e-129">The **Results** report is available only if you use results groups on the questionnaire, and if you selected **Results page** on the **Questionnaires** page.</span></span> <span data-ttu-id="f941e-130">**Svar**-rapporten og **Feil svar**-rapporten er bare tilgjengelige hvis du har valgt **Svarrapport** på **Spørreskjemaer**-siden.</span><span class="sxs-lookup"><span data-stu-id="f941e-130">The **Answer** report and the **Incorrect answers** report are available only if you selected **Answer report** on the **Questionnaires** page.</span></span>

## <a name="questionnaire-statistics"></a><span data-ttu-id="f941e-131">Spørreskjemastatistikk</span><span class="sxs-lookup"><span data-stu-id="f941e-131">Questionnaire statistics</span></span>

<span data-ttu-id="f941e-132">Du kan bruke spørreskjemastatistikk til å analysere resultatene av et utfylt spørreskjema, basert på beregninger du definerer.</span><span class="sxs-lookup"><span data-stu-id="f941e-132">You can use questionnaire statistics to analyze the results of a completed questionnaire, based on calculations that you define.</span></span> <span data-ttu-id="f941e-133">Hvis du vil definere beregninger, må du utføre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="f941e-133">To define calculations, you must complete the following tasks:</span></span>

-   <span data-ttu-id="f941e-134">Velg kriterier for å beregne og vise statistikken.</span><span class="sxs-lookup"><span data-stu-id="f941e-134">Select criteria to calculate and display the statistics.</span></span>
    -   <span data-ttu-id="f941e-135">Du kan vise statistikk per spørreskjema, spørsmål, spørsmålsrader eller resultatgrupper.</span><span class="sxs-lookup"><span data-stu-id="f941e-135">You can show statistics by questionnaire, questions, question rows, or results groups.</span></span>
    -   <span data-ttu-id="f941e-136">Velg diagramtypen som skal brukes når du viser resultatene.</span><span class="sxs-lookup"><span data-stu-id="f941e-136">Select the type of chart that will be used when you view results.</span></span>
    -   <span data-ttu-id="f941e-137">Velg typene personer fra nettverket, for eksempel ansatte, kontaktpersoner eller søkere, du vil ta med svar for.</span><span class="sxs-lookup"><span data-stu-id="f941e-137">Select the types of people from the network, such as employees, contact persons, or applicants, to include answers for.</span></span> <span data-ttu-id="f941e-138">Du kan også ta med svar fra spørreskjemaer som ble fylt ut anonymt.</span><span class="sxs-lookup"><span data-stu-id="f941e-138">You can also include answers from questionnaires that were completed anonymously.</span></span>
    -   <span data-ttu-id="f941e-139">Definer intervaller som er basert på alder eller ansiennitet for å analysere resultater.</span><span class="sxs-lookup"><span data-stu-id="f941e-139">Set up intervals that are based on age or seniority to analyze results.</span></span>
-   <span data-ttu-id="f941e-140">Velg eller kontroller innstillinger som innsnevrer temaet for statistikken.</span><span class="sxs-lookup"><span data-stu-id="f941e-140">Select or verify settings that refine the subject of the statistics.</span></span> <span data-ttu-id="f941e-141">Når du velger et postnummer, kan du for eksempel analysere resultatene for alle respondentene innenfor et bestemt geografisk område.</span><span class="sxs-lookup"><span data-stu-id="f941e-141">For example, by selecting a ZIP Code or postal code, you can analyze results for all respondents within a specific geographic area.</span></span>
-   <span data-ttu-id="f941e-142">Velg eller kontroller vilkår for å analysere resultatene etter respondent eller spørreskjemaets kjennetegn.</span><span class="sxs-lookup"><span data-stu-id="f941e-142">Select or verify criteria to analyze results by respondent or questionnaire characteristics.</span></span> <span data-ttu-id="f941e-143">Hvis du for eksempel velger **Postnummer**, kan du analysere sammenhengen mellom respondentens plassering og riktige svar.</span><span class="sxs-lookup"><span data-stu-id="f941e-143">For example, by selecting **ZIP/postal code**, you can analyze the correlation between a respondent’s location and correct answers.</span></span>

<span data-ttu-id="f941e-144">Innstillingene du definerer, lagres og kan brukes til å beregne resultatene på nytt periodisk.</span><span class="sxs-lookup"><span data-stu-id="f941e-144">The settings that you define are saved and can be used to periodically recalculate results.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]