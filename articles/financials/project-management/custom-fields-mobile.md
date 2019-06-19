---
title: Implementere egendefinerte felt for Microsoft Dynamics 365 Project Timesheet-mobilappen på IOS og Android
description: Dette emnet inneholder vanlige mønstre for bruk av utvidelser for implementering av egendefinerte felt.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 4343c875da05641c57b7784bf52f1c814dd26d20
ms.sourcegitcommit: 19859d8566a8c7840066b2c10c6b08b67f1b83f4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2019
ms.locfileid: "1618002"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="05e3f-103">Implementere egendefinerte felt for Microsoft Dynamics 365 Project Timesheet-mobilappen på IOS og Android</span><span class="sxs-lookup"><span data-stu-id="05e3f-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05e3f-104">Dette emnet inneholder vanlige mønstre for bruk av utvidelser for implementering av egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="05e3f-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="05e3f-105">Følgende emner dekkes:</span><span class="sxs-lookup"><span data-stu-id="05e3f-105">The following topics are covered:</span></span>

- <span data-ttu-id="05e3f-106">De forskjellige datatypene som det egendefinerte feltrammeverket støtter</span><span class="sxs-lookup"><span data-stu-id="05e3f-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="05e3f-107">Vise skrivebeskyttede eller redigerbare felt i timeregistreringsoppføringer og lagre brukerleverte verdier tilbake til databasen</span><span class="sxs-lookup"><span data-stu-id="05e3f-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="05e3f-108">Vise skrivebeskyttede felt i timeregistreringshodet</span><span class="sxs-lookup"><span data-stu-id="05e3f-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="05e3f-109">Integrere annen egendefinert forretningslogikk for å angi standardverdier i felt og utføre tilleggsvalidering</span><span class="sxs-lookup"><span data-stu-id="05e3f-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="05e3f-110">Målgruppe</span><span class="sxs-lookup"><span data-stu-id="05e3f-110">Audience</span></span>

