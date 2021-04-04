---
title: Migrering av valutadatatype for dobbelt skriving
description: Dette emnet beskriver hvordan du endrer antallet desimaler som dobbelt skriving støtter for valuta.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 78820ff49958fc3b474038c0fcd126bcf6886d0d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560829"
---
# <a name="currency-data-type-migration-for-dual-write"></a><span data-ttu-id="d9647-103">Migrering av valutadatatype for dobbelt skriving</span><span class="sxs-lookup"><span data-stu-id="d9647-103">Currency data-type migration for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d9647-104">Du kan øke antallet desimaler som støttes for valutaverdier, til maksimalt 10.</span><span class="sxs-lookup"><span data-stu-id="d9647-104">You can increase the number of decimal places that are supported for currency values to a maximum of 10.</span></span> <span data-ttu-id="d9647-105">Standardgrensen er fire desimalplasser.</span><span class="sxs-lookup"><span data-stu-id="d9647-105">The default limit is four decimal places.</span></span> <span data-ttu-id="d9647-106">Hvis du øker antallet desimaler, bidrar du til å hindre tap av data når du bruker toveisskriving for å synkronisere data.</span><span class="sxs-lookup"><span data-stu-id="d9647-106">By increasing the number of decimal places, you help prevent data loss when you use dual-write to sync data.</span></span> <span data-ttu-id="d9647-107">Økningen i antall desimalplasser er en endring som velges.</span><span class="sxs-lookup"><span data-stu-id="d9647-107">The increase in the number of decimal places is an opt-in change.</span></span> <span data-ttu-id="d9647-108">Hvis du vil implementere den, må du be om hjelp fra Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d9647-108">To implement it, you must request assistance from Microsoft.</span></span>

<span data-ttu-id="d9647-109">Prosessen med å endre antall desimaler har to trinn:</span><span class="sxs-lookup"><span data-stu-id="d9647-109">The process of changing the number of decimal places has two steps:</span></span>

1. <span data-ttu-id="d9647-110">Be om migrering fra Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d9647-110">Request migration from Microsoft.</span></span>
2. <span data-ttu-id="d9647-111">Endre antall desimaler i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d9647-111">Change the number of decimal places in Dataverse.</span></span>

<span data-ttu-id="d9647-112">Finance and Operations-appen og Dataverse må støtte samme antall desimalplasser i valutaverdier.</span><span class="sxs-lookup"><span data-stu-id="d9647-112">The Finance and Operations app and Dataverse must support the same number of decimal places in currency values.</span></span> <span data-ttu-id="d9647-113">Ellers kan det oppstå tap av data når denne informasjonen synkroniseres mellom apper.</span><span class="sxs-lookup"><span data-stu-id="d9647-113">Otherwise, data loss can occur when this information is synced between apps.</span></span> <span data-ttu-id="d9647-114">Migreringsprosessen konfigurerer måten valuta og valutakursverdier lagres på, på nytt, men den endrer ikke data.</span><span class="sxs-lookup"><span data-stu-id="d9647-114">The migration process reconfigures the way that currency and exchange rate values are stored, but it doesn't change any data.</span></span> <span data-ttu-id="d9647-115">Når migreringen er fullført, kan antall desimaler for valutakoder og prissetting økes, og dataene som brukere legger inn og viser, kan ha større desimalpresisjon.</span><span class="sxs-lookup"><span data-stu-id="d9647-115">After the migration is completed, the number of decimal places for currency codes and pricing can be increased, and the data that users enter and view can have more decimal precision.</span></span>

<span data-ttu-id="d9647-116">Migreringen er valgfri.</span><span class="sxs-lookup"><span data-stu-id="d9647-116">Migration is optional.</span></span> <span data-ttu-id="d9647-117">Hvis du kan dra nytte av støtte for flere desimaler, anbefaler vi at du vurderer migreringen.</span><span class="sxs-lookup"><span data-stu-id="d9647-117">If you might benefit from support for more decimal places, we recommend that you consider migration.</span></span> <span data-ttu-id="d9647-118">Organisasjoner som ikke krever verdier som har mer enn fire desimalplasser, trenger ikke å migrere.</span><span class="sxs-lookup"><span data-stu-id="d9647-118">Organizations that don't require values that have more than four decimal places don't have to migrate.</span></span>

