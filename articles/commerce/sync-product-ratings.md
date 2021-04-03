---
title: Synkronisere produktvurderinger i Dynamics 365 Commerce
description: Dette emnet beskriver hvordan du synkroniserer produktvurderinger i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ab6de4bfa619df74bafc5511affddd516bdb34f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260315"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a>Synkronisere produktvurderinger i Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du synkroniserer produktvurderinger i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Hvis du vil bruke produktvurderinger i omnikanaler, for eksempel ved salgsstedet og i telefonsentre, må produktvurderingene fra vurderings- og omtaletjenesten importeres til handelskanaldatabasen. Når produktvurderinger gjøres tilgjengelig i omnikanaler, kan de hjelpe kundene indirekte i løpet av samhandlingen med salgspartnere.

Dette emnet beskriver følgende oppgaver:

1. Konfigurer **Synkroniseringsjobb for produktvurderinger** som en satsvis jobb for å synkronisere produktvurderinger fra **tjenesten for vurderinger og omtaler**.
1. Kontroller at den satsvise jobben for synkronisering av produktvurdering er vellykket.
1. Gjør produktvurderinger tilgjengelige på salgsstedet.

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a>Konfigurere en satsvis jobb for å synkronisere produktvurderinger

> [!IMPORTANT]
> Før du starter må du kontrollere at versjon 10.0.6 eller senere av Dynamics 365 Commerce er installert.

### <a name="initialize-the-commerce-scheduler"></a>Initialisere handelsplanleggeren

Bruk følgende fremgangsmåte for å initialisere handelsplanleggeren.

1. Gå til **Retail og Commerce \> Hovedkvarteroppsett \> Handelsplanlegger \> Initialiser handelsplanlegger**. Du kan også søke etter "Initialiser handelsplanlegger".
1. I dialogboksen **Initialiser handelsplanlegger** kontrollerer du at alternativet **Slett eksisterende konfigurasjon** er satt til **Nei**, og deretter velger du **OK**.

### <a name="verify-the-retailproductrating-subjob"></a>Kontrollere RetailProductRating-deljobben

Følg denne fremgangsmåten for å kontrollere at **RetailProductRating**-deljobben finnes.

1. Gå til **Retail og Commerce \> Hovedkvarteroppsett \> Handelsplanlegger \> Deljobber i planlegger**. Du kan også søke etter "Deljobber i planlegger".
1. I listen over deljobber finner eller søker du etter deljobben **RetailProductRating**.

Illustrasjonen nedenfor viser et eksempel på deljobbdetaljer i Commerce.

