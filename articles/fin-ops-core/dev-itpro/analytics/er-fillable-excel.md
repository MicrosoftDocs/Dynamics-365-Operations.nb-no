---
title: Utforme en konfigurasjon til å generere dokumenter i Excel-format
description: Dette emnet inneholder informasjon om hvordan du utformer et format for elektronisk rapportering (ER) for å fylle ut en Excel-mal, og deretter generere utgående dokumenter i Excel-format.
author: NickSelin
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e889b08f10c5d0c95fed7c9e422340706bdd154a
ms.sourcegitcommit: 67ce81c57194afb26a04ae4c0b7509e0efa32afc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/14/2020
ms.locfileid: "3375819"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a><span data-ttu-id="a648a-103">Utforme en konfigurasjon til å generere dokumenter i Excel-format</span><span class="sxs-lookup"><span data-stu-id="a648a-103">Design a configuration for generating documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a648a-104">Du kan utforme en konfigurasjon av format for [Elektronisk rapportering (ER)](general-electronic-reporting.md) som har en [formatkomponent](general-electronic-reporting.md#FormatComponentOutbound) for ER som du kan konfigurere til å generere et utgående dokument i et Microsoft Excel-arbeidsbokformat.</span><span class="sxs-lookup"><span data-stu-id="a648a-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) format configuration that has an ER [format component](general-electronic-reporting.md#FormatComponentOutbound) that you can configure to generate an outbound document in a Microsoft Excel workbook format.</span></span> <span data-ttu-id="a648a-105">Spesielle formatkomponenter for ER må brukes til dette formålet.</span><span class="sxs-lookup"><span data-stu-id="a648a-105">Specific ER format components must be used for this purpose.</span></span>

<span data-ttu-id="a648a-106">Hvis du vil ha mer informasjon om denne funksjonen, kan du følge fremgangsmåten i emnet [Utforme en konfigurasjon for generering av rapporter i OPENXML-format](tasks/er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="a648a-106">To learn more about this feature, follow the steps in the topic, [Design a configuration for generating reports in OPENXML format](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="add-a-new-er-format"></a><span data-ttu-id="a648a-107">Legge til et nytt ER-format</span><span class="sxs-lookup"><span data-stu-id="a648a-107">Add a new ER format</span></span>

<span data-ttu-id="a648a-108">Når du legger til en ny formatkonfigurasjon for ER for å generere et utgående dokument i et Excel-arbeidsbokformat, må du velge **Excel**-verdien for attributtet **Formattype** for formatet, eller la verdien for attributtet **Formattype** stå tom.</span><span class="sxs-lookup"><span data-stu-id="a648a-108">When you add a new ER format configuration to generate an outbound document in an Excel workbook format, you must either select the **Excel** value for the **Format type** attribute of the format or leave the **Format type** attribute blank.</span></span>

- <span data-ttu-id="a648a-109">Hvis du velger **Excel**, kan du konfigurere formatet til å generere et utgående dokument bare i Excel-format.</span><span class="sxs-lookup"><span data-stu-id="a648a-109">If you select **Excel**, you can configure the format to generate an outbound document only in Excel format.</span></span>
- <span data-ttu-id="a648a-110">Hvis du lar attributtet stå tomt, kan du konfigurere formatet til å generere et utgående dokument i et format som støttes av ER-rammeverket.</span><span class="sxs-lookup"><span data-stu-id="a648a-110">If you leave the attribute blank, you can configure the format to generate an outbound document in any format that is supported by the ER framework.</span></span>

<span data-ttu-id="a648a-111">Hvis du vil konfigurere formatkomponenten for ER for konfigurasjonen, velger du **Utforming** i handlingsruten og åpner formatkomponenten for ER for redigering i ER-operasjonsutformingen.</span><span class="sxs-lookup"><span data-stu-id="a648a-111">To configure the ER format component of the configuration, select **Designer** on the Action Pane, and open the ER format component for editing in the ER Operation designer.</span></span>

![Siden Konfigurasjoner](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a><span data-ttu-id="a648a-113">Komponent for Excel-fil</span><span class="sxs-lookup"><span data-stu-id="a648a-113">Excel file component</span></span>

### <a name="manual-entry"></a><span data-ttu-id="a648a-114">Manuell oppføring</span><span class="sxs-lookup"><span data-stu-id="a648a-114">Manual entry</span></span>

<span data-ttu-id="a648a-115">Du må legge til en **Excel\\Fil**-komponent for det konfigurerte ER-formatet for å generere et utgående dokument i Excel-format.</span><span class="sxs-lookup"><span data-stu-id="a648a-115">You must add an **Excel\\File** component to the configured ER format to generate an outbound document in Excel format.</span></span>

![Excel\Fil-komponent](./media/er-excel-format-add-file-component.png)

<span data-ttu-id="a648a-117">Hvis du vil angi oppsettet for det utgående dokumentet, knytter du en Excel-arbeidsbok som har filtypen XLSX, til **Excel-\\Fil**-komponenten som malen for utgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="a648a-117">To specify the layout of the outbound document, attach an Excel workbook that has the .xlsx extension to the **Excel\\File** component as the template for outbound documents.</span></span>

> [!NOTE]
> <span data-ttu-id="a648a-118">Når du knytter en mal manuelt, må du bruke en [dokumenttype](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) som er konfigurert for dette formålet i [ER-parameterne](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span><span class="sxs-lookup"><span data-stu-id="a648a-118">When you manually attach a template, you must use a [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) that has been configured for that purpose in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span></span>

![Legge til et vedlegg i Excel\Fil-komponenten](./media/er-excel-format-add-file-component2.png)

<span data-ttu-id="a648a-120">Hvis du vil angi hvordan den tilknyttede malen skal fylles ut når du kjører det konfigurerte ER-formatet, må du legge til nestede komponenter av typen **Ark**, **Område** og **Celle** i **Excel\\Fil**-komponenten.</span><span class="sxs-lookup"><span data-stu-id="a648a-120">To specify how the attached template will be filled in when you run the configured ER format, you must add nested **Sheet**, **Range**, and **Cell** components to the **Excel\\File** component.</span></span> <span data-ttu-id="a648a-121">Hver nestede komponent må knyttes til et Excel-navngitt element.</span><span class="sxs-lookup"><span data-stu-id="a648a-121">Each nested component must be associated with an Excel named item.</span></span>

### <a name="template-import"></a><span data-ttu-id="a648a-122">Malimport</span><span class="sxs-lookup"><span data-stu-id="a648a-122">Template import</span></span>

<span data-ttu-id="a648a-123">Du kan velge **Importer fra Excel** i kategorien **Import** i handlingsruten for å importere en ny mal til et tomt ER-format.</span><span class="sxs-lookup"><span data-stu-id="a648a-123">You can select **Import from Excel** on the **Import** tab of the Action Pane to import a new template into a blank ER format.</span></span> <span data-ttu-id="a648a-124">I dette eksemplet opprettes det en **Excel\\Fil**-komponent automatisk, og den importerte malen blir knyttet til den.</span><span class="sxs-lookup"><span data-stu-id="a648a-124">In this example, an **Excel\\File** component will be created automatically, and the imported template will be attached to it.</span></span> <span data-ttu-id="a648a-125">Alle nødvendige ER-komponenter vil også bli opprettet automatisk, basert på listen over Excel-navngitte elementer som blir funnet.</span><span class="sxs-lookup"><span data-stu-id="a648a-125">All required ER components will also be created automatically, based on the list of Excel named items that are discovered.</span></span>

![Velge Importer fra Excel](./media/er-excel-format-import-template.png)

> [!NOTE]
> <span data-ttu-id="a648a-127">Hvis du vil opprette det valgfrie elementet **Ark** i det redigerbare ER-formatet, setter du alternativet **Opprett Excel-ark-element** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a648a-127">If you want to create the optional **Sheet** element in the editable ER format, set the **Create Excel Sheet format element** option to **Yes**.</span></span>

## <a name="sheet-component"></a><span data-ttu-id="a648a-128">Komponenten Ark</span><span class="sxs-lookup"><span data-stu-id="a648a-128">Sheet component</span></span>

<span data-ttu-id="a648a-129">Komponenten **Ark** viser et regneark i den vedlagte Excel-arbeidsboken som må fylles ut.</span><span class="sxs-lookup"><span data-stu-id="a648a-129">The **Sheet** component indicates a worksheet of the attached Excel workbook that must be filled in.</span></span> <span data-ttu-id="a648a-130">Navnet på regnearket i en Excel-mal er definert i komponenten **Ark** for denne komponenten.</span><span class="sxs-lookup"><span data-stu-id="a648a-130">The name of the worksheet in an Excel template is defined in the **Sheet** property of this component.</span></span>

> [!NOTE]
> <span data-ttu-id="a648a-131">Denne komponenten er valgfri for Excel-arbeidsbøker som inneholder ett regneark.</span><span class="sxs-lookup"><span data-stu-id="a648a-131">This component is optional for Excel workbooks that contain a single worksheet.</span></span>

<span data-ttu-id="a648a-132">I kategorien **Tilordning** for ER-operasjonsutformingen kan du konfigurere egenskapen **Aktivert** for en **Ark**-komponent for å angi om komponenten må plasseres i et generert dokument:</span><span class="sxs-lookup"><span data-stu-id="a648a-132">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Sheet** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="a648a-133">Hvis et uttrykk for egenskapen **Aktivert** er konfigurert til å returnere **Sann** under kjøring, eller hvis ingen uttrykk er konfigurert i det hele tatt, vil det aktuelle regnearket plasseres i det genererte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="a648a-133">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate worksheet will be put in the generated document.</span></span>
- <span data-ttu-id="a648a-134">Hvis et uttrykk for egenskapen **Aktivert** er konfigurert til å returnere **Usann** under kjøring, vil det genererte dokumentet ikke inneholde et regneark.</span><span class="sxs-lookup"><span data-stu-id="a648a-134">If an expression of the **Enabled** property is configured to return **False** at runtime, the generated document won't contain a worksheet.</span></span>

![Eksempel på en arkkomponent](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a><span data-ttu-id="a648a-136">Områdekomponent</span><span class="sxs-lookup"><span data-stu-id="a648a-136">Range component</span></span>

<span data-ttu-id="a648a-137">Komponenten **Område** angir et Excel-område som må kontrolleres av denne ER-komponenten.</span><span class="sxs-lookup"><span data-stu-id="a648a-137">The **Range** component indicates an Excel range that must be controlled by this ER component.</span></span> <span data-ttu-id="a648a-138">Navnet på området er definert i egenskapen **Excel-område** for denne komponenten.</span><span class="sxs-lookup"><span data-stu-id="a648a-138">The name of the range is defined in the **Excel range** property of this component.</span></span>

<span data-ttu-id="a648a-139">Egenskapen **Replikeringsretning** angir om og hvordan området skal gjentas i et generert dokument:</span><span class="sxs-lookup"><span data-stu-id="a648a-139">The **Replication direction** property specifies whether and how the range will be repeated in a generated document:</span></span>

- <span data-ttu-id="a648a-140">Hvis egenskapen **Replikeringsretning** er satt til **Ingen replikering**, blir ikke det riktige Microsoft Excel-området gjentatt i det genererte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="a648a-140">If the **Replication direction** property is set to **No replication**, the appropriate Excel range won't be repeated in the generated document.</span></span>
- <span data-ttu-id="a648a-141">Hvis egenskapen **Replikeringsretning** er satt til **Vertikal**, blir ikke det riktige Microsoft Excel-området gjentatt i det genererte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="a648a-141">If the **Replication direction** property is set to **Vertical**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="a648a-142">Hvert replikerte område er plassert under det opprinnelige området i en Excel-mal.</span><span class="sxs-lookup"><span data-stu-id="a648a-142">Every replicated range is put below the original range in an Excel template.</span></span> <span data-ttu-id="a648a-143">Antall repetisjoner defineres av antall poster i en datakilde for typen **Postliste** som er bundet til denne ER-komponenten.</span><span class="sxs-lookup"><span data-stu-id="a648a-143">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>
- <span data-ttu-id="a648a-144">Hvis egenskapen **Replikeringsretning** er satt til **Horisontal**, blir ikke det riktige Microsoft Excel-området gjentatt i det genererte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="a648a-144">If the **Replication direction** property is set to **Horizontal**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="a648a-145">Hvert replikerte område er plassert til høyre for det opprinnelige området i en Excel-mal.</span><span class="sxs-lookup"><span data-stu-id="a648a-145">Every replicated range is put to the right of the original range in an Excel template.</span></span> <span data-ttu-id="a648a-146">Antall repetisjoner defineres av antall poster i en datakilde for typen **Postliste** som er bundet til denne ER-komponenten.</span><span class="sxs-lookup"><span data-stu-id="a648a-146">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>

<span data-ttu-id="a648a-147">Hvis du vil finne ut mer om horisontal replikering, kan du følge trinnene i [Bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk](tasks/er-horizontal-1.md).</span><span class="sxs-lookup"><span data-stu-id="a648a-147">To learn more about horizontal replication, follow the steps in [Use horizontally expandable ranges to dynamically add columns in Excel reports](tasks/er-horizontal-1.md).</span></span>

<span data-ttu-id="a648a-148">Komponenten **Område** kan ha andre nestede komponenter som brukes til å angi verdier i de riktige navngitte områdene i Excel.</span><span class="sxs-lookup"><span data-stu-id="a648a-148">The **Range** component can have other nested ER components that are used to enter values in the appropriate Excel named ranges.</span></span>

- <span data-ttu-id="a648a-149">Hvis en av komponentene i gruppen **Tekst** brukes til å angi verdier, angis verdien i et Excel-område som en tekstverdi.</span><span class="sxs-lookup"><span data-stu-id="a648a-149">If any component of the **Text** group is used to enter values, the value is entered in an Excel range as a text value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a648a-150">Bruk dette mønsteret til å formatere angitte verdier basert på den nasjonale innstillingen som er definert i appen.</span><span class="sxs-lookup"><span data-stu-id="a648a-150">Use this pattern to format entered values based on the locale that is defined in the application.</span></span>

- <span data-ttu-id="a648a-151">Hvis komponenten **Celle** i **Excel**-gruppen brukes til å angi verdier, angis verdien i et Excel-område som en verdi av datatypen som er definert av bindingen for den **Celle**-komponenten (for eksempel **Streng**, **Kommatall** eller **Heltall**).</span><span class="sxs-lookup"><span data-stu-id="a648a-151">If the **Cell** component of the **Excel** group is used to enter values, the value is entered in an Excel range as a value of the data type that is defined by the binding of that **Cell** component (for example, **String**, **Real**, or **Integer**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="a648a-152">Bruk dette mønsteret til å la Excel formatere angitte verdier basert på den nasjonale innstillingen til den lokale datamaskinen som åpner det utgående dokumentet.</span><span class="sxs-lookup"><span data-stu-id="a648a-152">Use this pattern to enable the Excel application to format entered values based on the locale of the local computer that opens the outbound document.</span></span>

<span data-ttu-id="a648a-153">I kategorien **Tilordning** for ER-operasjonsutformingen kan du konfigurere egenskapen **Aktivert** for en **Område**-komponent for å angi om komponenten må plasseres i et generert dokument:</span><span class="sxs-lookup"><span data-stu-id="a648a-153">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Range** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="a648a-154">Hvis et uttrykk for egenskapen **Aktivert** er konfigurert til å returnere **Sann** under kjøring, eller hvis ingen uttrykk er konfigurert i det hele tatt, vil det aktuelle området bli fylt ut i det genererte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="a648a-154">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate range will be filled in in the generated document.</span></span>
- <span data-ttu-id="a648a-155">Hvis et uttrykk for egenskapen **Aktivert** er konfigurert til å returnere **Usann** under kjøring, og hvis området ikke representerer hele rader eller kolonner, vil ikke det aktuelle området fylles ut i det genererte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="a648a-155">If an expression of the **Enabled** property is configured to return **False** at runtime, and if this range doesn't represent the entire rows or columns, the appropriate range won't be filled in in the generated document.</span></span>
- <span data-ttu-id="a648a-156">Hvis et uttrykk for egenskapen **Aktivert** er konfigurert til å returnere **Usann** under kjøring, og hvis området representerer hele rader eller kolonner, vil det genererte dokumentet inneholde de radene og kolonnene som skjulte rader og kolonner.</span><span class="sxs-lookup"><span data-stu-id="a648a-156">If an expression of the **Enabled** property is configured to return **False** at runtime, and this range represents the entire rows or columns, the generated document will contain those rows and columns as hidden rows and columns.</span></span>

## <a name="cell-component"></a><span data-ttu-id="a648a-157">Komponenten Celle</span><span class="sxs-lookup"><span data-stu-id="a648a-157">Cell component</span></span>

<span data-ttu-id="a648a-158">Komponenten **Celle** brukes til å fylle ut Excel-navngitte celler, figurer og bilder.</span><span class="sxs-lookup"><span data-stu-id="a648a-158">The **Cell** component is used to fill in Excel named cells, shapes, and pictures.</span></span> <span data-ttu-id="a648a-159">Hvis du vil angi et Excel-navngitt objekt som må fylles ut av en ER-komponent ofr **Celle**, må du angi navnet på dette objektet i egenskapen **Excel-område** for komponenten **Celle**.</span><span class="sxs-lookup"><span data-stu-id="a648a-159">To indicate an Excel named object that must be filled in by a **Cell** ER component, you must specify the name of that object in the **Excel range** property of the **Cell** component.</span></span>

<span data-ttu-id="a648a-160">I kategorien **Tilordning** for ER-operasjonsutformingen kan du konfigurere egenskapen **Aktivert** for en **Celle**-komponent for å angi om objektet må fylles ut i et generert dokument:</span><span class="sxs-lookup"><span data-stu-id="a648a-160">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Cell** component to specify whether the object must be filled in in a generated document:</span></span>

- <span data-ttu-id="a648a-161">Hvis et uttrykk for egenskapen **Aktivert** er konfigurert til å returnere **Sann** under kjøring, eller hvis ingen uttrykk er konfigurert i det hele tatt, vil det aktuelle objektet bli fylt ut i det genererte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="a648a-161">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate object will be filled in in the generated document.</span></span> <span data-ttu-id="a648a-162">Bindingen for denne **Celle**-komponenten angir en verdi som plasseres i det aktuelle objektet.</span><span class="sxs-lookup"><span data-stu-id="a648a-162">The binding of this **Cell** component specifies a value that is put in the appropriate object.</span></span>
- <span data-ttu-id="a648a-163">Hvis et uttrykk for egenskapen **Aktivert** er konfigurert til å returnere **Usann** under kjøring, vil det aktuelle objektet ikke bli fylt ut i det genererte dokumentet.</span><span class="sxs-lookup"><span data-stu-id="a648a-163">If an expression of the **Enabled** property is configured to return **False** at runtime, the appropriate object won't be filled in in the generated document.</span></span>

<span data-ttu-id="a648a-164">Når en **Celle**-komponent er konfigurert til å angi en verdi i en celle, kan den bindes til en datakilde som returnerer verdien av en primitiv datatype (for eksempel **Streng**, **Kommatall** eller **Heltall**).</span><span class="sxs-lookup"><span data-stu-id="a648a-164">When a **Cell** component is configured to enter a value in a cell, it can be bound with a data source that returns the value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="a648a-165">I dette tilfellet angis verdien i cellen som en verdi av den samme datatypen.</span><span class="sxs-lookup"><span data-stu-id="a648a-165">In this case, the value is entered in the cell as a value of the same data type.</span></span>

<span data-ttu-id="a648a-166">Når en **Celle**-komponent er konfigurert til å angi en verdi i en Excel-figur, kan den bindes til en datakilde som returnerer en verdi av en primitiv datatype (for eksempel **Streng**, **Kommatall** eller **Heltall**).</span><span class="sxs-lookup"><span data-stu-id="a648a-166">When a **Cell** component is configured to enter a value in an Excel shape, it can be bound with a data source that returns a value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="a648a-167">I dette tilfellet angis verdien i Excel-figuren som teksten for den figuren.</span><span class="sxs-lookup"><span data-stu-id="a648a-167">In this case, the value is entered in the Excel shape as the text of that shape.</span></span> <span data-ttu-id="a648a-168">For verdier for datatyper som ikke er en **Streng**, utføres konverteringen til tekst automatisk.</span><span class="sxs-lookup"><span data-stu-id="a648a-168">For values of data types that aren't **String**, the conversion to text is done automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="a648a-169">Du kan konfigurere en **Celle**-komponent slik at den bare fyller ut en figur i tilfeller der en figurtekstegenskap støttes.</span><span class="sxs-lookup"><span data-stu-id="a648a-169">You can configure a **Cell** component to fill in a shape only in cases where a shape text property is supported.</span></span>

<span data-ttu-id="a648a-170">Når en **Celle**-komponent er konfigurert til å angi en verdi i et Excel-bilde, kan den bindes til en datakilde som returnerer en verdi for datatypen **Container** som representerer et bilde i binærformat.</span><span class="sxs-lookup"><span data-stu-id="a648a-170">When a **Cell** component is configured to enter a value in an Excel picture, it can be bound with a data source that returns a value of the **Container** data type that represents an image in binary format.</span></span> <span data-ttu-id="a648a-171">I dette tilfellet angis verdien i Excel-bildet som et bilde.</span><span class="sxs-lookup"><span data-stu-id="a648a-171">In this case, the value is entered in the Excel picture as an image.</span></span>

> [!NOTE]
> <span data-ttu-id="a648a-172">Alle Excel-bilder og -figurer anses å være forankret ved øverste venstre hjørne til en bestemt Excel-celle eller -område.</span><span class="sxs-lookup"><span data-stu-id="a648a-172">Every Excel picture and shape is considered to be anchored by its upper-left corner to a specific Excel cell or range.</span></span> <span data-ttu-id="a648a-173">Hvis du vil replikere et Excel-bilde eller -figur, må du konfigurere cellen eller området som den er forankret til, som en replikert celle eller et replikert område.</span><span class="sxs-lookup"><span data-stu-id="a648a-173">If you want to replicate an Excel picture or shape, you must configure the cell or range that it's anchored to as a replicated cell or range.</span></span>

<span data-ttu-id="a648a-174">Hvis du vil finne ut mer om hvordan du bygger inn bilder og figurer, kan du se [Bygge inn bilder og figurer i dokumenter du genererer ved hjelp av ER](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="a648a-174">To learn more about how to embed images and shapes, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="page-break-component"></a><span data-ttu-id="a648a-175">Komponeten Sideskift</span><span class="sxs-lookup"><span data-stu-id="a648a-175">Page break component</span></span>

<span data-ttu-id="a648a-176">Komponenten **PageBreak** tvinger Excel til å starte en ny side.</span><span class="sxs-lookup"><span data-stu-id="a648a-176">The **PageBreak** component forces Excel to start a new page.</span></span> <span data-ttu-id="a648a-177">Denne komponenten er ikke nødvendig når du vil bruke standard sideveksling i Excel, men du bør bruke den når du vil at ER-formatet skal strukturere sideveksling for Excel.</span><span class="sxs-lookup"><span data-stu-id="a648a-177">This component isn't required when you want to use Excel's default paging, but you should use it when you want Excel to follow your ER format to structure paging.</span></span>

## <a name="edit-an-added-er-format"></a><span data-ttu-id="a648a-178">Redigere et tillagt ER-format</span><span class="sxs-lookup"><span data-stu-id="a648a-178">Edit an added ER format</span></span>

### <a name="update-a-template"></a><span data-ttu-id="a648a-179">Oppdatere en mal</span><span class="sxs-lookup"><span data-stu-id="a648a-179">Update a template</span></span>

<span data-ttu-id="a648a-180">Du kan velge **Oppdater fra Excel** i kategorien **Import** i handlingsruten for å importere en oppdatert mal til et redigerbart ER-format.</span><span class="sxs-lookup"><span data-stu-id="a648a-180">You can select **Update from Excel** on the **Import** tab of the Action Pane to import an updated template into an editable ER format.</span></span> <span data-ttu-id="a648a-181">I løpet av denne prosessen vil en mal for den valgte **Excel\\Fil**-komponenten bli erstattet med en ny mal.</span><span class="sxs-lookup"><span data-stu-id="a648a-181">During this process, a template of the selected **Excel\\File** component will be replaced by a new template.</span></span> <span data-ttu-id="a648a-182">Innholdet i det redigerbare ER-formatet vil bli synkronisert med innholdet i den oppdaterte ER-malen.</span><span class="sxs-lookup"><span data-stu-id="a648a-182">The content of the editable ER format will be synced with the content of the updated ER template.</span></span>

- <span data-ttu-id="a648a-183">En ny komponent for ER-format vil automatisk opprettes for hvert Excel-navn hvis komponenten for ER format ikke finnes i det redigerbare formatet.</span><span class="sxs-lookup"><span data-stu-id="a648a-183">A new ER format component will automatically be created for every Excel name if the ER format component isn't found in the editable format.</span></span>
- <span data-ttu-id="a648a-184">Alle komponenter for ER-format vil bli slettet fra det redigerbare ER-formatet hvis det riktige Excel-navnet ikke blir funnet for det.</span><span class="sxs-lookup"><span data-stu-id="a648a-184">Every ER format component will be deleted from the editable ER format if the appropriate Excel name isn't found for it.</span></span>

> [!NOTE]
> <span data-ttu-id="a648a-185">Sett alternativet **Opprett element for Excel-arkformat** til **Ja** hvis du vil opprette det valgfrie **Ark**-elementet i det redigerbare ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="a648a-185">Set the **Create Excel Sheet format element** option to **Yes** if you want to create the optional **Sheet** element in the editable ER format.</span></span>
>
> <span data-ttu-id="a648a-186">Hvis det redigerbare ER-formatet opprinnelig inneholdt **Ark**-elementer, anbefales det at du setter akternativet **Opprett element for Excel-arkformat** til **Ja** når du importerer en oppdatert mal.</span><span class="sxs-lookup"><span data-stu-id="a648a-186">If the editable ER format originally contained **Sheet** elements, we recommend that you set the **Create Excel Sheet format element** option to **Yes** when you import an updated template.</span></span> <span data-ttu-id="a648a-187">Hvis ikke, vil alle nestede elementer i det opprinnelige **Ark**-elementet bli opprettet fra grunnen av.</span><span class="sxs-lookup"><span data-stu-id="a648a-187">Otherwise, all nested elements of the original **Sheet** element will be created from scratch.</span></span> <span data-ttu-id="a648a-188">Alle bindinger av elementene for nyopprettet format vil derfor gå tapt i det oppdaterte ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="a648a-188">Therefore, all bindings of the re-created format elements will be lost in the updated ER format.</span></span>

![Alternativet Opprett element for Excel-arkformat i dialogboksen Oppdater fra Excel](./media/er-excel-format-update-template.png)

<span data-ttu-id="a648a-190">Hvis du vil finne ut mer om denne funksjonen, kan du følge fremgangsmåten i [Endre formater for elektronisk rapportering ved å bruke Excel-maler på nytt](modify-electronic-reporting-format-reapply-excel-template.md).</span><span class="sxs-lookup"><span data-stu-id="a648a-190">To learn more about this feature, follow the steps in [Modify Electronic reporting formats by reapplying Excel templates](modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

## <a name="validate-an-er-format"></a><span data-ttu-id="a648a-191">Validere et ER-format</span><span class="sxs-lookup"><span data-stu-id="a648a-191">Validate an ER format</span></span>

<span data-ttu-id="a648a-192">Når du validerer et ER-format som kan redigeres, utføres det en konsekvenskontroll for å sikre at Excel-navnet finnes i Excel-malen som brukes for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="a648a-192">When you validate an ER format that can be edited, a consistency check is done to make sure that the Excel name is present in the Excel template that is currently used.</span></span> <span data-ttu-id="a648a-193">Du vil bli varslet om eventuelle inkonsekvenser.</span><span class="sxs-lookup"><span data-stu-id="a648a-193">You will be notified about any inconsistencies.</span></span> <span data-ttu-id="a648a-194">For noen inkonsekvenser vil alternativet for automatisk korrigering av problemer bli tilbudt.</span><span class="sxs-lookup"><span data-stu-id="a648a-194">For some inconsistencies, the option to automatically fix issues will be offered.</span></span>

![Valideringsfeilmelding](./media/er-excel-format-validate.png)


## <a name="additional-resources"></a><span data-ttu-id="a648a-196">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a648a-196">Additional resources</span></span>

[<span data-ttu-id="a648a-197">Oversikt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="a648a-197">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="a648a-198">Utforme en konfigurasjon for generering av rapporter i OPENXML-format</span><span class="sxs-lookup"><span data-stu-id="a648a-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks\er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="a648a-199">Endre formater for elektronisk rapportering ved å bruke Excel-maler på nytt</span><span class="sxs-lookup"><span data-stu-id="a648a-199">Modify Electronic reporting formats by reapplying Excel templates</span></span>](modify-electronic-reporting-format-reapply-excel-template.md)

[<span data-ttu-id="a648a-200">Bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk</span><span class="sxs-lookup"><span data-stu-id="a648a-200">Use horizontally expandable ranges to dynamically add columns in Excel reports</span></span>](tasks/er-horizontal-1.md)

[<span data-ttu-id="a648a-201">Bygge inn bilder og figurer i dokumenter du genererer ved hjelp av ER</span><span class="sxs-lookup"><span data-stu-id="a648a-201">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="a648a-202">Konfigurere elektronisk rapportering (ER) for å hente data til Power BI</span><span class="sxs-lookup"><span data-stu-id="a648a-202">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)