## <a name="requesting-migration-from-microsoft"></a><span data-ttu-id="d9647-119">Be om migrering fra Microsoft</span><span class="sxs-lookup"><span data-stu-id="d9647-119">Requesting migration from Microsoft</span></span>

<span data-ttu-id="d9647-120">Lagring for eksisterende valutakolonner i Dataverse kan ikke støtte flere enn fire desimalplasser.</span><span class="sxs-lookup"><span data-stu-id="d9647-120">Storage for existing currency columns in Dataverse can't support more than four decimal places.</span></span> <span data-ttu-id="d9647-121">I løpet av migreringsprosessen kopieres derfor valutaverdier til nye interne kolonner i databasen.</span><span class="sxs-lookup"><span data-stu-id="d9647-121">Therefore, during the migration process, currency values are copied to new internal columns in the database.</span></span> <span data-ttu-id="d9647-122">Denne prosessen skjer kontinuerlig til alle data er migrert.</span><span class="sxs-lookup"><span data-stu-id="d9647-122">This process occurs continuously until all data has been migrated.</span></span> <span data-ttu-id="d9647-123">Internt, på slutten av migreringen, erstatter de nye lagringstypene de gamle lagringstypene, men dataverdiene er uendret.</span><span class="sxs-lookup"><span data-stu-id="d9647-123">Internally, at the end of migration, the new storage types replace the old storage types, but the data values are unchanged.</span></span> <span data-ttu-id="d9647-124">Valutakolonnene kan da støtte opptil 10 desimalplasser.</span><span class="sxs-lookup"><span data-stu-id="d9647-124">The currency columns can then support up to 10 decimal places.</span></span> <span data-ttu-id="d9647-125">Under migreringsprosessen kan Dataverse fortsatt brukes uten avbrudd.</span><span class="sxs-lookup"><span data-stu-id="d9647-125">During the migration process, Dataverse can continue to be used without interruption.</span></span>

<span data-ttu-id="d9647-126">Samtidig endres valutakursene, slik at de støtter opptil 12 desimalplasser i stedet for den gjeldende grensen på 10.</span><span class="sxs-lookup"><span data-stu-id="d9647-126">At the same time, exchange rates are modified so that they support up to 12 decimal places instead of the current limit of 10.</span></span> <span data-ttu-id="d9647-127">Denne endringen er nødvendig, slik at antall desimaler er det samme i både Finance and Operations-appen og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d9647-127">This change is required so that the number of decimal places is the same in both the Finance and Operations app and Dataverse.</span></span>

<span data-ttu-id="d9647-128">Migreringen endrer ikke data.</span><span class="sxs-lookup"><span data-stu-id="d9647-128">Migration doesn't change any data.</span></span> <span data-ttu-id="d9647-129">Når kolonnene for valuta og valutakurs er konvertert, kan administratorer konfigurere systemet til å bruke opptil 10 desimaler for valutakolonner ved å angi antall desimalplasser for hver transaksjonsvaluta og for prissetting.</span><span class="sxs-lookup"><span data-stu-id="d9647-129">After the currency and exchange rate columns are converted, admins can configure the system to use up to 10 decimal places for currency columns by specifying the number of decimal places for each transaction currency and for pricing.</span></span>

### <a name="request-a-migration"></a><span data-ttu-id="d9647-130">Be om en migrering</span><span class="sxs-lookup"><span data-stu-id="d9647-130">Request a migration</span></span>

<span data-ttu-id="d9647-131">Hvis du vil gjøre denne funksjonen tilgjengelig, send en e-post til **CDSExpandDecimal@microsoft.com**, og inkluder følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="d9647-131">To make this feature available, email **CDSExpandDecimal@microsoft.com**, and include the following information:</span></span>

+ <span data-ttu-id="d9647-132">**Emne:** Forespørsel om å aktivere utvidet desimalstøtte for \<organizationID\></span><span class="sxs-lookup"><span data-stu-id="d9647-132">**Subject:** Request to enable expanded decimal support for \<organizationID\></span></span>
+ <span data-ttu-id="d9647-133">**Tekst:** Jeg vil aktivere utvidet støtte for desimaler i organisasjonen min \<organizationID\>.</span><span class="sxs-lookup"><span data-stu-id="d9647-133">**Body:** I would like to enable expanded decimal support for my org \<organizationID\>.</span></span>

