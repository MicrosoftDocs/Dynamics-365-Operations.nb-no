---
title: Opprette og arbeide med egendefinerte felt
description: Dette emnet forklarer hvordan du oppretter egendefinerte felt via brukergrensesnittet for å tilpasse programmet slik at det passer for bedriften.
author: jasongre
ms.date: 05/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: b15b25ac172e8ab942e950c9e8c4aff1e26c9291
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193861"
---
# <a name="create-and-work-with-custom-fields"></a><span data-ttu-id="9b05b-103">Opprette og arbeide med egendefinerte felt</span><span class="sxs-lookup"><span data-stu-id="9b05b-103">Create and work with custom fields</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b05b-104">Selv om det er et omfattende sett med felt som standard for å administrere mange forretningsprosesser, har et firma noen ganger behov for å spore ytterligere informasjon i systemet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-104">While there is an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="9b05b-105">Selv om programmerere kan brukes til å legge til disse feltene som utvidelser i utviklerverktøy, gjør funksjonen egendefinerte felt det mulig å legge til felt direkte fra brukergrensesnittet, slik at du kan skreddersy programmet slik at det passer til bedriften din ved hjelp av Webleseren.</span><span class="sxs-lookup"><span data-stu-id="9b05b-105">While programmers can be used to add those fields as extensions in the developer tools, the custom fields feature allows fields to be added directly from the user interface, thereby allowing you to tailor the application to fit your business using your web browser.</span></span>

<span data-ttu-id="9b05b-106">*Bare brukere med spesialtilgang har tilgang til denne funksjonen.*</span><span class="sxs-lookup"><span data-stu-id="9b05b-106">*Only users with special permissions have access to this feature.*</span></span>

