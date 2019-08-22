---
title: Aktivatyper
description: Dette emnet forklarer hvordan du oppretter aktivatyper i Aktivastyring. Det beskriver også elementene som er relatert til aktivatyper.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 288dac77f9d999012ec930ef2bca5c0921c2955f
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783494"
---
# <a name="asset-types"></a>Aktivatyper

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Dette emnet forklarer hvordan du oppretter aktivatyper. Det beskriver også elementene som er relatert til aktivatyper. Aktivatyper brukes som generelle kategorier for aktiva. Eksempler inkluderer CNC-maskiner, måleutstyr og lastebilmotorer. Aktivatyper brukes til å administrere jobbtypene (vedlikeholdsoppgaver), livsløpstilstander for aktiva, aktivamål, aktivaattributter, maler for tilstandsvurdering og aktivamodeller som kan velges for et aktivum. Når du oppretter et aktivum, må du angi type.

For hver aktivatype kan varianter av aktivatypeoppsettet opprettes. Hvis du for eksempel har en aktivatype som heter **Lastebiler**, kan du opprette varianter av denne aktivatypen for forskjellige aktivaprodusenter og aktivamodeller. For hvert oppsett av aktivatype kan du legge til de nødvendige reservedels- og vedlikeholdsplanene.

Først definerer du de nødvendige aktivatypene. Deretter oppretter du aktivamodellene som skal være knyttet til aktivatypene. På siden **Standarder for aktivatype** oppretter du til slutt alle variantene av aktivatyper som kreves for utstyret.

## <a name="create-an-asset-type"></a>Opprette en aktivatype

1. Velg **Aktivastyring** \> **Oppsett** \> **Aktivatyper** \> **Aktivatyper**.
2. Velg **Ny** for å opprette en aktivatype.
3. I **Aktivatype**-feltet angir du en ID for aktivatype.
4. Angi et navn i **Navn**-feltet.
5. Velg en livsløpsmodell for aktivumet i feltet **Livsløpsmodell for aktiva**. Hvis du vil ha mer informasjon om livsløpstilstander og livsløpsmodeller for aktiva, kan du se [Livsløpstilstander for aktiva](object-stages.md).
6. Angi **Total**-alternativet til **Ja** hvis oppsummerte KPI-verdier skal beregnes for aktiva som har denne aktivatypen.
7. Velg **Lagre**.
8. I hurtigfanen **Jobbtyper** velger du jobbtypene som skal relateres til aktivatypen.

    - Hvis du vil velge en jobbtype, velger du den i feltet **Gjenværende jobbtyper**, og deretter velger du pil høyre ![Pil høyre](media/29-setup-for-objects.png) for å flytte den til delen **Valgte jobbtyper**.
    - Hvis du vil velge alle tilgjengelige jobbtyper, velger du ![Videresend alle-pilknappen](media/30-setup-for-objects.png). Alle jobbtyper overføres fra feltet **Gjenværende jobbtyper** til feltet **Valgte jobbtyper**.
    - Hvis du vil avbryte valget av en jobbtype, velger du den i feltet **Valgte jobbtyper**, og deretter velger du pil venstre ![Pil venstre](media/31-setup-for-objects.png) for å flytte den til feltet **Gjenværende jobbtyper**.

9. Du kan også velge aktivamålene som skal være knyttet til aktivatypen. På hurtigfanen **Aktivamål** foretar du valg ved hjelp av metodene som er beskrevet for jobbtyper i trinn 8. Hvis du vil ha mer informasjon om oppsettet av aktivamål, se [Mål av vedlikeholdsgjenstand](counters.md).
10. Du kan også velge attributtypene som skal være knyttet til aktivatypen. På hurtigfanen **Attributtyper** foretar du valg ved hjelp av metodene som er beskrevet for jobbtyper i trinn 8. Hvis du vil opprette den foretrukne sekvensen med attributtverdier, velger du en attributtype i feltet **Valgte attributtyer** og bruker pil opp og pil ned til å flytte den. Sekvensen av attributtyper vises på aktiva som bruker denne aktivatypen. Hvis du vil ha mer informasjon om aktivaattributter, se [Vedlikeholdsattributtyper](../setup-for-functional-locations/specification-types.md).

    > [!NOTE]
    > Når du legger til nye attributtyper på hurtigfanen **Attributtyper**, oppdateres eksisterende aktiva automatisk med denne informasjonen.

11. Du kan også velge malene for tilstandsvurdering som skal være knyttet til aktivatypen. På hurtigfanen **Tilstandsvurderinger** foretar du valg ved hjelp av metodene som er beskrevet for jobbtyper i trinn 8. Hvis du vil ha mer informasjon om maler og registreringer for tilstandsvurdering, se [Tilstandsvurdering](../setup-for-objects/condition-assessment.md).
12. Hurtigfanen **Aktivamodell** viser alle kombinasjonene av aktivaprodusenter og -modeller som er definert for den valgte aktivatypen. Hvis du vil se kombinasjonene som er delt i henhold produsent, velger du **Aktivamodell** for å åpne **Aktivamodell**-siden.

    På siden **Aktivamodell** kan du legge til relasjoner for aktivamodell – aktivatype. På siden **Aktivatyper** kan du også legge til relasjoner for aktivaprodusent – aktivamodell direkte for en aktivatype. På siden **Aktivamodell** (**Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Aktivamodell**) kan du opprette nye relasjoner for aktivaprodusent – aktivamodell – aktivatype. Derfor er det tre måter å definere og redigere relasjoner for aktivaprodusent – aktivamodell – aktivatype. Alle tilgjengelige kombinasjoner vises fra ulike perspektiver, og du kan velge ditt foretrukne inngangspunkt når du arbeider med oppsettet.

