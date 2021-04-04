---
title: Opprette og arbeide med egendefinerte felt
description: Dette emnet forklarer hvordan du oppretter egendefinerte felt via brukergrensesnittet for å tilpasse programmet slik at det passer for bedriften.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
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
ms.openlocfilehash: 9c97393419278e49b112f98ba6dcc4bec9565cb7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566276"
---
# <a name="create-and-work-with-custom-fields"></a><span data-ttu-id="bda54-103">Opprette og arbeide med egendefinerte felt</span><span class="sxs-lookup"><span data-stu-id="bda54-103">Create and work with custom fields</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bda54-104">Selv om det er et omfattende sett med felt som standard for å administrere mange forretningsprosesser, har et firma noen ganger behov for å spore ytterligere informasjon i systemet.</span><span class="sxs-lookup"><span data-stu-id="bda54-104">While there is an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="bda54-105">Selv om programmerere kan brukes til å legge til disse feltene som utvidelser i utviklerverktøy, gjør funksjonen egendefinerte felt det mulig å legge til felt direkte fra brukergrensesnittet, slik at du kan skreddersy programmet slik at det passer til bedriften din ved hjelp av Webleseren.</span><span class="sxs-lookup"><span data-stu-id="bda54-105">While programmers can be used to add those fields as extensions in the developer tools, the custom fields feature allows fields to be added directly from the user interface, thereby allowing you to tailor the application to fit your business using your web browser.</span></span>

<span data-ttu-id="bda54-106">Muligheten til å legge til egendefinerte felt er tilgjengelig i plattformoppdateringen 13 og senere.</span><span class="sxs-lookup"><span data-stu-id="bda54-106">The ability to add custom fields is available in platform update 13 and later.</span></span> <span data-ttu-id="bda54-107">Bare brukere med spesialtilgang har tilgang til denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="bda54-107">Only users with special permissions have access to this feature.</span></span>