![Detaljer i RetailProductRating-deljobben](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> Hvis du ikke finner deljobben **RetailProductRating** kan det hende at du allerede har kjørt jobben **Synkroniser produktvurderinger** og jobben **1040 CDX** før du initialiserte handelsplanleggeren. I dette tilfellet følger du denne fremgangsmåten for å kjøre jobben **Fullstendig datasynkronisering**.

> 1. Gå til **Retail og Commerce \> Hovedkvarteroppsett \> Handelsplanlegger \> Kanaldatabase**. Du kan også søke etter "kanaldatabase".
> 1. Velg kanaldatabasen som skal synkroniseres.
> 1. I handlingsruten velger du **Fullstendig datasynkronisering**.
> 1. I rullegardinboksen **Velg en distribusjonsplan** velger du **1040 – produkter**, og deretter velger du **OK**.
> 1. Gjenta trinnene for den forrige prosedyren for å kontrollere at deljobben **RetailProductRating** er opprettet.

### <a name="import-product-ratings"></a>Importere produktvurderinger

Følg denne fremgangsmåten for å importere produktvurderinger til Commerce fra vurderings- og omtaletjenesten:

1. Gå til **Retail og Commerce \> Hovedkvarteroppsett \> Handelsplanlegger \> Synkroniser produktvurderinger-jobb**. Du kan også søke etter "Synkroniser produktvurderinger-jobb".
1. I dialogboksen **Hent produktvurderinger** i hurtigfanen **Kjør i bakgrunnen** velger du **Regelmessighet**.
1. Angi et gjentakende mønster i dialogboksen **Definer regelmessighet** . (Den foreslåtte verdien er to timer.) Ikke planlegg en regelmessighet som er mindre enn én time.
1. Velg **OK**.
1. Sett alternativet **Partiprosess** til **Ja**. Denne innstillingen hjelper deg med å kontrollere at du kan overvåke loggene og kontrollere at statusen til de satsvise jobbene kjøres.
1. Velg **OK** for å planlegge den satsvise jobben.

Illustrasjonen nedenfor viser et eksempel på konfigurasjon av satsvis jobb i Commerce.

![Konfigurasjon av den satsvise jobben for synkroniserings produktvurderinger](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a>Kontrollere at den satsvise jobben for synkronisering av produktvurdering er vellykket

Følg denne fremgangsmåten for å kontrollere at den satsvise jobben for **Synkroniser produktvurderinger** er fullført.

1. Gå til **Retail og Commerce \> Systemansvarlig \> Forespørsler \> Satsvise jobber** eller, hvis du bruker en Commerce-spesifikk SKU, går du til **Retail og Commerce \> Forespørsler og rapporter \> Satsvise jobber** i stedet. Du kan også søke etter "Satsvise jobber".
1. Hvis du vil vise detaljene for den satsvise jobben, kan du gå til kolonnen **Jobbeskrivelse** i listen over satsvise jobber og søke etter en beskrivelse som inneholder "Hent produktvurderinger".
1. Velg jobb-ID for å vise detaljene for de satsvise jobbene, for eksempel planlagt startdato/-klokkeslett og teksten for regelmessighet.

Følgende illustrasjon viser et eksempel på detaljene for den satsvise jobben i Commerce når den satsvise jobben er planlagt å kjøres med totimersintervaller.

![Detaljer for den satsvise jobben for synkronisering av produktvurderinger](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a>Gjør produktvurderinger tilgjengelige på salgsstedet

Vurderings- og omtaleløsningen i Dynamics 365 Commerce er en omnikanalløsning. Produktvurderinger vises imidlertid ikke som standard på salgsstedet. Hvis du vil hjelpe kunder i butikker med å se vurderinger og omtaler når de blir hjulpet av salgsmedarbeidere, må du slå på produktvurderinger på salgsstedet.

Følg denne fremgangsmåten for å slå på produktvurderinger på salgsstedet:

1. Gå til **Retail og Commerce \> Handelsoppsett \> Parametere \> Handelsparametere**. Du kan også søke etter "Handelsparametere".
1. Velg **Ny** i kategorien **Konfigurasjonsparametre**.
1. Skriv inn et navn, for eksempel **VurderingerOgOmtaler.AktiverProduktvurderingerForDetaljhandelsbutikker**, og sett verdien til **Sann**.
1. Velg **Lagre**.
1. Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**. Alternativt kan du søke etter "Distribusjonsplan".
1. Velg **1110** i jobblisten (**Global konfigurasjon**), og velg deretter **Kjør nå**.
1. Når jobben er kjørt uten problemer, må du kontrollere at produktvurderingene nå vises på salgsstedet.

Følgende illustrasjon viser et eksempel på konfigurasjon av handelsparametere for å slå på produktvurderinger på salgsstedet.

![Konfigurasjon av handelsparametere for produktvurderinger på salgsstedet](media/rnr-hq-enable-ratings-in-pos.png)

Illustrasjonen nedenfor viser et eksempel på produktvurderinger på salgsstedet.

![Produktvurderinger på salgsstedet](media/rnr-pos-catalog-ratings.png)

Illustrasjonen nedenfor viser et eksempel på produktvurderinger i telefonsenterkanaler.

![Produktvurderinger i en telefonsenterkanal](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over vurderinger og anmeldelser](ratings-reviews-overview.md)

[Velge å bruke vurderinger og anmeldelser](opt-in-ratings-reviews.md)

[Administrere vurderinger og anmeldelser](manage-reviews.md)

[Konfigurere vurderinger og anmeldelser](configure-ratings-reviews.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]