<span data-ttu-id="05e3f-111">Dette emnet er ment for utviklere som integrerer sine egendefinerte felt i Microsoft Dynamics 365 Project Timesheet-mobilapplikasjonen som er tilgjengelig for Apple iOS og Google Android.</span><span class="sxs-lookup"><span data-stu-id="05e3f-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="05e3f-112">Det antas at leserne er kjent med funksjonene for utvikling og prosjekttimeregistrering i X++.</span><span class="sxs-lookup"><span data-stu-id="05e3f-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="05e3f-113">Datakontrakt – TSTimesheetCustomField X++-klasse</span><span class="sxs-lookup"><span data-stu-id="05e3f-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="05e3f-114">Klassen **TSTimesheetCustomField** er X++-datakontraktklassen som representerer informasjon om et egendefinert felt for timeregistreringsfunksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="05e3f-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="05e3f-115">Det blir sendt lister over de egendefinerte feltobjektene både på TSTimesheetDetails-datakontrakten og TSTimesheetEntry-datakontrakten for å vise egendefinerte felt i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="05e3f-116">**TSTimesheetDetails** – timeregistreringshodekontrakten.</span><span class="sxs-lookup"><span data-stu-id="05e3f-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="05e3f-117">**TSTimesheetEntry** – kontrakten for timeregistreringstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="05e3f-118">Grupper av disse objektene som har samme prosjektinformasjon og **timesheetLineRecId**-verdi, utgjør en linje.</span><span class="sxs-lookup"><span data-stu-id="05e3f-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="05e3f-119">fieldBaseType (typer)</span><span class="sxs-lookup"><span data-stu-id="05e3f-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="05e3f-120">Egenskapen **FieldBaseType** i **TsTimesheetCustom**-objektet bestemmer typen av feltet som vises i appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="05e3f-121">Følgende **Typer**-verdier som støttes.</span><span class="sxs-lookup"><span data-stu-id="05e3f-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="05e3f-122">Typer-verdi</span><span class="sxs-lookup"><span data-stu-id="05e3f-122">Types value</span></span> | <span data-ttu-id="05e3f-123">Type</span><span class="sxs-lookup"><span data-stu-id="05e3f-123">Type</span></span>              | <span data-ttu-id="05e3f-124">Notater</span><span class="sxs-lookup"><span data-stu-id="05e3f-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="05e3f-125">0</span><span class="sxs-lookup"><span data-stu-id="05e3f-125">0</span></span>           | <span data-ttu-id="05e3f-126">Streng (og Opplisting)</span><span class="sxs-lookup"><span data-stu-id="05e3f-126">String (and Enum)</span></span> | <span data-ttu-id="05e3f-127">Feltet vises som et tekstfelt.</span><span class="sxs-lookup"><span data-stu-id="05e3f-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="05e3f-128">1</span><span class="sxs-lookup"><span data-stu-id="05e3f-128">1</span></span>           | <span data-ttu-id="05e3f-129">Heltall</span><span class="sxs-lookup"><span data-stu-id="05e3f-129">Integer</span></span>           | <span data-ttu-id="05e3f-130">Verdien vises som et tall uten desimaler.</span><span class="sxs-lookup"><span data-stu-id="05e3f-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="05e3f-131">2</span><span class="sxs-lookup"><span data-stu-id="05e3f-131">2</span></span>           | <span data-ttu-id="05e3f-132">Kommatall</span><span class="sxs-lookup"><span data-stu-id="05e3f-132">Real</span></span>              | <span data-ttu-id="05e3f-133">Verdien vises som et tall med desimaler.</span><span class="sxs-lookup"><span data-stu-id="05e3f-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="05e3f-134">Hvis du vil vise den reelle verdien som en valuta i appen, bruker du **fieldExtenededType**-egenskapen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="05e3f-135">Du kan bruke egenskapen **numberOfDecimals** til å angi antall desimaler som vises.</span><span class="sxs-lookup"><span data-stu-id="05e3f-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="05e3f-136">3</span><span class="sxs-lookup"><span data-stu-id="05e3f-136">3</span></span>           | <span data-ttu-id="05e3f-137">Dato</span><span class="sxs-lookup"><span data-stu-id="05e3f-137">Date</span></span>              | <span data-ttu-id="05e3f-138">Datoformater bestemmes av brukerens innstilling for **Dato, klokkeslett og nummerformat**, som er angitt under **Innstillinger for språk og land/område** i **Brukeralternativer**.</span><span class="sxs-lookup"><span data-stu-id="05e3f-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="05e3f-139">4</span><span class="sxs-lookup"><span data-stu-id="05e3f-139">4</span></span>           | <span data-ttu-id="05e3f-140">Boolsk</span><span class="sxs-lookup"><span data-stu-id="05e3f-140">Boolean</span></span>           | |
| <span data-ttu-id="05e3f-141">15</span><span class="sxs-lookup"><span data-stu-id="05e3f-141">15</span></span>          | <span data-ttu-id="05e3f-142">GUID</span><span class="sxs-lookup"><span data-stu-id="05e3f-142">GUID</span></span>              | |
| <span data-ttu-id="05e3f-143">16</span><span class="sxs-lookup"><span data-stu-id="05e3f-143">16</span></span>          | <span data-ttu-id="05e3f-144">Int64</span><span class="sxs-lookup"><span data-stu-id="05e3f-144">Int64</span></span>             | |