<span data-ttu-id="bda54-108">Denne videoen viser hvor enkelt det er å legge til et egendefinert felt på en side: [Legge til egendefinerte felt](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span><span class="sxs-lookup"><span data-stu-id="bda54-108">This video shows how easy it is to add a custom field to a page: [Adding custom fields](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span></span>

## <a name="creating-custom-fields"></a><span data-ttu-id="bda54-109">Opprette egendefinerte felt</span><span class="sxs-lookup"><span data-stu-id="bda54-109">Creating custom fields</span></span>

<span data-ttu-id="bda54-110">Når du har identifisert tilleggsinformasjon du vil spore i programmet, kan du opprette det egendefinerte feltet i den aktuelle tabellen og vise det nye feltet på en side.</span><span class="sxs-lookup"><span data-stu-id="bda54-110">After you've identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>

<span data-ttu-id="bda54-111">Trinnene nedenfor beskriver prosessen for å opprette et egendefinert felt og plassere dette feltet i et skjema.</span><span class="sxs-lookup"><span data-stu-id="bda54-111">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>

1. <span data-ttu-id="bda54-112">Naviger til skjemaet der det er behov for det nye feltet.</span><span class="sxs-lookup"><span data-stu-id="bda54-112">Navigate to the form where the new field is needed.</span></span>
2. <span data-ttu-id="bda54-113">Fordi sluttmålet er å vise det egendefinerte feltet i et skjema, finnes inngangspunktet for å opprette egendefinerte felt i tilpassingsopplevelsen.</span><span class="sxs-lookup"><span data-stu-id="bda54-113">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="bda54-114">Åpne tilpassingsverktøylinjen ved å velge **Alternativer** og deretter **Tilpass dette skjemaet**.</span><span class="sxs-lookup"><span data-stu-id="bda54-114">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span>
3. <span data-ttu-id="bda54-115">Klikk på **Sett inn** og deretter **Felt**.</span><span class="sxs-lookup"><span data-stu-id="bda54-115">Click **Insert** and then **Field**.</span></span>
4. <span data-ttu-id="bda54-116">Velg området i skjemaet der du vil vise det nye feltet.</span><span class="sxs-lookup"><span data-stu-id="bda54-116">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="bda54-117">Når du har valgt det, viser **Sett inn felt**-dialogboksen en liste over eksisterende felt som kan settes inn i det merkede området i skjemaet.</span><span class="sxs-lookup"><span data-stu-id="bda54-117">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>
5. <span data-ttu-id="bda54-118">Kontroller at feltet du er interessert i, ikke allerede finnes i listen.</span><span class="sxs-lookup"><span data-stu-id="bda54-118">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="bda54-119">Hvis det finnes, kan du ganske enkelt velge feltet i listen og klikke **Sett inn**.</span><span class="sxs-lookup"><span data-stu-id="bda54-119">If it does, you can simply select that field in the list and click **Insert**.</span></span>
6. <span data-ttu-id="bda54-120">Klikk på **Opprett nytt felt**-knappen over listen for å starte prosessen med å lage et egendefinert felt.</span><span class="sxs-lookup"><span data-stu-id="bda54-120">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="bda54-121">Dette åpner **Opprett nytt felt**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bda54-121">This will open the **Create new field** dialog box.</span></span>

    <span data-ttu-id="bda54-122">Hvis du ikke ser **Opprett nytt felt**-knappen, har du ikke de nødvendige tillatelsene til å bruke denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="bda54-122">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>

7. <span data-ttu-id="bda54-123">Angi følgende informasjon i dialogboksen **Opprett nytt felt**.</span><span class="sxs-lookup"><span data-stu-id="bda54-123">In the **Create new field** dialog box, enter the following information.</span></span>

    1. <span data-ttu-id="bda54-124">Velg databasetabellen der dette feltet skal legges til.</span><span class="sxs-lookup"><span data-stu-id="bda54-124">Select the database table where this field should be added.</span></span> <span data-ttu-id="bda54-125">Legg merke til at bare tabeller som støtter egendefinerte felt, vises i fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="bda54-125">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="bda54-126">Se delen nedenfor for tekniske detaljer om støttede tabeller.</span><span class="sxs-lookup"><span data-stu-id="bda54-126">See the section below for technical details on supported tables.</span></span>
    2. <span data-ttu-id="bda54-127">Velg datatypen for det nye feltet.</span><span class="sxs-lookup"><span data-stu-id="bda54-127">Select the data type for the new field.</span></span> <span data-ttu-id="bda54-128">Tilgjengelige datatyper er avmerkingsboks, dato, dato/klokkeslett, desimal, tall, plukkliste og tekst.</span><span class="sxs-lookup"><span data-stu-id="bda54-128">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>

        - <span data-ttu-id="bda54-129">Hvis du velger datatypen tekst, kan du også angi den maksimale lengden på teksten som kan angis i dette feltet.</span><span class="sxs-lookup"><span data-stu-id="bda54-129">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span>
        - <span data-ttu-id="bda54-130">Hvis du velger datatypen plukkliste, kan du også velge settet med gyldige verdier for feltet.</span><span class="sxs-lookup"><span data-stu-id="bda54-130">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>

    3. <span data-ttu-id="bda54-131">Angi navn, etikett, og hjelpetekst for feltet.</span><span class="sxs-lookup"><span data-stu-id="bda54-131">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="bda54-132">Navnet tilsvarer det fysiske feltnavnet i databasen, mens etikett- og hjelpeteksten er teksten som brukes til å representere dette feltet i brukergrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="bda54-132">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>

8. <span data-ttu-id="bda54-133">Hvis dette er det eneste feltet du vil opprette for dette skjemaet, klikker du **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="bda54-133">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="bda54-134">Hvis du vil opprette flere felt, klikker du **Lagre og ny** og går tilbake til trinn 7.</span><span class="sxs-lookup"><span data-stu-id="bda54-134">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="bda54-135">Legg merke til at det er en grense på **20 egendefinerte felt per tabell**.</span><span class="sxs-lookup"><span data-stu-id="bda54-135">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9. <span data-ttu-id="bda54-136">Når du avslutter **Opprett nytt felt**-dialogboksen, kommer du tilbake til **Sett inn felt**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="bda54-136">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="bda54-137">Egendefinerte felt som nettopp ble lagt til, merkes automatisk i feltlisten til å bli satt inn i skjemaet.</span><span class="sxs-lookup"><span data-stu-id="bda54-137">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>
10. <span data-ttu-id="bda54-138">Klikk på **Sett inn** for å sette inn de merkede feltene i det valgte området i skjemaet.</span><span class="sxs-lookup"><span data-stu-id="bda54-138">Click **Insert** to insert the marked fields into the selected region of the form.</span></span>
11. <span data-ttu-id="bda54-139">**Valgfritt:** Aktiver **Flytt**-modus fra tilpassingsverktøylinjen for å flytte de nye feltene til ønsket plassering i det valgte området.</span><span class="sxs-lookup"><span data-stu-id="bda54-139">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="bda54-140">Se [Tilpasse brukeropplevelsen](personalize-user-experience.md) for mer informasjon om hvordan du bruker de ulike tilpassingsfunksjonene for å optimalisere et skjema for din personlige bruk.</span><span class="sxs-lookup"><span data-stu-id="bda54-140">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>

## <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="bda54-141">Dele egendefinerte felt med andre brukere</span><span class="sxs-lookup"><span data-stu-id="bda54-141">Sharing custom fields with other users</span></span>

<span data-ttu-id="bda54-142">Når du har opprettet et egendefinert felt og vist det i et skjema, kan det hende at du vil gi denne oppdaterte sidevisningen som inneholder det nye feltet, til andre brukere i systemet.</span><span class="sxs-lookup"><span data-stu-id="bda54-142">After you have created a custom field and exposed it on a form, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="bda54-143">Dette kan gjøres på to forskjellige måter ved hjelp av tilpassingsfunksjonene i produktet:</span><span class="sxs-lookup"><span data-stu-id="bda54-143">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="bda54-144">Den anbefalte måten er via systemadministratoren, som kan overføre en tilpassing til alle brukere eller en undergruppe av brukere.</span><span class="sxs-lookup"><span data-stu-id="bda54-144">The recommended route is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> <span data-ttu-id="bda54-145">Se [Tilpasse brukeropplevelsen](personalize-user-experience.md) for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="bda54-145">See [Personalize the user experience](personalize-user-experience.md) for more details.</span></span>
- <span data-ttu-id="bda54-146">Du kan også eksportere endringene (kalt *tilpasninger*), sende dem til én eller flere brukere, og få hver av disse brukerne til å importere endringene.</span><span class="sxs-lookup"><span data-stu-id="bda54-146">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="bda54-147">Med **Behandle**-alternativet på tilpassingsverktøylinjen kan du eksportere og importere tilpasninger.</span><span class="sxs-lookup"><span data-stu-id="bda54-147">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="bda54-148">Behandle egendefinerte felt</span><span class="sxs-lookup"><span data-stu-id="bda54-148">Managing custom fields</span></span>

<span data-ttu-id="bda54-149">Administrasjon av alle de egendefinerte feltene i systemet kan gjøres ved hjelp av **Egendefinerte felt**-siden i systemadministrasjonsmodulen.</span><span class="sxs-lookup"><span data-stu-id="bda54-149">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span> <span data-ttu-id="bda54-150">Denne siden gir brukere tilgang til mange funksjoner, som:</span><span class="sxs-lookup"><span data-stu-id="bda54-150">This page allows users access to many capabilities, including:</span></span>

- <span data-ttu-id="bda54-151">Vise en liste over alle de egendefinerte feltene i systemet.</span><span class="sxs-lookup"><span data-stu-id="bda54-151">Viewing a list of all custom fields in the system.</span></span>
- <span data-ttu-id="bda54-152">Begrenset redigering av eksisterende egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="bda54-152">Limited editing of existing custom fields.</span></span>
- <span data-ttu-id="bda54-153">Slette egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="bda54-153">Deleting custom fields.</span></span>
- <span data-ttu-id="bda54-154">Vise egendefinerte felt på dataenheter.</span><span class="sxs-lookup"><span data-stu-id="bda54-154">Exposing custom fields on data entities.</span></span>
- <span data-ttu-id="bda54-155">Gi oversettelser av etiketter og hjelpetekst for egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="bda54-155">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="bda54-156">Vise alle egendefinerte felt</span><span class="sxs-lookup"><span data-stu-id="bda54-156">Viewing all custom fields</span></span>

<span data-ttu-id="bda54-157">**Egendefinerte felt**-siden gir en oversikt over alle de egendefinerte feltene som er definert i systemet.</span><span class="sxs-lookup"><span data-stu-id="bda54-157">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="bda54-158">Bare velg tabellen som du er interessert i, og siden oppdateres og vil vise en liste over de egendefinerte feltene som er knyttet til denne tabellen.</span><span class="sxs-lookup"><span data-stu-id="bda54-158">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="bda54-159">Hvis du velger et egendefinert felt fra listen, kan du vise alle detaljene om feltet.</span><span class="sxs-lookup"><span data-stu-id="bda54-159">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="bda54-160">Redigere egendefinerte felt</span><span class="sxs-lookup"><span data-stu-id="bda54-160">Editing custom fields</span></span>

<span data-ttu-id="bda54-161">Når du har opprettet et egendefinert felt, er det bare bestemte deler av informasjonen om det egendefinerte feltet som kan endres på **Egendefinerte felt**-siden.</span><span class="sxs-lookup"><span data-stu-id="bda54-161">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>

<span data-ttu-id="bda54-162">Du *kan* endre disse attributtene:</span><span class="sxs-lookup"><span data-stu-id="bda54-162">You *can* modify these attributes:</span></span>

- <span data-ttu-id="bda54-163">Etikett</span><span class="sxs-lookup"><span data-stu-id="bda54-163">Label</span></span>
- <span data-ttu-id="bda54-164">Hjelpetekst</span><span class="sxs-lookup"><span data-stu-id="bda54-164">Help text</span></span>
- <span data-ttu-id="bda54-165">Lengde, for tekstfelt</span><span class="sxs-lookup"><span data-stu-id="bda54-165">Length, for Text fields</span></span>

<span data-ttu-id="bda54-166">Du *kan ikke* redigere følgende attributter:</span><span class="sxs-lookup"><span data-stu-id="bda54-166">You *cannot* edit the following attributes:</span></span>

- <span data-ttu-id="bda54-167">Feltnavn</span><span class="sxs-lookup"><span data-stu-id="bda54-167">Field name</span></span>
- <span data-ttu-id="bda54-168">Datatype</span><span class="sxs-lookup"><span data-stu-id="bda54-168">Data type</span></span>

<span data-ttu-id="bda54-169">I tillegg, for plukklistefelt, kan du endre rekkefølgen på settet med gyldige verdier for det egendefinerte feltet og legge til nye verdier. Eksisterende verdier for plukklistefeltet kan imidlertid ikke fjernes.</span><span class="sxs-lookup"><span data-stu-id="bda54-169">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="bda54-170">Husk å klikke **Bruk endringer** når du er ferdig med å redigere feltene for en bestemt tabell slik at endringene lagres.</span><span class="sxs-lookup"><span data-stu-id="bda54-170">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span>

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="bda54-171">Vise egendefinerte felt på dataenheter</span><span class="sxs-lookup"><span data-stu-id="bda54-171">Exposing custom fields on data entities</span></span>

<span data-ttu-id="bda54-172">Det kan også være viktig å tillate at egendefinerte felt kan vises på dataenheter.</span><span class="sxs-lookup"><span data-stu-id="bda54-172">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="bda54-173">Dataenheter brukes i [Oversikt over Office-integrering](../../dev-itpro/office-integration/office-integration.md)-funksjonen, samt for dataimport- og dataeksportscenarier.</span><span class="sxs-lookup"><span data-stu-id="bda54-173">Data entities are utilized in the [Office integration overview](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>

<span data-ttu-id="bda54-174">Følg denne fremgangsmåten for å vise et egendefinert felt på en dataenhet:</span><span class="sxs-lookup"><span data-stu-id="bda54-174">Follow these steps to expose a custom field on a data entity:</span></span>

1. <span data-ttu-id="bda54-175">Velg det egendefinerte feltet i **Egendefinerte felt** skjemaet.</span><span class="sxs-lookup"><span data-stu-id="bda54-175">Select the custom field on the **Custom fields** form.</span></span>
2. <span data-ttu-id="bda54-176">Utvid **Enheter**-delen til å vise settet med relevante enheter.</span><span class="sxs-lookup"><span data-stu-id="bda54-176">Expand the **Entities** section to view the set of relevant entities.</span></span>
3. <span data-ttu-id="bda54-177">Klikk på **Rediger**-knappen.</span><span class="sxs-lookup"><span data-stu-id="bda54-177">Click the **Edit** button.</span></span>
4. <span data-ttu-id="bda54-178">Endre **Aktivert**-feltet slik at det velges for hver enhet som skal vise dette feltet.</span><span class="sxs-lookup"><span data-stu-id="bda54-178">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>
5. <span data-ttu-id="bda54-179">Klikk på **Bruk endringer** for å lagre valgene.</span><span class="sxs-lookup"><span data-stu-id="bda54-179">Click **Apply changes** to save your selections.</span></span>

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="bda54-180">Tillate at egendefinerte felt vises på andre språk</span><span class="sxs-lookup"><span data-stu-id="bda54-180">Allowing custom fields to be displayed in other languages</span></span>

<span data-ttu-id="bda54-181">Ettersom det kan være behov for tilgang til egendefinerte felt på forskjellige språk, har **Egendefinerte felt**-siden en mekanisme for å tillate at etikett- og hjelpeteksten for et egendefinert felt kan oversettes til andre språk.</span><span class="sxs-lookup"><span data-stu-id="bda54-181">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>

<span data-ttu-id="bda54-182">Trinnene nedenfor beskriver prosessen for å oversette egendefinerte felt til andre språk:</span><span class="sxs-lookup"><span data-stu-id="bda54-182">The following steps describe the process for translating custom fields in other languages:</span></span>

1. <span data-ttu-id="bda54-183">Velg det egendefinerte feltet på **Egendefinerte felt**-siden.</span><span class="sxs-lookup"><span data-stu-id="bda54-183">Select the custom field on the **Custom fields** page.</span></span>
2. <span data-ttu-id="bda54-184">Velg **Oversettelser**-knappen i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="bda54-184">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="bda54-185">Dette åpner en rullegardinmeny med eksisterende oversettelser for dette feltet.</span><span class="sxs-lookup"><span data-stu-id="bda54-185">This will open a drop-down menu with existing translations for this field.</span></span>
3. <span data-ttu-id="bda54-186">**Språk**-rullegardinmenyen viser settet med språk som det er allerede er gitt oversettelser for.</span><span class="sxs-lookup"><span data-stu-id="bda54-186">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span>

    <span data-ttu-id="bda54-187">Hvis du vil redigere en eksisterende oversettelse, velger du ønsket språk fra menyen og endrer verdiene for etiketten og hjelpeteksten.</span><span class="sxs-lookup"><span data-stu-id="bda54-187">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>

    <span data-ttu-id="bda54-188">Ellers klikker du **Legg til språk**-knappen, velger ønsket språk fra menyen og angir deretter oversatte verdier for etikett- og hjelpeteksten.</span><span class="sxs-lookup"><span data-stu-id="bda54-188">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>

4. <span data-ttu-id="bda54-189">Klikk på **OK** når du er ferdig.</span><span class="sxs-lookup"><span data-stu-id="bda54-189">Click **OK** when you are finished.</span></span>

### <a name="deleting-custom-fields"></a><span data-ttu-id="bda54-190">Slette egendefinerte felt</span><span class="sxs-lookup"><span data-stu-id="bda54-190">Deleting custom fields</span></span>

<span data-ttu-id="bda54-191">I enkelte sjeldne tilfeller kan du bestemme at et egendefinert felt ikke lenger er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="bda54-191">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="bda54-192">Når dette skjer, kan systemansvarlig velge å slette feltet fra **Egendefinerte felt**-siden.</span><span class="sxs-lookup"><span data-stu-id="bda54-192">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="bda54-193">Hvis du vil gjøre dette, kontrollerer du at riktig felt er valgt, klikker **Slett**, klikker **Ja** for å bekrefte slettingen, og klikker til slutt **Bruk endringer**.</span><span class="sxs-lookup"><span data-stu-id="bda54-193">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="bda54-194">Denne handlingen kan ikke angres, og fører til at dataene som er knyttet til feltet, slettes permanent fra databasen.</span><span class="sxs-lookup"><span data-stu-id="bda54-194">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span>

## <a name="appendix"></a><span data-ttu-id="bda54-195">Tillegg</span><span class="sxs-lookup"><span data-stu-id="bda54-195">Appendix</span></span>

### <a name="who-can-create-custom-fields"></a><span data-ttu-id="bda54-196">Hvem kan opprette egendefinerte felt?</span><span class="sxs-lookup"><span data-stu-id="bda54-196">Who can create custom fields?</span></span>

<span data-ttu-id="bda54-197">Som en beskyttelse av systemet kan bare systemansvarlige opprette egendefinerte felt som standard.</span><span class="sxs-lookup"><span data-stu-id="bda54-197">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="bda54-198">De privilegerte brukerne som organisasjonen anser som nødvendige, kan imidlertid gis rettigheter til å opprette egendefinerte felt av en systemansvarlig ved hjelp av sikkerhetsrollen **Privilegert bruker for kjøretidstilpasning**.</span><span class="sxs-lookup"><span data-stu-id="bda54-198">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="bda54-199">Brukere uten denne sikkerhetsrollen kan ikke opprette egendefinerte felt, men vil fremdeles kunne se og samhandle med egendefinerte felt som er lagt til av andre brukere i systemet.</span><span class="sxs-lookup"><span data-stu-id="bda54-199">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="bda54-200">Hvilke tabeller støtter egendefinerte felt?</span><span class="sxs-lookup"><span data-stu-id="bda54-200">What tables support custom fields?</span></span>

<span data-ttu-id="bda54-201">Av ytelsesårsaker og tekniske årsaker er det bare tabeller som oppfyller følgende vilkår som for tiden tillater at egendefinerte felt legges til.</span><span class="sxs-lookup"><span data-stu-id="bda54-201">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="bda54-202">Tabellen må merkes som en av disse gruppene:</span><span class="sxs-lookup"><span data-stu-id="bda54-202">The table must be tagged as one of these groups:</span></span>

    - <span data-ttu-id="bda54-203">Gruppere</span><span class="sxs-lookup"><span data-stu-id="bda54-203">Group</span></span>
    - <span data-ttu-id="bda54-204">WorksheetHeader</span><span class="sxs-lookup"><span data-stu-id="bda54-204">WorksheetHeader</span></span>
    - <span data-ttu-id="bda54-205">Hoved</span><span class="sxs-lookup"><span data-stu-id="bda54-205">Main</span></span>
    - <span data-ttu-id="bda54-206">Diverse</span><span class="sxs-lookup"><span data-stu-id="bda54-206">Miscellaneous</span></span>
    - <span data-ttu-id="bda54-207">Parameter</span><span class="sxs-lookup"><span data-stu-id="bda54-207">Parameter</span></span>
    - <span data-ttu-id="bda54-208">Referanse</span><span class="sxs-lookup"><span data-stu-id="bda54-208">Reference</span></span>
    - <span data-ttu-id="bda54-209">TransactionHeader</span><span class="sxs-lookup"><span data-stu-id="bda54-209">TransactionHeader</span></span>

- <span data-ttu-id="bda54-210">Tabellen kan ikke utvide en annen tabell.</span><span class="sxs-lookup"><span data-stu-id="bda54-210">The table cannot extend another table.</span></span>
- <span data-ttu-id="bda54-211">Tabellen kan ikke merkes som en systemtabell.</span><span class="sxs-lookup"><span data-stu-id="bda54-211">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="bda54-212">Tabellen kan ikke være en midlertidig tabell.</span><span class="sxs-lookup"><span data-stu-id="bda54-212">The table cannot be a temporary table.</span></span>

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a><span data-ttu-id="bda54-213">Kan jeg referere til egendefinerte felt fra utviklerverktøy?</span><span class="sxs-lookup"><span data-stu-id="bda54-213">Can I reference custom fields from the developer tools?</span></span>  

<span data-ttu-id="bda54-214">Egendefinerte felt kan bare administreres gjennom brukergrensesnittet og kan ikke refereres til av koden.</span><span class="sxs-lookup"><span data-stu-id="bda54-214">Custom fields can only be managed through the user interface and cannot be referenced by code.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]