<span data-ttu-id="d9647-134">En Microsoft-representant vil kontakte deg innen to til tre arbeidsdager for de neste trinnene.</span><span class="sxs-lookup"><span data-stu-id="d9647-134">A Microsoft representative will contact you within two to three business days for the next steps.</span></span>

<span data-ttu-id="d9647-135">Når du ber om en migrering, bør du være oppmerksom på følgende detaljer og planlegge dem i henhold til følgende:</span><span class="sxs-lookup"><span data-stu-id="d9647-135">When you request a migration, you should be aware of the following details and plan for them accordingly:</span></span>

+ <span data-ttu-id="d9647-136">Tiden som kreves for å migrere dataene, avhenger av mengden data i systemet.</span><span class="sxs-lookup"><span data-stu-id="d9647-136">The time that is required to migrate the data depends the amount of data in the system.</span></span> <span data-ttu-id="d9647-137">Migrering av store databaser kan ta flere dager.</span><span class="sxs-lookup"><span data-stu-id="d9647-137">Migration of large databases can take several days.</span></span>
+ <span data-ttu-id="d9647-138">Størrelsen på databasen øker midlertidig mens migreringen kjøres, fordi det kreves ekstra plass til indekser.</span><span class="sxs-lookup"><span data-stu-id="d9647-138">The size of the database temporarily increases while the migration is running, because additional space is needed for indexes.</span></span> <span data-ttu-id="d9647-139">Det meste av den ekstra plassen frigjøres når migreringen er fullført.</span><span class="sxs-lookup"><span data-stu-id="d9647-139">Most of the additional space is freed when the migration is completed.</span></span>
+ <span data-ttu-id="d9647-140">Hvis det under migreringsprosessen oppstår feil som hindrer migreringen fra å bli fullført, sender systemet varsler til Microsoft kundestøtte, slik at støttepersonale kan settes inn.</span><span class="sxs-lookup"><span data-stu-id="d9647-140">During the migration process, if errors occur that prevent the migration from being completed, the system raise alerts to Microsoft Support, so that Support staff can intervene.</span></span> <span data-ttu-id="d9647-141">Selv om det oppstår feil under migreringen, forblir imidlertid Dataverse fullstendig tilgjengelig for vanlig bruk.</span><span class="sxs-lookup"><span data-stu-id="d9647-141">However, even if errors occur during the migration, Dataverse remains fully available for regular use.</span></span>
+ <span data-ttu-id="d9647-142">Migreringsprosessen er ikke reversibel.</span><span class="sxs-lookup"><span data-stu-id="d9647-142">The migration process isn't reversible.</span></span>

## <a name="changing-the-number-of-decimal-places"></a><span data-ttu-id="d9647-143">Endre antall desimaler</span><span class="sxs-lookup"><span data-stu-id="d9647-143">Changing the number of decimal places</span></span>

<span data-ttu-id="d9647-144">Når migreringen er fullført, kan Dataverse lagre numre som har flere desimaler.</span><span class="sxs-lookup"><span data-stu-id="d9647-144">After the migration is completed, Dataverse can store numbers that have more decimal places.</span></span> <span data-ttu-id="d9647-145">Administratorer kan velge hvor mange desimaler som brukes for bestemte valutakoder og for prissetting.</span><span class="sxs-lookup"><span data-stu-id="d9647-145">Admins can choose how many decimal places are used for specific currency codes and for pricing.</span></span> <span data-ttu-id="d9647-146">Brukere av Microsoft Power Apps, Power BI og Power Automate kan deretter vise og bruke tall som har flere desimaler.</span><span class="sxs-lookup"><span data-stu-id="d9647-146">Users of Microsoft Power Apps, Power BI, and Power Automate can then view and use numbers that have more decimal places.</span></span>

<span data-ttu-id="d9647-147">Hvis du vil utføre denne endringen, må du oppdatere følgende innstillinger i Power Apps:</span><span class="sxs-lookup"><span data-stu-id="d9647-147">To make this change, you must update the following settings in Power Apps:</span></span>