- <span data-ttu-id="05e3f-145">Hvis egenskapen **stringOptions** ikke er angitt på **TSTimesheetCustomField**-objektet, gis det et fritekstfelt til brukeren.</span><span class="sxs-lookup"><span data-stu-id="05e3f-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="05e3f-146">Egenskapen **stringLength** kan brukes til å angi den maksimale strenglengden som brukere kan angi.</span><span class="sxs-lookup"><span data-stu-id="05e3f-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="05e3f-147">Hvis egenskapen **stringOptions** er angitt på **TSTimesheetCustomField**-objektet, er disse listeelementene de eneste verdiene brukerne kan velge ved å bruke alternativknappene (valgknapper).</span><span class="sxs-lookup"><span data-stu-id="05e3f-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="05e3f-148">I dette tilfellet kan strengfeltet fungere som en opplistingsverdi for brukeroppføring.</span><span class="sxs-lookup"><span data-stu-id="05e3f-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="05e3f-149">Hvis du vil lagre verdien i databasen som en opplisting, kan du manuelt tilordne strengverdien tilbake til opplistingsverdien før du lagrer databasen ved hjelp av kommandokjeden (se delen "Bruke kommandokjede på klassen TSTimesheetEntryService for å lagre en timeregistreringsoppføring fra appen tilbake til databasen" senere i dette emnet for å se et eksempel).</span><span class="sxs-lookup"><span data-stu-id="05e3f-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="05e3f-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="05e3f-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="05e3f-151">Du kan bruke denne egenskapen til å formatere reelle verdier som valuta.</span><span class="sxs-lookup"><span data-stu-id="05e3f-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="05e3f-152">Denne fremgangsmåten gjelder bare når **fieldBaseType**-verdien er **Kommatall**.</span><span class="sxs-lookup"><span data-stu-id="05e3f-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="05e3f-153">**TSCustomFieldExtendedType:None** – Ingen formatering brukes.</span><span class="sxs-lookup"><span data-stu-id="05e3f-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="05e3f-154">**TSCustomFieldExtendedType::Currency** – Formaterer verdien som valuta.</span><span class="sxs-lookup"><span data-stu-id="05e3f-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="05e3f-155">Når valutaformatering er aktiv, kan **stringValue**-feltet brukes til å sende valutakoden som skal vises i appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="05e3f-156">Verdien er en skrivebeskyttet verdi.</span><span class="sxs-lookup"><span data-stu-id="05e3f-156">The value is a read-only value.</span></span>

    <span data-ttu-id="05e3f-157">Feltet **realValue** inneholder pengebeløpet som skal lagres i databasen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="05e3f-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="05e3f-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="05e3f-159">Du kan bruke denne egenskapen til å angi hvor det egendefinerte feltet skal vises i appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="05e3f-160">**TSCustomFieldSection::Header** – Feltet vises i **Vis flere detaljer**-delen i appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="05e3f-161">Begge feltene er alltid skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="05e3f-161">These fields are always read-only.</span></span>
- <span data-ttu-id="05e3f-162">**TSCustomFieldSection::Line** – Feltet vil vises etter alle medfølgende linjefelt på timeregistreringsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="05e3f-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="05e3f-163">Disse feltene kan enten være redigerbare eller skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="05e3f-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="05e3f-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="05e3f-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="05e3f-165">Denne egenskapen identifiserer feltet når verdiene som appen gir, lagres tilbake til databasen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="05e3f-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="05e3f-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="05e3f-167">Denne egenskapen identifiserer feltet når verdiene som appen gir, lagres tilbake til databasen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="05e3f-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="05e3f-168">isEditable (NoYes)</span></span>

<span data-ttu-id="05e3f-169">Sett denne egenskapen til **Ja** for å angi at feltet i timeregistreringsdelen skal være redigerbar av brukere.</span><span class="sxs-lookup"><span data-stu-id="05e3f-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="05e3f-170">Sett egenskapen til **Nei** for å skrivebeskytte feltet.</span><span class="sxs-lookup"><span data-stu-id="05e3f-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="05e3f-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="05e3f-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="05e3f-172">Sett denne egenskapen til **Ja** for å angi at feltet i timeregistreringsdelen skal være obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="05e3f-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="05e3f-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="05e3f-173">label (str)</span></span>

