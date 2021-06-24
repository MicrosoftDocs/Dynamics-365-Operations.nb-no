---
title: Instrumentbord for bruksstyring
description: Dette emnet forklarer hvordan du bruker instrumentbordet for bruksstyring til å overvåke bruken av tjenesten for elektronisk fakturering og opprettholder samsvar med forskriftene.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130512"
---
# <a name="usage-management-dashboard"></a><span data-ttu-id="18ed2-103">Instrumentbord for bruksstyring</span><span class="sxs-lookup"><span data-stu-id="18ed2-103">Usage management dashboard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18ed2-104">Instrumentbordet **Bruksstyring** hjelper deg å overvåke bruken av tjenesten for elektronisk fakturering, slik at organisasjonen kan opprettholde samsvar med forskriftene når det gjelder månedlig bruk.</span><span class="sxs-lookup"><span data-stu-id="18ed2-104">The **Usage management** dashboard helps you monitor usage of the Electronic Invoicing service, and therefore helps your organization remain compliant in terms of its monthly usage.</span></span> <span data-ttu-id="18ed2-105">Forskriftssamsvar fastsettes ved å beregne innsendingsvolumet og sammenligne det med det tilegnede innsendingsvolumet for å finne eventuelle avvik mellom tilegnet og brukt volum.</span><span class="sxs-lookup"><span data-stu-id="18ed2-105">Compliance is determined by calculating the submission volume and comparing it with the acquired volume of submissions to identify any deviations between the acquired volume and the used volume.</span></span>

<span data-ttu-id="18ed2-106">Instrumentbordet har følgende indikatorer:</span><span class="sxs-lookup"><span data-stu-id="18ed2-106">The dashboard includes the following indicators:</span></span>

- <span data-ttu-id="18ed2-107">Én kostnadsindikator du kan bruke til å overvåke forbruk for å sikre at det er i tråd med lisensen:</span><span class="sxs-lookup"><span data-stu-id="18ed2-107">One cost indicator that you can use to monitor consumption for licensing compliance purposes:</span></span>

    - <span data-ttu-id="18ed2-108">Bruk per måned (eksport)</span><span class="sxs-lookup"><span data-stu-id="18ed2-108">Usage per month (export)</span></span>

- <span data-ttu-id="18ed2-109">Tre driftsindikatorer du kan bruke til å spore bruk av tjenesten for elektronisk fakturering til administrasjonsformål:</span><span class="sxs-lookup"><span data-stu-id="18ed2-109">Three operational indicators that you can use to track usage of the Electronic Invoicing service for management purposes:</span></span>

    - <span data-ttu-id="18ed2-110">Bruk etter funksjon</span><span class="sxs-lookup"><span data-stu-id="18ed2-110">Usage by feature</span></span>
    - <span data-ttu-id="18ed2-111">Bruk etter miljø</span><span class="sxs-lookup"><span data-stu-id="18ed2-111">Usage by environment</span></span>
    - <span data-ttu-id="18ed2-112">Bruk per måned (import)</span><span class="sxs-lookup"><span data-stu-id="18ed2-112">Usage per month (import)</span></span>

## <a name="measurement-scope"></a><span data-ttu-id="18ed2-113">Målingsomfang</span><span class="sxs-lookup"><span data-stu-id="18ed2-113">Measurement scope</span></span>

- <span data-ttu-id="18ed2-114">Måleenhet:</span><span class="sxs-lookup"><span data-stu-id="18ed2-114">Unit of measure:</span></span> 

    <span data-ttu-id="18ed2-115">Instrumentbordet **Bruksstyring** teller forretningsdokumentene som sendes inn, og importerte elektroniske fakturaer.</span><span class="sxs-lookup"><span data-stu-id="18ed2-115">The **Usage management** dashboard counts the submission of business documents and imported electronic invoices.</span></span>

- <span data-ttu-id="18ed2-116">Organisasjon:</span><span class="sxs-lookup"><span data-stu-id="18ed2-116">Organization:</span></span> 

    <span data-ttu-id="18ed2-117">Opptellingen summeres etter leier-ID-en for organisasjonen, uansett antall forekomster av Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management, eller antall juridiske enheter der tjenesten for elektronisk fakturering er aktivert.</span><span class="sxs-lookup"><span data-stu-id="18ed2-117">Counting is summarized by the tenant ID of your organization, regardless of the number of instances of Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management, or the number of legal entities where the Electronic Invoicing service is enabled.</span></span>


## <a name="indicator-usage-per-month-export"></a><span data-ttu-id="18ed2-118">Indikator: Bruk per måned (eksport)</span><span class="sxs-lookup"><span data-stu-id="18ed2-118">Indicator: Usage per month (export)</span></span>

