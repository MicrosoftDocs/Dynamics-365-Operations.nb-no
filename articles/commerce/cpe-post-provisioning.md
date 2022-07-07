---
title: Konfigurere et Dynamics 365 Commerce-sandkassemiljø
description: Denne artikkelen forklarer hvordan du konfigurerer Microsoft Dynamics 365 Commerce-sandkassemiljø etter klargjøring.
author: psimolin
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 259a580981003f135e234f66e9e93ceb18605412
ms.sourcegitcommit: 252cb41c3029b623354698463f7b44a29fd9f184
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013115"
---
# <a name="configure-a-dynamics-365-commerce-sandbox-environment"></a>Konfigurere et Dynamics 365 Commerce-sandkassemiljø

[!include [banner](includes/banner.md)]

Denne artikkelen forklarer hvordan du konfigurerer Microsoft Dynamics 365 Commerce-sandkassemiljø etter klargjøring.

Fullfør fremgangsmåtene i denne artikkelen bare etter at Commerce-sandkassemiljøet er klargjort. Hvis du vil ha informasjon om hvordan du klargjør Commerce-sandkassemiljøet, kan du se [Klargjøre et Commerce-sandkassemiljø](provisioning-guide.md).

Etter at Commerce-sandkassemiljøet er klargjort ende til ende, må du fullføre flere trinn etter klargjøring før du kan begynne å bruke miljøet. Hvis du vil fullføre disse trinnene, må du bruke Microsoft Dynamics Lifecycle Services (LCS, ) og Dynamics 365 Commerce.

## <a name="before-you-start"></a>Før du starter