<span data-ttu-id="05e3f-174">Denne egenskapen angir etiketten som vises ved siden av feltet i appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="05e3f-175">stringOptions (List of Strings)</span><span class="sxs-lookup"><span data-stu-id="05e3f-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="05e3f-176">Denne egenskapen gjelder bare når **fieldBaseType** er satt til **Streng**.</span><span class="sxs-lookup"><span data-stu-id="05e3f-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="05e3f-177">Hvis **stringOptions** er angitt, angis strengverdiene som er tilgjengelige for valg via alternativknapper (valgknapper), av strengene i listen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="05e3f-178">Hvis ingen strenger angis, tillates fritekstregistrering i strengfeltet (se delen "Bruke kommandokjede på klassen TSTimesheetEntryService for å lagre en timeregistreringsoppføring fra appen tilbake til databasen" senere i dette emnet for et eksempel).</span><span class="sxs-lookup"><span data-stu-id="05e3f-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="05e3f-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="05e3f-179">stringLength (int)</span></span>

<span data-ttu-id="05e3f-180">Denne egenskapen angir den maksimale lengden for et strengfelt.</span><span class="sxs-lookup"><span data-stu-id="05e3f-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="05e3f-181">Den gjelder bare når **fieldBaseType** er satt til **Streng**.</span><span class="sxs-lookup"><span data-stu-id="05e3f-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="05e3f-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="05e3f-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="05e3f-183">Denne egenskapen angir antall desimaler som vises for et reelt felt.</span><span class="sxs-lookup"><span data-stu-id="05e3f-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="05e3f-184">Den gjelder bare når **fieldBaseType** er satt til **Kommatall**.</span><span class="sxs-lookup"><span data-stu-id="05e3f-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="05e3f-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="05e3f-185">orderSequence (int)</span></span>

<span data-ttu-id="05e3f-186">Denne egenskapen kontrollerer i hvilken rekkefølge de egendefinerte feltene vises i appen når mer enn ett egendefinert felt er angitt.</span><span class="sxs-lookup"><span data-stu-id="05e3f-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="05e3f-187">Felt som har lavere tall, vises først.</span><span class="sxs-lookup"><span data-stu-id="05e3f-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="05e3f-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="05e3f-188">booleanValue (boolean)</span></span>

<span data-ttu-id="05e3f-189">For felt av typen **Boolsk** sender denne egenskapen den boolske verdien for feltet mellom serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="05e3f-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="05e3f-190">guidValue (guid)</span></span>

<span data-ttu-id="05e3f-191">For felt av typen **GUID** sender denne egenskapen den globalt unike identifikatoren (GUID) for feltet mellom serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="05e3f-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="05e3f-192">int64Value (int64)</span></span>

<span data-ttu-id="05e3f-193">For felt av typen **Int64** sender denne egenskapen int64-verdien for feltet mellom serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="05e3f-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="05e3f-194">intValue (int)</span></span>

<span data-ttu-id="05e3f-195">For felt av typen **Int** sender denne egenskapen int-verdien for feltet mellom serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="05e3f-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="05e3f-196">realValue (real)</span></span>

<span data-ttu-id="05e3f-197">For felt av typen **Kommatall** sender denne egenskapen kommatallverdien for feltet mellom serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="05e3f-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="05e3f-198">stringValue (str)</span></span>

<span data-ttu-id="05e3f-199">For felt av typen **Streng** sender denne egenskapen strengverdien for feltet mellom serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="05e3f-200">Det brukes også for felt av typen **Kommatall** som formateres som valuta.</span><span class="sxs-lookup"><span data-stu-id="05e3f-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="05e3f-201">For disse feltene brukes egenskapen til å sende valutakoden til appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="05e3f-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="05e3f-202">dateValue (date)</span></span>