<span data-ttu-id="18ed2-119">Denne indikatoren gir detaljer om de elektroniske fakturaene som organisasjonen utsteder i løpet av en definert periode.</span><span class="sxs-lookup"><span data-stu-id="18ed2-119">This indicator provides details about the electronic invoices that your organization issues during a defined period.</span></span>

### <a name="scope"></a><span data-ttu-id="18ed2-120">Område</span><span class="sxs-lookup"><span data-stu-id="18ed2-120">Scope</span></span>
- <span data-ttu-id="18ed2-121">Antall forretningsdokumenter som sendes fra Finance og Supply Chain Management til tjenesten for elektronisk fakturering, uansett hvor mange linjer disse forretningsdokumentene inneholder.</span><span class="sxs-lookup"><span data-stu-id="18ed2-121">The number of business documents that are submitted from Finance and Supply Chain Management to the Electronic Invoicing service, regardless of number of lines that those business documents contain.</span></span>
- <span data-ttu-id="18ed2-122">Antall innsendte forretningsdokumenter som er behandlet av tjenesten for elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="18ed2-122">The number of submitted business documents that are successfully processed by the Electronic Invoicing service.</span></span> <span data-ttu-id="18ed2-123">Et dokument regnes som behandlet når handlingsflyten som er definert i funksjonskonfigurasjonen, er fullført.</span><span class="sxs-lookup"><span data-stu-id="18ed2-123">A document is considered successfully processed when the flow of actions that are defined in the feature setup is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="18ed2-124">Når en elektronisk faktura sendes til en ekstern nettjeneste, er opptellingen uavhengig av resultatene av nettjenestebehandling (godtatt, avvist eller skjemavalideringsfeil).</span><span class="sxs-lookup"><span data-stu-id="18ed2-124">When an electronic invoice is submitted to an external web service, counting is independent of the results of web service processing (accepted, rejected, or schema validation error).</span></span> <span data-ttu-id="18ed2-125">Hvis nettjenesten mottok og svarte på forespørselen fra tjenesten for elektronisk fakturering, regnes innsendingen som en gyldig telling.</span><span class="sxs-lookup"><span data-stu-id="18ed2-125">If the web service received and responded to the request from the Electronic Invoicing service, the submission is considered a valid counting.</span></span>

- <span data-ttu-id="18ed2-126">**Unntak:** Forretningsdokumenter telles ikke hvis de sendes inn på nytt fra Finance og Supply Chain Management til tjenesten for elektronisk fakturering, for eksempel i scenarioer der det kreves en ny sending av samme forretningsdokument for å endre statusen for den elektroniske fakturaen.</span><span class="sxs-lookup"><span data-stu-id="18ed2-126">**Exception:** Business documents aren't counted if they are resubmitted from Finance and Supply Chain Management to the Electronic Invoicing service, such as in the scenarios where a resubmission of the same business document is required to change the status of the electronic invoice.</span></span> <span data-ttu-id="18ed2-127">Utstedelse av en elektronisk faktura for Brasil (regnskapsdokument) telles for eksempel som gyldig, men annulleringsforespørselen for den telles ikke.</span><span class="sxs-lookup"><span data-stu-id="18ed2-127">For example, issuance of a Brazilian electronic invoice (fiscal document) is counted as valid, but the cancellation request for it isn't counted.</span></span>


### <a name="calculation"></a><span data-ttu-id="18ed2-128">Beregning</span><span class="sxs-lookup"><span data-stu-id="18ed2-128">Calculation</span></span>

<span data-ttu-id="18ed2-129">Beregningen av saldoen utføres som følger:</span><span class="sxs-lookup"><span data-stu-id="18ed2-129">The calculation of the balance is calculated as follows:</span></span>

<span data-ttu-id="18ed2-130">Saldo = Gratis + Kjøpt – Brukt</span><span class="sxs-lookup"><span data-stu-id="18ed2-130">Balance = Free + Purchased – Used</span></span>

<span data-ttu-id="18ed2-131">Der:</span><span class="sxs-lookup"><span data-stu-id="18ed2-131">Where:</span></span>