<span data-ttu-id="9b05b-107">Denne videoen viser hvor enkelt det er å legge til et egendefinert felt på en side: [Legge til egendefinerte felt](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span><span class="sxs-lookup"><span data-stu-id="9b05b-107">This video shows how easy it is to add a custom field to a page: [Adding custom fields](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span></span>

## <a name="creating-custom-fields"></a><span data-ttu-id="9b05b-108">Opprette egendefinerte felt</span><span class="sxs-lookup"><span data-stu-id="9b05b-108">Creating custom fields</span></span>

<span data-ttu-id="9b05b-109">Når du har identifisert tilleggsinformasjon du vil spore i programmet, kan du opprette det egendefinerte feltet i den aktuelle tabellen og vise det nye feltet på en side.</span><span class="sxs-lookup"><span data-stu-id="9b05b-109">After you've identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>

<span data-ttu-id="9b05b-110">Trinnene nedenfor beskriver prosessen for å opprette et egendefinert felt og plassere dette feltet i et skjema.</span><span class="sxs-lookup"><span data-stu-id="9b05b-110">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>

1. <span data-ttu-id="9b05b-111">Naviger til skjemaet der det er behov for det nye feltet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-111">Navigate to the form where the new field is needed.</span></span>
2. <span data-ttu-id="9b05b-112">Fordi sluttmålet er å vise det egendefinerte feltet i et skjema, finnes inngangspunktet for å opprette egendefinerte felt i tilpassingsopplevelsen.</span><span class="sxs-lookup"><span data-stu-id="9b05b-112">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="9b05b-113">Åpne tilpassingsverktøylinjen ved å velge **Alternativer** og deretter **Tilpass dette skjemaet**.</span><span class="sxs-lookup"><span data-stu-id="9b05b-113">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span>
3. <span data-ttu-id="9b05b-114">Klikk på **Sett inn** og deretter **Felt**.</span><span class="sxs-lookup"><span data-stu-id="9b05b-114">Click **Insert** and then **Field**.</span></span>
4. <span data-ttu-id="9b05b-115">Velg området i skjemaet der du vil vise det nye feltet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-115">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="9b05b-116">Når du har valgt det, viser **Sett inn felt**-dialogboksen en liste over eksisterende felt som kan settes inn i det merkede området i skjemaet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-116">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>
5. <span data-ttu-id="9b05b-117">Kontroller at feltet du er interessert i, ikke allerede finnes i listen.</span><span class="sxs-lookup"><span data-stu-id="9b05b-117">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="9b05b-118">Hvis det finnes, kan du ganske enkelt velge feltet i listen og klikke **Sett inn**.</span><span class="sxs-lookup"><span data-stu-id="9b05b-118">If it does, you can simply select that field in the list and click **Insert**.</span></span>
6. <span data-ttu-id="9b05b-119">Klikk på **Opprett nytt felt**-knappen over listen for å starte prosessen med å lage et egendefinert felt.</span><span class="sxs-lookup"><span data-stu-id="9b05b-119">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="9b05b-120">Dette åpner **Opprett nytt felt**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="9b05b-120">This will open the **Create new field** dialog box.</span></span>

    <span data-ttu-id="9b05b-121">Hvis du ikke ser **Opprett nytt felt**-knappen, har du ikke de nødvendige tillatelsene til å bruke denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="9b05b-121">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>

7. <span data-ttu-id="9b05b-122">Angi følgende informasjon i dialogboksen **Opprett nytt felt**.</span><span class="sxs-lookup"><span data-stu-id="9b05b-122">In the **Create new field** dialog box, enter the following information.</span></span>
   
    1. <span data-ttu-id="9b05b-123">Velg databasetabellen der dette feltet skal legges til.</span><span class="sxs-lookup"><span data-stu-id="9b05b-123">Select the database table where this field should be added.</span></span> <span data-ttu-id="9b05b-124">Legg merke til at bare tabeller som støtter egendefinerte felt, vises i fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="9b05b-124">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="9b05b-125">Se delen nedenfor for tekniske detaljer om støttede tabeller.</span><span class="sxs-lookup"><span data-stu-id="9b05b-125">See the section below for technical details on supported tables.</span></span>

    2. <span data-ttu-id="9b05b-126">Velg datatypen for det nye feltet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-126">Select the data type for the new field.</span></span> <span data-ttu-id="9b05b-127">Tilgjengelige datatyper er avmerkingsboks, dato, dato/klokkeslett, desimal, tall, plukkliste og tekst.</span><span class="sxs-lookup"><span data-stu-id="9b05b-127">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>

        - <span data-ttu-id="9b05b-128">Hvis du velger datatypen tekst, kan du også angi den maksimale lengden på teksten som kan angis i dette feltet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-128">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span>
        - <span data-ttu-id="9b05b-129">Hvis du velger datatypen plukkliste, kan du også velge settet med gyldige verdier for feltet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-129">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>

    3. <span data-ttu-id="9b05b-130">Angi navn, etikett, og hjelpetekst for feltet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-130">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="9b05b-131">Navnet tilsvarer det fysiske feltnavnet i databasen, mens etikett- og hjelpeteksten er teksten som brukes til å representere dette feltet i brukergrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-131">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>

8. <span data-ttu-id="9b05b-132">Hvis dette er det eneste feltet du vil opprette for dette skjemaet, klikker du **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9b05b-132">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="9b05b-133">Hvis du vil opprette flere felt, klikker du **Lagre og ny** og går tilbake til trinn 7.</span><span class="sxs-lookup"><span data-stu-id="9b05b-133">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="9b05b-134">Legg merke til at det er en grense på **20 egendefinerte felt per tabell**.</span><span class="sxs-lookup"><span data-stu-id="9b05b-134">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9. <span data-ttu-id="9b05b-135">Når du avslutter **Opprett nytt felt**-dialogboksen, kommer du tilbake til **Sett inn felt**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="9b05b-135">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="9b05b-136">Egendefinerte felt som nettopp ble lagt til, merkes automatisk i feltlisten til å bli satt inn i skjemaet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-136">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>
10. <span data-ttu-id="9b05b-137">Klikk på **Sett inn** for å sette inn de merkede feltene i det valgte området i skjemaet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-137">Click **Insert** to insert the marked fields into the selected region of the form.</span></span>
11. <span data-ttu-id="9b05b-138">**Valgfritt:** Aktiver **Flytt**-modus fra tilpassingsverktøylinjen for å flytte de nye feltene til ønsket plassering i det valgte området.</span><span class="sxs-lookup"><span data-stu-id="9b05b-138">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="9b05b-139">Se [Tilpasse brukeropplevelsen](personalize-user-experience.md) for mer informasjon om hvordan du bruker de ulike tilpassingsfunksjonene for å optimalisere et skjema for din personlige bruk.</span><span class="sxs-lookup"><span data-stu-id="9b05b-139">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>

> [!WARNING]
> <span data-ttu-id="9b05b-140">Muligheten til å angi verdier i et egendefinert felt som legges til en side, er avhengig av om tabellen som er knyttet til det egendefinerte feltet, kan redigeres eller være skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-140">The ability to enter values in a custom field added to a page is dependent on whether the table associated with the custom field is editable or read only.</span></span> <span data-ttu-id="9b05b-141">Når den tilknyttede tabellen er skrivebeskyttet, blir også alle felt som er koblet til denne tabellen, inkludert eventuelle egendefinerte felt, skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-141">When the associated table is read only, all fields linked to that table, including any custom fields, will also be read only.</span></span>


## <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="9b05b-142">Dele egendefinerte felt med andre brukere</span><span class="sxs-lookup"><span data-stu-id="9b05b-142">Sharing custom fields with other users</span></span>

<span data-ttu-id="9b05b-143">Når du har opprettet et egendefinert felt og vist det på en side, kan det hende at du vil gi denne oppdaterte sidevisningen som inneholder det nye feltet, til andre brukere i systemet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-143">After you have created a custom field and exposed it on a page, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="9b05b-144">Dette kan gjøres på to forskjellige måter ved hjelp av tilpassingsfunksjonene i produktet:</span><span class="sxs-lookup"><span data-stu-id="9b05b-144">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="9b05b-145">Den anbefalte ruten er å **publisere en [lagret visning](saved-views.md)** med det egendefinerte feltet lagt til på siden for riktig sett med brukere.</span><span class="sxs-lookup"><span data-stu-id="9b05b-145">The recommended route is to **publish a [saved view](saved-views.md)** with the custom field added to the page to the appropriate set of users.</span></span> <span data-ttu-id="9b05b-146">Hvis funksjonen for lagret visning ikke er aktivert, kan systemadministrator bruke tilpasningen for de ønskede brukerne fra tilpasningsskjemaet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-146">If the saved views feature is not enabled, the system administrator can apply the personalization to the desired users from the Personalization form.</span></span> <span data-ttu-id="9b05b-147">Hvis du vil ha mer informasjon, kan du se [Tilpasse brukeropplevelsen](personalize-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="9b05b-147">For more information, see [Personalize the user experience](personalize-user-experience.md).</span></span>
- <span data-ttu-id="9b05b-148">Du kan også eksportere endringene (kalt *tilpasninger*), sende dem til én eller flere brukere, og få hver av disse brukerne til å importere endringene.</span><span class="sxs-lookup"><span data-stu-id="9b05b-148">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="9b05b-149">Med **Behandle**-alternativet på tilpassingsverktøylinjen kan du eksportere og importere tilpasninger.</span><span class="sxs-lookup"><span data-stu-id="9b05b-149">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="9b05b-150">Behandle egendefinerte felt</span><span class="sxs-lookup"><span data-stu-id="9b05b-150">Managing custom fields</span></span>

<span data-ttu-id="9b05b-151">Administrasjon av alle de egendefinerte feltene i systemet kan gjøres ved hjelp av **Egendefinerte felt**-siden i systemadministrasjonsmodulen.</span><span class="sxs-lookup"><span data-stu-id="9b05b-151">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span> <span data-ttu-id="9b05b-152">Denne siden gir brukere tilgang til mange funksjoner, som:</span><span class="sxs-lookup"><span data-stu-id="9b05b-152">This page allows users access to many capabilities, including:</span></span>

- <span data-ttu-id="9b05b-153">Vise en liste over alle de egendefinerte feltene i systemet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-153">Viewing a list of all custom fields in the system.</span></span>
- <span data-ttu-id="9b05b-154">Begrenset redigering av eksisterende egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="9b05b-154">Limited editing of existing custom fields.</span></span>
- <span data-ttu-id="9b05b-155">Slette egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="9b05b-155">Deleting custom fields.</span></span>
- <span data-ttu-id="9b05b-156">Vise egendefinerte felt på dataenheter.</span><span class="sxs-lookup"><span data-stu-id="9b05b-156">Exposing custom fields on data entities.</span></span>
- <span data-ttu-id="9b05b-157">Gi oversettelser av etiketter og hjelpetekst for egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="9b05b-157">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="9b05b-158">Vise alle egendefinerte felt</span><span class="sxs-lookup"><span data-stu-id="9b05b-158">Viewing all custom fields</span></span>

<span data-ttu-id="9b05b-159">**Egendefinerte felt**-siden gir en oversikt over alle de egendefinerte feltene som er definert i systemet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-159">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="9b05b-160">Bare velg tabellen som du er interessert i, og siden oppdateres og vil vise en liste over de egendefinerte feltene som er knyttet til denne tabellen.</span><span class="sxs-lookup"><span data-stu-id="9b05b-160">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="9b05b-161">Hvis du velger et egendefinert felt fra listen, kan du vise alle detaljene om feltet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-161">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="9b05b-162">Redigere egendefinerte felt</span><span class="sxs-lookup"><span data-stu-id="9b05b-162">Editing custom fields</span></span>

<span data-ttu-id="9b05b-163">Når du har opprettet et egendefinert felt, er det bare bestemte deler av informasjonen om det egendefinerte feltet som kan endres på **Egendefinerte felt**-siden.</span><span class="sxs-lookup"><span data-stu-id="9b05b-163">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>

<span data-ttu-id="9b05b-164">Du *kan* endre disse attributtene:</span><span class="sxs-lookup"><span data-stu-id="9b05b-164">You *can* modify these attributes:</span></span>

- <span data-ttu-id="9b05b-165">Etikett</span><span class="sxs-lookup"><span data-stu-id="9b05b-165">Label</span></span>
- <span data-ttu-id="9b05b-166">Hjelpetekst</span><span class="sxs-lookup"><span data-stu-id="9b05b-166">Help text</span></span>
- <span data-ttu-id="9b05b-167">Lengde, for tekstfelt</span><span class="sxs-lookup"><span data-stu-id="9b05b-167">Length, for Text fields</span></span>

<span data-ttu-id="9b05b-168">Du *kan ikke* redigere følgende attributter:</span><span class="sxs-lookup"><span data-stu-id="9b05b-168">You *cannot* edit the following attributes:</span></span>

- <span data-ttu-id="9b05b-169">Feltnavn</span><span class="sxs-lookup"><span data-stu-id="9b05b-169">Field name</span></span>
- <span data-ttu-id="9b05b-170">Datatype</span><span class="sxs-lookup"><span data-stu-id="9b05b-170">Data type</span></span>

<span data-ttu-id="9b05b-171">I tillegg, for plukklistefelt, kan du endre rekkefølgen på settet med gyldige verdier for det egendefinerte feltet og legge til nye verdier. Eksisterende verdier for plukklistefeltet kan imidlertid ikke fjernes.</span><span class="sxs-lookup"><span data-stu-id="9b05b-171">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="9b05b-172">Husk å klikke **Bruk endringer** når du er ferdig med å redigere feltene for en bestemt tabell slik at endringene lagres.</span><span class="sxs-lookup"><span data-stu-id="9b05b-172">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span>

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="9b05b-173">Vise egendefinerte felt på dataenheter</span><span class="sxs-lookup"><span data-stu-id="9b05b-173">Exposing custom fields on data entities</span></span>

<span data-ttu-id="9b05b-174">Det kan også være viktig å tillate at egendefinerte felt kan vises på dataenheter.</span><span class="sxs-lookup"><span data-stu-id="9b05b-174">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="9b05b-175">Dataenheter brukes i [Oversikt over Office-integrering](../../dev-itpro/office-integration/office-integration.md)-funksjonen, samt for dataimport- og dataeksportscenarier.</span><span class="sxs-lookup"><span data-stu-id="9b05b-175">Data entities are utilized in the [Office integration overview](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>

<span data-ttu-id="9b05b-176">Følg denne fremgangsmåten for å vise et egendefinert felt på en dataenhet:</span><span class="sxs-lookup"><span data-stu-id="9b05b-176">Follow these steps to expose a custom field on a data entity:</span></span>

1. <span data-ttu-id="9b05b-177">Velg det egendefinerte feltet i **Egendefinerte felt** skjemaet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-177">Select the custom field on the **Custom fields** form.</span></span>
2. <span data-ttu-id="9b05b-178">Utvid **Enheter**-delen til å vise settet med relevante enheter.</span><span class="sxs-lookup"><span data-stu-id="9b05b-178">Expand the **Entities** section to view the set of relevant entities.</span></span>
3. <span data-ttu-id="9b05b-179">Klikk på **Rediger**-knappen.</span><span class="sxs-lookup"><span data-stu-id="9b05b-179">Click the **Edit** button.</span></span>
4. <span data-ttu-id="9b05b-180">Endre **Aktivert**-feltet slik at det velges for hver enhet som skal vise dette feltet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-180">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>
5. <span data-ttu-id="9b05b-181">Klikk på **Bruk endringer** for å lagre valgene.</span><span class="sxs-lookup"><span data-stu-id="9b05b-181">Click **Apply changes** to save your selections.</span></span>

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="9b05b-182">Tillate at egendefinerte felt vises på andre språk</span><span class="sxs-lookup"><span data-stu-id="9b05b-182">Allowing custom fields to be displayed in other languages</span></span>

<span data-ttu-id="9b05b-183">Ettersom det kan være behov for tilgang til egendefinerte felt på forskjellige språk, har **Egendefinerte felt**-siden en mekanisme for å tillate at etikett- og hjelpeteksten for et egendefinert felt kan oversettes til andre språk.</span><span class="sxs-lookup"><span data-stu-id="9b05b-183">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>

<span data-ttu-id="9b05b-184">Trinnene nedenfor beskriver prosessen for å oversette egendefinerte felt til andre språk:</span><span class="sxs-lookup"><span data-stu-id="9b05b-184">The following steps describe the process for translating custom fields in other languages:</span></span>

1. <span data-ttu-id="9b05b-185">Velg det egendefinerte feltet på **Egendefinerte felt**-siden.</span><span class="sxs-lookup"><span data-stu-id="9b05b-185">Select the custom field on the **Custom fields** page.</span></span>
2. <span data-ttu-id="9b05b-186">Velg **Oversettelser**-knappen i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9b05b-186">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="9b05b-187">Dette åpner en rullegardinmeny med eksisterende oversettelser for dette feltet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-187">This will open a drop-down menu with existing translations for this field.</span></span>
3. <span data-ttu-id="9b05b-188">**Språk**-rullegardinmenyen viser settet med språk som det er allerede er gitt oversettelser for.</span><span class="sxs-lookup"><span data-stu-id="9b05b-188">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span>

    <span data-ttu-id="9b05b-189">Hvis du vil redigere en eksisterende oversettelse, velger du ønsket språk fra menyen og endrer verdiene for etiketten og hjelpeteksten.</span><span class="sxs-lookup"><span data-stu-id="9b05b-189">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>

    <span data-ttu-id="9b05b-190">Ellers klikker du **Legg til språk**-knappen, velger ønsket språk fra menyen og angir deretter oversatte verdier for etikett- og hjelpeteksten.</span><span class="sxs-lookup"><span data-stu-id="9b05b-190">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>

4. <span data-ttu-id="9b05b-191">Klikk på **OK** når du er ferdig.</span><span class="sxs-lookup"><span data-stu-id="9b05b-191">Click **OK** when you are finished.</span></span>

### <a name="deleting-custom-fields"></a><span data-ttu-id="9b05b-192">Slette egendefinerte felt</span><span class="sxs-lookup"><span data-stu-id="9b05b-192">Deleting custom fields</span></span>

<span data-ttu-id="9b05b-193">I enkelte sjeldne tilfeller kan du bestemme at et egendefinert felt ikke lenger er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="9b05b-193">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="9b05b-194">Når dette skjer, kan systemansvarlig velge å slette feltet fra **Egendefinerte felt**-siden.</span><span class="sxs-lookup"><span data-stu-id="9b05b-194">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="9b05b-195">Hvis du vil gjøre dette, kontrollerer du at riktig felt er valgt, klikker **Slett**, klikker **Ja** for å bekrefte slettingen, og klikker til slutt **Bruk endringer**.</span><span class="sxs-lookup"><span data-stu-id="9b05b-195">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="9b05b-196">Denne handlingen kan ikke angres, og fører til at dataene som er knyttet til feltet, slettes permanent fra databasen.</span><span class="sxs-lookup"><span data-stu-id="9b05b-196">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span>

## <a name="appendix"></a><span data-ttu-id="9b05b-197">Tillegg</span><span class="sxs-lookup"><span data-stu-id="9b05b-197">Appendix</span></span>

### <a name="why-cant-i-enter-a-value-in-my-custom-field"></a><span data-ttu-id="9b05b-198">Hvorfor kan jeg ikke angi en verdi i det egendefinerte feltet?</span><span class="sxs-lookup"><span data-stu-id="9b05b-198">Why can't I enter a value in my custom field?</span></span> 

<span data-ttu-id="9b05b-199">Hvis du ikke kan skrive inn en verdi i det egendefinerte feltet når siden er i redigeringsmodus, kan dette skyldes at tabellen som feltet ble lagt til i, for øyeblikket er skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-199">If you can't type a value into the custom field when the page is in Edit mode, this may be because the table that the field was added to is currently read only.</span></span> <span data-ttu-id="9b05b-200">Alle feltene i en tabell blir skrivebeskyttet hvis backing-tabellen for øyeblikket er konfigurert som skrivebeskyttet på siden.</span><span class="sxs-lookup"><span data-stu-id="9b05b-200">All fields in a table become read only if the backing table is currently configured as read only on the page.</span></span>   

### <a name="who-can-create-custom-fields"></a><span data-ttu-id="9b05b-201">Hvem kan opprette egendefinerte felt?</span><span class="sxs-lookup"><span data-stu-id="9b05b-201">Who can create custom fields?</span></span>

<span data-ttu-id="9b05b-202">Som en beskyttelse av systemet kan bare systemansvarlige opprette egendefinerte felt som standard.</span><span class="sxs-lookup"><span data-stu-id="9b05b-202">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="9b05b-203">De privilegerte brukerne som organisasjonen anser som nødvendige, kan imidlertid gis rettigheter til å opprette egendefinerte felt av en systemansvarlig ved hjelp av sikkerhetsrollen **Privilegert bruker for kjøretidstilpasning**.</span><span class="sxs-lookup"><span data-stu-id="9b05b-203">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="9b05b-204">Brukere uten denne sikkerhetsrollen kan ikke opprette egendefinerte felt, men vil fremdeles kunne se og samhandle med egendefinerte felt som er lagt til av andre brukere i systemet.</span><span class="sxs-lookup"><span data-stu-id="9b05b-204">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="9b05b-205">Hvilke tabeller støtter egendefinerte felt?</span><span class="sxs-lookup"><span data-stu-id="9b05b-205">What tables support custom fields?</span></span>

<span data-ttu-id="9b05b-206">Av ytelsesårsaker og tekniske årsaker er det bare tabeller som oppfyller følgende vilkår som for tiden tillater at egendefinerte felt legges til.</span><span class="sxs-lookup"><span data-stu-id="9b05b-206">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="9b05b-207">Tabellen må merkes som en av disse gruppene:</span><span class="sxs-lookup"><span data-stu-id="9b05b-207">The table must be tagged as one of these groups:</span></span>

    - <span data-ttu-id="9b05b-208">Gruppere</span><span class="sxs-lookup"><span data-stu-id="9b05b-208">Group</span></span>
    - <span data-ttu-id="9b05b-209">WorksheetHeader</span><span class="sxs-lookup"><span data-stu-id="9b05b-209">WorksheetHeader</span></span>
    - <span data-ttu-id="9b05b-210">Hoved</span><span class="sxs-lookup"><span data-stu-id="9b05b-210">Main</span></span>
    - <span data-ttu-id="9b05b-211">Diverse</span><span class="sxs-lookup"><span data-stu-id="9b05b-211">Miscellaneous</span></span>
    - <span data-ttu-id="9b05b-212">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b05b-212">Parameter</span></span>
    - <span data-ttu-id="9b05b-213">Referanse</span><span class="sxs-lookup"><span data-stu-id="9b05b-213">Reference</span></span>
    - <span data-ttu-id="9b05b-214">TransactionHeader</span><span class="sxs-lookup"><span data-stu-id="9b05b-214">TransactionHeader</span></span>

- <span data-ttu-id="9b05b-215">Tabellen kan ikke utvide en annen tabell.</span><span class="sxs-lookup"><span data-stu-id="9b05b-215">The table cannot extend another table.</span></span>
- <span data-ttu-id="9b05b-216">Tabellen kan ikke merkes som en systemtabell.</span><span class="sxs-lookup"><span data-stu-id="9b05b-216">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="9b05b-217">Tabellen kan ikke være en midlertidig tabell.</span><span class="sxs-lookup"><span data-stu-id="9b05b-217">The table cannot be a temporary table.</span></span>

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a><span data-ttu-id="9b05b-218">Kan jeg referere til egendefinerte felt fra utviklerverktøy?</span><span class="sxs-lookup"><span data-stu-id="9b05b-218">Can I reference custom fields from the developer tools?</span></span>  

<span data-ttu-id="9b05b-219">Egendefinerte felt kan bare administreres gjennom brukergrensesnittet og kan ikke refereres til av koden.</span><span class="sxs-lookup"><span data-stu-id="9b05b-219">Custom fields can only be managed through the user interface and cannot be referenced by code.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