<span data-ttu-id="05e3f-203">For felt av typen **Dato** sender denne egenskapen datoverdien for feltet mellom serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="05e3f-204">Vise og lagre et egendefinert felt i timeregistreringsdelen</span><span class="sxs-lookup"><span data-stu-id="05e3f-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="05e3f-205">Nedenfor vises et skjermbilde fra mobilappen for en timeregistreringsoppretting.</span><span class="sxs-lookup"><span data-stu-id="05e3f-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="05e3f-206">Den viser medfølgende felt og et egendefinert felt i delen "Tidsoppføring" som kalles "Teststreng" med opplistingsverdien "andre alternativ" som allerede er angitt.</span><span class="sxs-lookup"><span data-stu-id="05e3f-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Egendefinert felt for teststreng i appen](media/timesheet-entry.jpg)



<span data-ttu-id="05e3f-208">Nedenfor vises et skjermbilde fra mobilappen til brukeren som velger et av opplistingsalternativene som er tilgjengelig for det egendefinerte feltet "Teststreng".</span><span class="sxs-lookup"><span data-stu-id="05e3f-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="05e3f-209">De to alternativene er "Første alternativ" og "Andre alternativ", som vises som alternativknapper.</span><span class="sxs-lookup"><span data-stu-id="05e3f-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="05e3f-210">Det andre alternativet er allerede valgt.</span><span class="sxs-lookup"><span data-stu-id="05e3f-210">The second option is currently selected.</span></span>