- <span data-ttu-id="18ed2-132">Gratis:</span><span class="sxs-lookup"><span data-stu-id="18ed2-132">Free:</span></span>
  
    <span data-ttu-id="18ed2-133">Et gratis volum med forretningsdokumenter kunden kan sende inn per måned.</span><span class="sxs-lookup"><span data-stu-id="18ed2-133">A free volume of business documents the customer can submit per month.</span></span> <span data-ttu-id="18ed2-134">Det omfatter en pakke med 100 forretningsdokumenter som kan sendes inn til tjenesten for elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="18ed2-134">It includes a package of 100 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="18ed2-135">Gratisvolumet er ikke kumulativt, og eventuell gjenstående saldo rulles ikke over til neste periode.</span><span class="sxs-lookup"><span data-stu-id="18ed2-135">Free volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="18ed2-136">Kjøpt:</span><span class="sxs-lookup"><span data-stu-id="18ed2-136">Purchased:</span></span>
  
    <span data-ttu-id="18ed2-137">En pakke med 1000 forretningsdokumenter som kan sendes inn til tjenesten for elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="18ed2-137">A package of 1,000 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="18ed2-138">Denne pakken må anskaffes for organisasjonen hver måned.</span><span class="sxs-lookup"><span data-stu-id="18ed2-138">This package must be acquired for your organization on a monthly basis.</span></span> <span data-ttu-id="18ed2-139">Det kjøpte volumet er ikke kumulativt, og eventuell gjenstående saldo rulles ikke over til neste periode.</span><span class="sxs-lookup"><span data-stu-id="18ed2-139">Purchased volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="18ed2-140">Brukt:</span><span class="sxs-lookup"><span data-stu-id="18ed2-140">Used:</span></span> 

    <span data-ttu-id="18ed2-141">Opptellingen av forretningsdokumentinnsendinger til tjenesten for elektronisk fakturering i henhold til definerte kriterier.</span><span class="sxs-lookup"><span data-stu-id="18ed2-141">The count of business document submissions to the Electronic Invoicing service according to defined criteria.</span></span>
   
> [!IMPORTANT]
> <span data-ttu-id="18ed2-142">Hvis organisasjonen har tenkt å overskride det månedlige volumet på 100 gratis innsendinger, kjøper du det høyeste volumet for å sikre at du opptrer i tråd med Microsofts lisenspolicy for tjenesten for elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="18ed2-142">If your organization plans to exceed the monthly volume of 100 free submissions, purchase the peak volume to ensure that you remain compliant with the Microsoft licensing policy for the Electronic Invoicing service.</span></span>
>
> <span data-ttu-id="18ed2-143">Det kjøpte volumet må for tiden angis manuelt i henhold til anskaffelsesdatoen som flere pakker med 1000 innsendinger.</span><span class="sxs-lookup"><span data-stu-id="18ed2-143">Currently, purchased volume must be manually entered, according to the date of acquisition, as multiple packages of 1,000 submissions.</span></span>

## <a name="indicator-usage-by-feature"></a><span data-ttu-id="18ed2-144">Indikator: Bruk etter funksjon</span><span class="sxs-lookup"><span data-stu-id="18ed2-144">Indicator: Usage by feature</span></span>

<span data-ttu-id="18ed2-145">Denne indikatoren viser bruken av funksjoner for elektronisk fakturering til utstedelse av elektroniske fakturaer i løpet av en definert periode.</span><span class="sxs-lookup"><span data-stu-id="18ed2-145">This indicator shows the usage of electronic invoicing features for issuance of electronic invoices during a defined period.</span></span>

- <span data-ttu-id="18ed2-146">Beregning:</span><span class="sxs-lookup"><span data-stu-id="18ed2-146">Calculation:</span></span>
  
    <span data-ttu-id="18ed2-147">Brukt = antall ganger hver funksjon for elektronisk fakturering ble brukt under innsendingen av forretningsdokumenter til tjenesten for elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="18ed2-147">Used = The count of how many times each electronic invoicing feature was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-by-environment"></a><span data-ttu-id="18ed2-148">Indikator: Bruk etter miljø</span><span class="sxs-lookup"><span data-stu-id="18ed2-148">Indicator: Usage by environment</span></span>

<span data-ttu-id="18ed2-149">Denne indikatoren viser bruken av tjenestemiljøer for elektronisk fakturering i løpet av en definert periode.</span><span class="sxs-lookup"><span data-stu-id="18ed2-149">This indicator shows the usage of electronic invoicing service environments during a defined period.</span></span>

- <span data-ttu-id="18ed2-150">Beregning:</span><span class="sxs-lookup"><span data-stu-id="18ed2-150">Calculation:</span></span>
    
    <span data-ttu-id="18ed2-151">Brukt = antall ganger hvert tjenestemiljø for elektronisk fakturering ble brukt under innsendingen av forretningsdokumenter til tjenesten for elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="18ed2-151">Used = The count of how many times each electronic invoicing service environment was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-per-month-import"></a><span data-ttu-id="18ed2-152">Indikator: Bruk per måned (import)</span><span class="sxs-lookup"><span data-stu-id="18ed2-152">Indicator: Usage per month (import)</span></span>