1. Logg på [LCS-portalen](https://lcs.dynamics.com).
1. Gå til prosjektet.
1. Velg miljøet fra listen.
1. Velg **Logg på miljøet** i miljøinformasjonen til høyre. Du vil bli sendt til Commerce Headquarters.
1. Kontroller at den juridiske enheten **USRT** er valgt i øvre høyre hjørne. Denne juridiske enheten er forhåndskonfigurert i demodataene.
1. Gå til **Handelsparametere \> Konfigurasjonsparametere** og kontroller at det finnes en oppføring for **ProductSearch.UseAzureSearch**, og at **true** er angitt for verdien. Hvis denne oppføringen mangler, legger du den til og angir **sann** for verdien.
1. Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Handelsplanlegger \> Initialiser handelsplanlegger**. På undermenyen **Initialiser handelsplanlegger** kontrollerer du at alternativet **Slett eksisterende konfigurasjon** er satt til **Ja** og velger deretter **OK**.
1. Butikk- og e-handelskanalene må legges til i Commerce Scale Unit for at de skal kunne fungere riktig. Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Handelsplanlegger \> Kanaldatabase**, og velg deretter Commerce Scale Unit i venstre rute. Legg til kanalene **AW-nettbutikk**, **AW-nettbutikk for bedrifter** og **Fabrikam-utvidet nettbutikk** i hurtigfanen **Detaljhandelskanal** hvis du har tenkt å bruke disse e-handelskanalene. Du kan eventuelt også legge til detaljhandelsbutikker hvis du skal bruke salgssted (for eksempel **Seattle**, **San Francisco** og/eller **San Jose**).
1. Du kan sikre at alle endringer synkroniseres med kanaldatabasen, ved å velge **Kanaldatabase \> Fullstendig datasynkronisering** for Commerce Scale Unit.

Under aktiviteter etter klargjøring i Commerce Headquarters må du kontrollere at den juridiske enheten **USRT** alltid er valgt.

## <a name="configure-the-point-of-sale"></a>Konfigurere salgsstedet

### <a name="associate-a-worker-with-your-identity"></a>Knytt en arbeider til din identitet

Hvis du vil knytte en arbeider med identiteten din i Commerce Headquarters, følger du denne fremgangsmåten.

1. Bruk menyen til venstre, og gå til **Moduler \> Retail og Commerce \> Ansatte \> Arbeidere**.
1. Finn og velg følgnede post i listen **000713 - Andrew Collette**. Denne eksempelbrukeren er knyttet til butikken i San Francisco som skal brukes i neste del.
1. Klikk **Commerce** i handlingsruten.
1. Velg **Tilknytt eksisterende ID**.
1. I feltet **E-post** (til høyre for **Søk ved hjelp av e-post**) skriver du inn e-postadressen din.
1. Velg **Søk**.
1. Velg posten med navnet ditt.
1. Velg **OK**.
1. Velg **Lagre**.

### <a name="activate-cloud-pos"></a>Aktivere Skysalgssted

Hvis du vil aktivere Cloud POS, følger du denne fremgangsmåten i LCS.

1. Fra den øverste menyen velger du **Skybaserte miljøer**.
1. Velg miljøet fra listen.
1. Velg **Logg på Cloud Point of Sale** i miljøinformasjonen til høyre.
1. Velg **Neste** for å åpne dialogboksen **Før du starter**.
1. La **Server-URL**-feltet være slik det er. Velg **Neste**.
1. Logg på ved hjelp av Microsoft Azure Active Directory (Azure AD)-kontoen din.
1. Under **Butikknavn** velger du **San Francisco**, og deretter velger du **Neste**.
1. Under **Register og enhet** velger du **SANFRAN-1**.
1. Velg **Aktiver**. Du er logget av og tatt til påloggingssiden for salgsstedet.
1. Du kan nå logge på Cloud POS-opplevelsen ved hjelp av operatør-ID-en **000713** og passordet **123**.

## <a name="set-up-your-e-commerce-sites"></a>Konfigurere e-handelsområdene

Det finnes tre demonstrasjonsområder for e-handel: Fabrikam, Adventure Works og Adventure Works Business. Følg trinnene nedenfor for å konfigurere hvert demonstrasjonsområde.

1. Logg på områdebyggeren ved hjelp av URL-adressen du noterte da du startet e-handel under klargjøring (se [Initialisere e-handel](provisioning-guide.md#initialize-e-commerce)).
1. Velg området (**Fabrikam**, **Adventure Works** eller **Adventure Works Business**), for å åpne dialogboksen for områdeoppsett.
1. Velg domenet du angav da du startet Commerce.
1. I Headquarters velger du den forhåndskonfigurerte nettbutikkanalen (**Fabrikam-utvidet nettbutikk**, **AW-nettbutikk** eller **AW-nettbutikk for bedrifter**) som svarer til standardkanalen.
1. Velg **nb-no** for standardspråk.
1. Konfigurer banefeltene. Disse kan stå tomme for et enkeltområde, men må konfigureres hvis du bruker samme domenenavn for flere områder. Hvis domenenavnet for eksempel er `https://www.constoso.com`, kan du bruke en tom bane for Fabrikam (`https://contoso.com`) og deretter bruke «aw» for Adventure Works (`https://contoso.com/aw`) og «awbusiness» for Adventure Works-forretningsområdet (`https://contoso.com/awbusiness`).
1. Velg **OK**. Listen over sider på området vises.
1. Du kan alternativt gjenta trinn 2–7 for å konfigurere de andre demonstrasjonsområdene etter behov.

## <a name="enable-jobs"></a>Aktivere jobber

Følg disse trinnene for å aktivere jobber i Commerce.

1. Logg deg på Headquarters-miljøet.
1. Gå til **Retail og Commerce \> Forespørsler og rapporter \> Satsvise jobber** ved hjelp av menyen til venstre.

    De resterende trinnene i denne prosedyren må fullføres for hver av følgende jobber:

    * Behandle e-postvarsling for detaljistordre
    * Produkttilgjengelighet
    * P-0001
    * Synkroniser ordrejobb

1. Bruk hurtigfilteret til å søke etter jobben ved hjelp av navnet.
1. Hvis statusen for jobben er **Utfører**, utfører du følgende trinn:

    1. Velg posten.
    1. Velg **Endre status** i kategorien **Satsvis jobb** i handlingsruten.
    1. Velg **Avbryt**, og velg deretter **OK**.

1. Hvis statusen for jobben er **Holdt tilbake**, utfører du følgende trinn:

    1. Velg posten.
    1. Velg **Endre status** i kategorien **Satsvis jobb** i handlingsruten.
    1. Velg **Venter**, og velg deretter **OK**.

Du kan også angi et intervall for regelmessighet til ett (1) minutt for følgende jobber:

* Behandle e-postvarslingsjobb for detaljistordre
* P-0001-jobb
* Synkroniser ordrejobb

### <a name="run-full-data-synchronization"></a>Kjøre fullstendig datasynkronisering

Hvis du vil kjøre full datasynkronisering i Commerce, gjør du følgende i Commerce Headquarters.

1. Bruk menyen til venstre og gå til **Moduler \> Retail og Commerce \> Hovedkvarteroppsett \> Handelsplanlegger \> Kanaldatabase**.
1. Velg kanalen med navnet **scXXXXXXXXX**.
1. I handlingsruten velger du **Fullstendig datasynkronisering**.
1. Angi **9999** som distribusjonsplan.
1. Velg **OK**.
1. Velg **OK**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Teste kredittkortinformasjon for å utføre testinnkjøp

Hvis du skal utføre testtransaksjoner på området, kan du bruke denne testkredittkortinformasjonen:

- **Kortnummer:** 4111-1111-1111-1111
- **Utløpsdato:** 10/30
- **Verdi for kortbekreftelse (CVV-kode):** 737

> [!IMPORTANT]
> Du bør ikke prøve å bruke faktisk kredittkortinformasjon på testområdet under noen omstendigheter!

## <a name="next-steps"></a>Neste trinn

Når klargjøringen og konfigurasjonstrinnene er fullført, er du klar til å bruke sandkassemiljøet. Bruk URL-adressen for Commerce-områdebygger for å gå til redigeringsopplevelsen. Bruk URL-adressen for Commerce-området for å gå til kundeområdet for detaljhandel.

Hvis du vil konfigurere valgfrie funksjoner for Commerce-sandkassemiljøet, kan du se [Konfigurere valgfrie funksjoner for et Commerce-sandkassemiljø](cpe-optional-features.md).

Hvis du vil la e-handelsbrukere logge seg på e-handelsområdet, må du foreta ytterligere konfigurasjon for å aktivere områdegodkjenning via bedrift-til-kunde (B2C) i Azure Active Directory. Hvis du vil ha instruksjoner, kan du se [Konfigurere en B2C-leier i Commerce](set-up-b2c-tenant.md).

## <a name="troubleshooting"></a>Feilsøking

### <a name="site-builder-channel-list-is-empty-when-configuring-site"></a>Kanallisten for områdebygger er tom når du konfigurerer et område

Hvis områdebyggeren ikke viser kanaler for nettbutikk, kontrollerer du i hovedkontoret at kanalene er lagt til i Commerce Scale Unit, som beskrevet i delen [Før du starter](#before-you-start) ovenfor. Kjør også **Initialiser handelsplanlegger** med **Ja** angitt for verdien for **Slett eksisterende konfigurasjon**.  Etter at du har fullført disse trinnene, kjører du jobben **9999** på Commerce Scale Unit på **Kanaldatabase**-siden (**Detaljhandel og handel \> Hovedkvarteroppsett \> Handelsplanlegger \> Kanaldatabase**).

### <a name="color-swatches-are-not-rendering-on-the-category-page-but-are-rendering-on-the-product-details-page-pdp-page"></a>Fargeprøver gjengis ikke på kategorisiden, men gjengis på siden for produktdetaljer

Følg denne fremgangsmåten for å sikre at farge- og størrelsesprøver er angitt slik at de kan omdefineres.

1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Kanalkategorier og produktattributter** i hovedkontoret.
1. Velg kanalen for nettbutikk i venstre rute, og velg deretter **Angi attributtmetadata**.
1. Angi **Ja** for alternativet **Vis attributter i kanal**, angi **Ja** for alternativet **Kan justeres**, og velg deretter **Lagre**. 
1. Gå tilbake til kanalsiden for nettbutikk, og velg deretter **Publiser kanaloppdateringer**.
1. Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Handelsplanlegger \> Kanaldatabase**, og kjør **9999**-jobben på Commerce Scale Unit.

### <a name="business-features-dont-appear-to-be-turned-on-for-the-adventureworks-business-site"></a>Det ser ikke ut til at bedriftsfunksjoner er aktivert for området AdventureWorks Bedrift

I hovedkontoret må du sørge for at kanalen for nettbutikk er konfigurert med **B2B** angitt for **Kundetype**. Hvis **B2C** er angitt for **Kundetype**, må det opprettes en ny kanal siden den eksisterende kanalen ikke kan redigeres. 

Demonstrasjonsdata i Commerce versjon 10.0.26 og tidligere hadde en feil der **AW-nettbutikk for bedrifter** var feilkonfigurert. Løsningen er å opprette en ny kanal med de samme innstillingene og konfigurasjonene, bortsett fra at **B2B** må angis for **Kundetype**.

## <a name="additional-resources"></a>Tilleggsressurser

[Klargjøre et Dynamics 365 Commerce-sandkassemiljø](provisioning-guide.md)

[Konfigurere valgfrie funksjoner for et Dynamics 365 Commerce-sandkassemiljø](cpe-optional-features.md)

[Konfigurere BOPIS i et Dynamics 365 Commerce-sandkassemiljø](cpe-bopis.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-nettsted](https://aka.ms/Dynamics365CommerceWebsite)

[Konfigurer en B2C-leier i Commerce](set-up-B2C-tenant.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