> [!NOTE]
> - Hvis du velger aktivamål på en aktivatype, oppdateres valgene automatisk på siden **Aktivamål** (**Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Aktivatyper** \> **Aktivamål**).
> - Feltene i **Detaljer**-delen i hurtigfanen **Generelt** viser antall jobbtyper, aktivamål, attributter og så videre, som er definert for den valgte aktivatypen.

Vanligvis er arbeidsordrer som opprettes manuelt, knyttet til korrigerende vedlikehold, mens arbeidsordrer som opprettes automatisk, er knyttet til forebyggende vedlikehold. Når du oppretter arbeidsordrer manuelt, kan bare jobbtyper som er valgt på hurtigfanen **Jobbtyper** på siden **Aktivatyper** brukes. Automatisk opprettede arbeidsordrer kan imidlertid bruke alle jobbtypene du oppretter på siden **Jjobbtyper** (**Aktivastyring** \> **Oppsett** \> **Jobber** \> **Jobbtyper**).

## <a name="create-asset-type-setup-lines"></a>Opprett oppsettslinjer for aktivatype

1. Velg **Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Aktivatyper** \> **Oppsett av aktivatype**. Alternativt kan du velge **Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Aktivatyper** \> **Aktivatyper**, velge en aktivatype og deretter velge **Oppsett av aktivatype**.
2. Første gang du bruker siden **Oppsett av aktivatype**, kan knappen **Opprett kombinasjoner** være nyttig. Du kan bruke denne knappen til raskt å opprette alle kombinasjoner av en aktivamodell på en aktivatype. Velg **Opprett kombinasjoner**, velg aktivatypen du vil opprette kombinasjoner for, og velg deretter **OK**.

    > [!NOTE]
    > Hvis du ikke vil bruke alle kombinasjonene av oppsettet av aktivatype som ble opprettet automatisk, kan du slette et oppsett ved å merke det og deretter velge **Slett**.

3. Velg **Ny** for å opprette et oppsett av aktivatype manuelt.
4. Avhengig av hvor spesifikt oppsettet av aktivatypen skal være, må du gjøre valg i feltene **Aktivatype**, **Produsent** og **Modell**.
5. Hvis en garantiavtale er knyttet til aktivatypen, velger du avtalen i feltene **Leverandørgaranti** og **Kundegaranti**. 
6. I hurtigfanen **Reservedeler** velger du **Legg til** for å legge til reservedeler i det valgte oppsettet for aktivatype.
7. Hvis du vil godkjenne en reservedel, velger du reservedelslinjen og velger deretter **Godkjenn**. Du kan velge flere linjer for godkjenning.
8. Hvis du vil se om en reservedel brukes et annet sted i aktivastyring (for eksempel i forbindelse med aktiva og arbeidsordrer), velger du reservedelslinjen og velger deretter **Vare der brukt** for å åpne siden **Vare der brukt**. Hvis du vil vise alle aktive reservedeler i listen, merker du av for **Aktiv**. Hvis du bare vil se godkjente reservedeler, merker du av for **Godkjent**.
9. I hurtigfanen **Vedlikeholdsplaner** velger du **Legg til** for å legge til vedlikeholdsplaner i det valgte oppsettet for aktivatype.
10. Hvis du vil kopiere et oppsett av aktivatype til et annet oppsett, kan du bruke funksjonen Kopier. Velg oppsettet for aktivatype der du vil kopiere et oppsett, velg **Kopier oppsett**, og velg oppsettet av aktivatype som oppsettet skal kopieres fra. Innstillingene for de ulike alternativene bestemmer hvor mye informasjon som er inkludert. Når du er ferdig, velger du **OK** for å kopiere oppsettet.

> [!NOTE]
> Hvis du har mange reservedelslinjer og vedlikeholdsplanlinjer som du vil bruke på nytt, lar kopieringsfunksjonen deg raskt og enkelt sette opp data for mange kombinasjoner av oppsett av aktivatype.

## <a name="spare-parts-on-the-asset-type-setup"></a>Reservedeler på oppsettet av aktivatype

Som beskrevet i delen "Opprett oppsettslinjer for aktivatype" er reservedeler definert på aktivamodeller på siden **Oppsett av aktivatype**. Derfor, når du åpner siden **Oppsett av aktivatype**, ser du bare reservedeler som er knyttet til den valgte kombinasjonen av en aktivatype, aktivaprodusent og aktivamodell. Hvis du vil se en liste over alle reservedelspostene, åpner du **Reservedeler**-siden (**Aktivastyring** \> **Forespørsler** \> **Reservedeler**).

På siden **Reservedeler** kan du også opprette nye reservedeler for eksisterende kombinasjoner av en aktivatype, aktivaprodusent og aktivamodell. Du kan bestemme om du foretrekker å opprette reservedelsposter på siden **Oppsett av aktivatype** eller siden **Reservedeler**. Siden **Oppsett av aktivatype** gir en oversikt over data om den valgte kombinasjonen av en aktivatype, aktivaprodusent og aktivamodell, mens siden **Reservedeler** gir en fullstendig oversikt over alle oppsettslinjer for aktivatype. Hvis siden **Reservedeler** inneholder mange poster, kan siden **Oppsett av aktivatype** gi deg en bedre oversikt.

Hvis du vil se om reservedelen på den valgte linejn brukes et annet sted i Aktivastyring (for eksempel i forbindelse med aktiva og arbeidsordrer), velger du **Vare der brukt** for å åpne siden **Vare der brukt**. 