<span data-ttu-id="18ed2-153">Denne indikatoren viser volumet av elektroniske fakturaer som er importert av tjenesten for elektronisk fakturering til Finance og Supply Chain Management i en definert periode.</span><span class="sxs-lookup"><span data-stu-id="18ed2-153">This indicator shows the volume of importation of electronic invoices by Electronic Invoicing service into Finance and Supply Chain Management during a defined period.</span></span>

- <span data-ttu-id="18ed2-154">Område:</span><span class="sxs-lookup"><span data-stu-id="18ed2-154">Scope:</span></span>

    <span data-ttu-id="18ed2-155">Elektroniske fakturaer som importeres til Finance og Supply Chain Management, uansett hvor mange linjer de elektroniske fakturaene inneholder.</span><span class="sxs-lookup"><span data-stu-id="18ed2-155">Electronic invoices that are imported into Finance and Supply Chain Management, regardless of the number of lines that those electronic invoices contain.</span></span>

- <span data-ttu-id="18ed2-156">Beregning:</span><span class="sxs-lookup"><span data-stu-id="18ed2-156">Calculation:</span></span>

    <span data-ttu-id="18ed2-157">Mottatt = opptellingen av importerte elektroniske fakturaer til Finance og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="18ed2-157">Received = The count of imported electronic invoices into Finance and Supply Chain Management.</span></span>

## <a name="functions"></a><span data-ttu-id="18ed2-158">Funksjoner</span><span class="sxs-lookup"><span data-stu-id="18ed2-158">Functions</span></span>
### <a name="purchase"></a><span data-ttu-id="18ed2-159">Kjøp</span><span class="sxs-lookup"><span data-stu-id="18ed2-159">Purchase</span></span>

<span data-ttu-id="18ed2-160">Velg **Kjøp** for å registrere beløpet for de anskaffede innsendingene manuelt, i fanen **Bruk per måned (eksport)**.</span><span class="sxs-lookup"><span data-stu-id="18ed2-160">On the **Usage per month (export)** tab, select **Purchase** to manually register the amount of acquired submissions.</span></span>

<span data-ttu-id="18ed2-161">Velg **Ny** for en gitt dato, og angi antallet **Pakker** som er anskaffet på denne datoen.</span><span class="sxs-lookup"><span data-stu-id="18ed2-161">For a given date, select **New** and enter the number of **Packages** acquired for on that date.</span></span>

<span data-ttu-id="18ed2-162">**Antall** beregnes som følger:</span><span class="sxs-lookup"><span data-stu-id="18ed2-162">The **Quantity** is calculated as:</span></span>

<span data-ttu-id="18ed2-163">Antall = Pakker \* 1,000</span><span class="sxs-lookup"><span data-stu-id="18ed2-163">Quantity = Packages \* 1.000</span></span>

<span data-ttu-id="18ed2-164">Beregnet **Antall** gjenspeiles i **Kjøpt** fra indikatoren **Bruk per måned (eksport)**.</span><span class="sxs-lookup"><span data-stu-id="18ed2-164">The calculated **Quantity** reflects in the **Purchased** from the indicator **Usage per month (export)**.</span></span>

### <a name="update"></a><span data-ttu-id="18ed2-165">Oppdatering</span><span class="sxs-lookup"><span data-stu-id="18ed2-165">Update</span></span>

<span data-ttu-id="18ed2-166">Velg **Oppdater** i handlingsruten for å oppdatere beregningen og dataene som vises på siden og i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="18ed2-166">On the Action Pane, select **Update** to refresh the calculation and update the data shown on the page and in the chart.</span></span>

### <a name="reset-history-data"></a><span data-ttu-id="18ed2-167">Tilbakestill historikkdata</span><span class="sxs-lookup"><span data-stu-id="18ed2-167">Reset history data</span></span>

<span data-ttu-id="18ed2-168">Velg **Tilbakestill loggdata** i handlingsruten for å oppdatere databasen som indikatorene skal beregnes fra.</span><span class="sxs-lookup"><span data-stu-id="18ed2-168">On the Action Pane, select **Reset history data** to refresh the database from where the indicators are calculated.</span></span>




> [!NOTE]
> <span data-ttu-id="18ed2-169">Instrumentbordet **Bruksstyring** viser ikke pengebeløp.</span><span class="sxs-lookup"><span data-stu-id="18ed2-169">The **Usage management** dashboard doesn't show monetary amounts.</span></span> <span data-ttu-id="18ed2-170">Det viser i stedet bare volumet av telte innsendinger og importerte dokumenter.</span><span class="sxs-lookup"><span data-stu-id="18ed2-170">Instead, it shows only the volume of counted submissions and imported documents.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