+ <span data-ttu-id="d9647-148">**Systeminnstillinger: Valutapresisjon for prissetting** – Kolonnen **Sett valutapresisjonen som brukes for prissetting i hele systemet** definerer hvordan valutaen vil fungere i organisasjonen når **Prissettingspresisjon** er valgt.</span><span class="sxs-lookup"><span data-stu-id="d9647-148">**System Settings: Currency precision for pricing** – The **Set the currency precision that is used for pricing throughout the system** column defines how the currency will behave for the organization when **Pricing Precision** is selected.</span></span>
+ <span data-ttu-id="d9647-149">**Forretningsstyring: Valutaer** – Med kolonnen **Valutapresisjon** kan du angi et egendefinert antall desimalplasser for en bestemt valuta.</span><span class="sxs-lookup"><span data-stu-id="d9647-149">**Business Management: Currencies** – The **Currency Precision** column lets you specify a custom number of decimal places for a specific currency.</span></span> <span data-ttu-id="d9647-150">Det er et tilbakefall til innstillingen for hele organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="d9647-150">There is a fallback to the organization-wide setting.</span></span>

<span data-ttu-id="d9647-151">Det er noen av begrensninger:</span><span class="sxs-lookup"><span data-stu-id="d9647-151">There are some limitations:</span></span>

+ <span data-ttu-id="d9647-152">Du kan ikke konfigurere valutakolonnen i en tabell.</span><span class="sxs-lookup"><span data-stu-id="d9647-152">You can't configure the currency column on a table.</span></span>
+ <span data-ttu-id="d9647-153">Du kan angi mer enn fire desimalplasser bare på nivåene **Prissetting** og **Transaksjonsvaluta**.</span><span class="sxs-lookup"><span data-stu-id="d9647-153">You can specify more than four decimal places only at the **Pricing** and **Transaction Currency** levels.</span></span>

### <a name="system-settings-currency-precision-for-pricing"></a><span data-ttu-id="d9647-154">Systeminnstillinger: Valutapresisjon for prissetting</span><span class="sxs-lookup"><span data-stu-id="d9647-154">System Settings: Currency precision for pricing</span></span>

<span data-ttu-id="d9647-155">Når migreringen er fullført, kan administratorer angi valutapresisjonen.</span><span class="sxs-lookup"><span data-stu-id="d9647-155">After migration is completed, admins can set the currency precision.</span></span> <span data-ttu-id="d9647-156">Gå til **Innstillinger \> Administrasjon**, og velg **Systeminnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="d9647-156">Go to **Settings \> Administration**, and select **System Settings**.</span></span> <span data-ttu-id="d9647-157">I **Generelt**-fanen endrer du verdien for kolonnen **Sett valutapresisjonen som brukes for prissetting i hele systemet**, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="d9647-157">Then, on the **General** tab, change the value of the **Set the currency precision that is used for pricing throughout the system** column, as shown in the following illustration.</span></span>

![Systeminnstillinger for valuta](media/currency-system-settings.png)

### <a name="business-management-currencies"></a><span data-ttu-id="d9647-159">Forretningsstyring: Valutaer</span><span class="sxs-lookup"><span data-stu-id="d9647-159">Business Management: Currencies</span></span>

<span data-ttu-id="d9647-160">Hvis du krever at valutapresisjonen for en bestemt valuta er forskjellig fra valutapresisjonen som brukes til prissetting, kan du endre den.</span><span class="sxs-lookup"><span data-stu-id="d9647-160">If you require that the currency precision for a specific currency differ from the currency precision that is used for pricing, you can change it.</span></span> <span data-ttu-id="d9647-161">Gå til **Innstillinger \> Forretningsstyring**, velg **Valutaer**, og velg valutaen som skal endres.</span><span class="sxs-lookup"><span data-stu-id="d9647-161">Go to **Settings \> Business Management**, select **Currencies**, and select the currency to change.</span></span> <span data-ttu-id="d9647-162">Deretter setter du **Valutapresisjon**-kolonnen til ønsket antall desimalplasser, som vist i følgende illustrasjon.</span><span class="sxs-lookup"><span data-stu-id="d9647-162">Then set the **Currency Precision** column to the number of decimal places that you want, as shown in the following illustration.</span></span>

![Valutainnstillinger for en bestemt nasjonal innstilling](media/specific-currency.png)

### <a name="tables-currency-column"></a><span data-ttu-id="d9647-164">tabeller: Valuta-kolonne</span><span class="sxs-lookup"><span data-stu-id="d9647-164">tables: Currency column</span></span>

<span data-ttu-id="d9647-165">Antallet desimaler som kan konfigureres for bestemte valutakolonner, er begrenset til fire.</span><span class="sxs-lookup"><span data-stu-id="d9647-165">The number of decimal places that can be configured for specific currency columns is limited to four.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]