![Alternativknapper (valgknapper) for det egendefinerte feltet Teststreng](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="05e3f-212">Utvid TSTimesheetLine-tabellen, slik at den har et egendefinert felt</span><span class="sxs-lookup"><span data-stu-id="05e3f-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="05e3f-213">I vanlige scenarioer er det sannsynlig at dataene for et egendefinert felt i delen timeregistreringsoppføring blir lagret i TSTimesheetLine-tabellen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="05e3f-214">Det kan imidlertid brukes andre tabeller hvis dataene kan hentes basert på en TSTimesheetTrans-post som oppgis, eller hvis det ikke finnes en bestemt postkontekst (hvis for eksempel feltet er angitt som skrivebeskyttet i prosjektparameterne).</span><span class="sxs-lookup"><span data-stu-id="05e3f-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="05e3f-215">Legg merke til at egendefinerte felt ikke trenger å ha noen reservedatabaseposter.</span><span class="sxs-lookup"><span data-stu-id="05e3f-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="05e3f-216">De kan genereres dynamisk basert på X++-logikk.</span><span class="sxs-lookup"><span data-stu-id="05e3f-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="05e3f-217">Denne fremgangsmåten kan være nyttig i skrivebeskyttede scenarioer (se delen "Bruke kommandokjede på klassen TSTimesheetDetails, metoden buildCustomFieldListForHeader for å fylle ut timeregistreringsdetaljer" for et eksempel på dynamisk genererte egendefinerte feltverdier.)</span><span class="sxs-lookup"><span data-stu-id="05e3f-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="05e3f-218">Nedenfor vises et skjermbilde fra Visual Studio i applikasjonsobjekttreet.</span><span class="sxs-lookup"><span data-stu-id="05e3f-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="05e3f-219">Det viser en utvidelse av TSTimesheetLine-tabellen med TestLineString-feltet lagt til som et egendefinert felt.</span><span class="sxs-lookup"><span data-stu-id="05e3f-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Linjestreng](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="05e3f-221">Bruk kommandokjede på buildCustomFieldList-metoden til TSTimesheetSettings-klassen for å vise et felt i delen timeregistreringsoppføring</span><span class="sxs-lookup"><span data-stu-id="05e3f-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="05e3f-222">Denne koden kontrollerer visningsinnstillingene for feltet i appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="05e3f-223">Det kontrollerer for eksempel felttypen, etiketten, om feltet er obligatorisk, og hvilken inndeling feltet vises i.</span><span class="sxs-lookup"><span data-stu-id="05e3f-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="05e3f-224">Følgende eksempel viser et strengfelt på tidsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="05e3f-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="05e3f-225">Dette feltet har to alternativer, **Første alternativ** og **Andre alternativ**, som er tilgjengelige via alternativknapper (valgknapper).</span><span class="sxs-lookup"><span data-stu-id="05e3f-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="05e3f-226">Feltet i appen er knyttet til **TestLineString**-feltet som legges til i TSTimesheetLine-tabellen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="05e3f-227">Legg merke til bruken av **TSTimesheetCustomField::newFromMetatdata()**-metoden for å forenkle initialiseringen av de egendefinerte feltegenskapene: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** og **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="05e3f-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="05e3f-228">Du kan også angi disse parameterne manuelt slik du vil.</span><span class="sxs-lookup"><span data-stu-id="05e3f-228">You can also set these parameters manually, as you prefer.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="05e3f-229">Bruke kommandokjede på buildCustomFieldListForEntry-metoden til TSTimesheetEntry-klassen for å angi verdier i en timeregistreringsoppføring</span><span class="sxs-lookup"><span data-stu-id="05e3f-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="05e3f-230">Metoden **buildCustomFieldListForEntry** brukes til å angi verdier på de lagrede timeregistreringslinjene i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="05e3f-231">Den bruker en TSTimesheetTrans-post som en parameter.</span><span class="sxs-lookup"><span data-stu-id="05e3f-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="05e3f-232">Felt fra denne posten kan brukes til å fylle ut den egendefinerte feltverdien i appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="05e3f-233">Bruk kommandokjeden på TSTimesheetEntryService-klassen til å lagre en timeregistreringsoppføring fra appen tilbake til databasen</span><span class="sxs-lookup"><span data-stu-id="05e3f-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="05e3f-234">Hvis du vil lagre et egendefinert felt tilbake til databasen i vanlig bruk, må du utvide flere metoder:</span><span class="sxs-lookup"><span data-stu-id="05e3f-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="05e3f-235">Metoden **timesheetLineNeedsUpdating** brukes til å fastsette om linjeposten er endret av brukeren i appen og må lagres til databasen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="05e3f-236">Hvis ytelse ikke er av betydning, kan denne metoden forenkles, slik at den alltid returnerer **sann**.</span><span class="sxs-lookup"><span data-stu-id="05e3f-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="05e3f-237">Metodene **populateTimesheetLineFromEntryDuringCreate** og **populateTimesheetLineFromEntryDuringUpdate** kan utvides, slik at de angir verdier i TSTimesheetLine-databaseposten fra TSTimesheetEntry-datakontraktposten som er angitt.</span><span class="sxs-lookup"><span data-stu-id="05e3f-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="05e3f-238">I eksemplet nedenfor ser du hvordan tilordningen mellom databasefeltet og oppføringsfeltet utføres manuelt via via X++-kode.</span><span class="sxs-lookup"><span data-stu-id="05e3f-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="05e3f-239">Metoden **populateTimesheetWeekFromEntry** kan også utvides hvis det egendefinerte feltet som er tilordnet **TSTimesheetEntry**-objektet, må skrive tilbake til TSTimesheetLineweek-databasetabellen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="05e3f-240">Det følgende eksemplet lagrer verdien **firstOption** eller **secondOption** som brukeren velger, i databasen som en rå-strengverdi.</span><span class="sxs-lookup"><span data-stu-id="05e3f-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="05e3f-241">Hvis databasefeltet er et felt av typen **Opplisting**, kan disse verdiene tilordnes til en opplistingsverdi manuelt og deretter lagres til et opplistingsfelt i databasetabellen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="05e3f-242">Vise et egendefinert felt i topptekstdelen for timeregistrering</span><span class="sxs-lookup"><span data-stu-id="05e3f-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="05e3f-243">Nedenfor vises et skjermbilde fra mobilappen til en bruker som viser en timeregistrering.</span><span class="sxs-lookup"><span data-stu-id="05e3f-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="05e3f-244">Knappen "Mer informasjon" er valgt i øvre høyre hjørne for å vise alternativet "Vis flere detaljer".</span><span class="sxs-lookup"><span data-stu-id="05e3f-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Vis flere detaljer-kommando](media/show-more.png)



<span data-ttu-id="05e3f-246">Nedenfor vises et skjermbilde fra mobilappen som viser "Mer"-delen av en timeregistrering.</span><span class="sxs-lookup"><span data-stu-id="05e3f-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="05e3f-247">Et egendefinert felt kalt "Utnyttelsesrate for denne timeregistreringen (beregnet egendefinert felt)" er lagt til i topptekstdelen for timeregistrering.</span><span class="sxs-lookup"><span data-stu-id="05e3f-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="05e3f-248">En skrivebeskyttet verdi på "0,667" angis for det egendefinerte feltet.</span><span class="sxs-lookup"><span data-stu-id="05e3f-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Mer-del](media/more-section.jpg)



### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="05e3f-250">Utvid TSTimesheetTable-tabellen, slik at den har et egendefinert felt</span><span class="sxs-lookup"><span data-stu-id="05e3f-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="05e3f-251">I vanlige scenarioer er det sannsynlig at dataene for et egendefinert felt i topptekstdelen hentes fra TSTimesheetHeader-tabellen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="05e3f-252">Det kan imidlertid brukes andre tabeller hvis dataene kan hentes basert på en TSTimesheetTable-post som oppgis, eller hvis det ikke finnes en bestemt postkontekst (hvis for eksempel feltet er angitt som skrivebeskyttet i prosjektparameterne).</span><span class="sxs-lookup"><span data-stu-id="05e3f-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="05e3f-253">Legg merke til at egendefinerte felt ikke trenger å ha noen reservedatabaseposter.</span><span class="sxs-lookup"><span data-stu-id="05e3f-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="05e3f-254">De kan genereres dynamisk basert på X++-logikk.</span><span class="sxs-lookup"><span data-stu-id="05e3f-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="05e3f-255">Eksemplet nedenfor viser denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="05e3f-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="05e3f-256">Felt i topptekstinndelingen er alltid skrivebeskyttet i appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="05e3f-257">Bruke kommandokjede på buildCustomFieldList-metoden til TSTimesheetSettings-klassen for å vise et felt i topptekstdelen</span><span class="sxs-lookup"><span data-stu-id="05e3f-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="05e3f-258">Denne koden kontrollerer visningsinnstillingene for feltet i appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="05e3f-259">Det kontrollerer for eksempel felttypen, etiketten, om feltet er obligatorisk, og hvilken inndeling feltet vises i.</span><span class="sxs-lookup"><span data-stu-id="05e3f-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="05e3f-260">Følgende eksempel viser en beregnet verdi i hodedelen i appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-260">The following example shows a computed value in the header section in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="05e3f-261">Bruke kommandokjede på buildCustomFieldListForHeader-metoden til TSTimesheetDetails-klassen for å fylle ut timeregistreringsdetaljer</span><span class="sxs-lookup"><span data-stu-id="05e3f-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="05e3f-262">Metoden **buildCustomFieldListForHeader** brukes til å fylle ut timeregistreringshodedetaljene i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="05e3f-263">Den bruker en TSTimesheetTable-post som en parameter.</span><span class="sxs-lookup"><span data-stu-id="05e3f-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="05e3f-264">Felt fra denne posten kan brukes til å fylle ut den egendefinerte feltverdien i appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="05e3f-265">Følgende eksempel leser ikke verdier fra databasen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="05e3f-266">I stedet brukes X++-logikk til å generere en beregnet verdi som deretter vises i appen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="05e3f-267">Andre muligheter for konfigurerbarhet/utvidelse</span><span class="sxs-lookup"><span data-stu-id="05e3f-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="05e3f-268">Legge til ekstra validering for appen</span><span class="sxs-lookup"><span data-stu-id="05e3f-268">Adding additional validation for the app</span></span>

<span data-ttu-id="05e3f-269">Eksisterende logikk for timeregistreringsfunksjonalitet på databasenivå vil fremdeles fungere som forventet.</span><span class="sxs-lookup"><span data-stu-id="05e3f-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="05e3f-270">Hvis du vil avbryte fullføringen av lagre- eller send-operasjoner og vise en bestemt feilmelding, kan du legge til **iverksett feil("melding til bruker")** i koden via en kommandokjedeutvidelse.</span><span class="sxs-lookup"><span data-stu-id="05e3f-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="05e3f-271">Her er tre eksempler på nyttige utvidelsesmetoder:</span><span class="sxs-lookup"><span data-stu-id="05e3f-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="05e3f-272">Hvis **validateWrite** i TSTimesheetLine-tabellen returnerer **usann** under en lagringsoperasjon for en timeregistreringslinje, vises en feilmelding i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="05e3f-273">Hvis **validateSubmit** i TSTimesheetTable-tabellen returnerer **usann** under innsending av timeregistrering i appen, vises en feilmelding for brukeren.</span><span class="sxs-lookup"><span data-stu-id="05e3f-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="05e3f-274">Logikk som fyller ut felt (for eksempel **Linjeegenskap**) under **sett inn**-metoden i TSTimesheetLine-tabellen, vil fortsatt kjøre.</span><span class="sxs-lookup"><span data-stu-id="05e3f-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="05e3f-275">Skjule og merke medfølgende felt som skrivebeskyttet via konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="05e3f-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="05e3f-276">Fra prosjektparameterne kan du gjøre medfølgende felt skrivebeskyttet eller skjult i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="05e3f-277">Angi alternativene i delen **Mobile timeregistreringer** i kategorien **Timeregistrering** på siden **Parametere for prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="05e3f-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Prosjektparametere](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="05e3f-279">Endre aktivitetene som er tilgjengelige for valg via utvidelser</span><span class="sxs-lookup"><span data-stu-id="05e3f-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="05e3f-280">Aktivitetene som er tilgjengelige for valg for et prosjekt, fylles ut via metodene **getActivitiesForProject()** og **getActivityQuery()** i **TsTimesheetProjectService**-klassen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="05e3f-281">Du kan bruke kommandokjeden til å endre denne virkemåten, slik at den samsvarer med forretningsscenarioet for aktivitetene som er tilgjengelige for valg for et bestemt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="05e3f-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="05e3f-282">Angi en standard prosjektkategori for timeregistreringsoppføringer</span><span class="sxs-lookup"><span data-stu-id="05e3f-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="05e3f-283">Registrering av en standard prosjektkategori i timeregistreringsoppføringer forekommer på tre nivåer.</span><span class="sxs-lookup"><span data-stu-id="05e3f-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="05e3f-284">Du kan bruke kommandokjeden til å utvide virkemåten på hvilke som helst eller alle disse nivåene for å oppnå den ønskede atferden.</span><span class="sxs-lookup"><span data-stu-id="05e3f-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="05e3f-285">Følgende hierarki brukes:</span><span class="sxs-lookup"><span data-stu-id="05e3f-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="05e3f-286">Appen prøver å plassere standardkategori fra prosjektressursen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="05e3f-287">Denne standardkategorien er angitt i metodene **getCurrentUserResource** og **getDelegatedResourcesForCurrentUser** i **TSTimesheetSettingsService**-klassen.</span><span class="sxs-lookup"><span data-stu-id="05e3f-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="05e3f-288">Hvis standardkategorien ikke er angitt på prosjektressursnivå, prøver appen å hente den fra prosjektaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="05e3f-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="05e3f-289">Denne standardkategorien angis i metoden **getActivitiesForProject** i klassen **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="05e3f-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="05e3f-290">Hvis standardkategorien ikke er angitt på prosjektaktivitetsnivå, hentes standardkategorien fra prosjektparametrene.</span><span class="sxs-lookup"><span data-stu-id="05e3f-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="05e3f-291">Denne standardkategorien angis i metoden **getProjectDetailsbyRule** i klassen **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="05e3f-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
