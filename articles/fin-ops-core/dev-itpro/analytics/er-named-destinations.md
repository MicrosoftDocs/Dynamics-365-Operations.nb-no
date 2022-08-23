---
title: Konfigurere postspesifikke ER-mål for utskriftsbehandling
description: Denne artikkelen forklarer hvordan du konfigurerer postspesifikke mål for utskriftsbehandling for et ER-format (Elektronisk rapportering) som er konfigurert til å generere utgående dokumenter.
author: kfend
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: 10.0.21
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.form: ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 7c92d580f6adebdba12b7964a42fd4752e9c9205
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285069"
---
# <a name="configure-print-management-record-specific-er-destinations"></a>Konfigurere postspesifikke ER-mål for utskriftsbehandling

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan en bruker i rollen systemansvarlig eller regnskapsmedarbeider kan utføre følgende oppgaver:

- Konfigurer navngitte [ER-mål (elektronisk rapportering)](general-electronic-reporting.md) for en ER-løsning som genererer fritekstfakturaer.
- Tilordne et ER-mål til en enkelt [utskriftsbehandlingspost](document-reporting-services.md).

Prosedyrene kan fullføres i firmaet USMF. Ingen koding er nødvendig.

## <a name="introduction"></a>Innledning

Du kan konfigurere [mål](electronic-reporting-destinations.md) for hver mappe i [konfigurasjonen](general-electronic-reporting.md#Configuration) av filutdatakomponenten for et ER-[format](general-electronic-reporting.md) som brukes til å generere et utgående dokument. Når du kjører et ER-format av denne typen og har nødvendige tilgangsrettigheter, kan du også endre de konfigurerte målinnstillingene ved kjøretid.

I Microsoft Dynamics 365 Finance **versjon 10.0.17 og nyere** kan en handlingskode [defineres](er-apis-app10-0-17.md) for et ER-format for å angi handlingen som brukerne utfører ved å kjøre dette ER-formatet. I **Kunder**-modulen i innstillingene for utskriftsbehandling kan du for eksempel velge et ER-format som genererer et bestemt forretningsdokument, for eksempel en fritekstfaktura. Du kan deretter velge **Vis** for å forhåndsvise fakturaen eller **Skriv ut** for å sende den til en skriver. Hvis en handling sendes for det kjørende ER-formatet ved kjøretid, kan du [konfigurere ulike ER-mål for ulike brukerhandlinger](er-action-dependent-destinations.md).

I Finance **versjon 10.0.21 og senere** kan et navngitt mål [defineres](er-apis-app10-0-21.md) for et ER-format og tilordnes til utskriftsbehandlingsposten som behandles når dette ER-formatet kjøres. I **Kunder**-modulen, i innstillingene for utskriftsbehandling, kan du for eksempel konfigurere **Original**-posten til å utføre følgende handlinger:

- Kjør et ER-format.
- Send den genererte fakturaen til en kunde via e-post.
- Konfigurer **Kopier**-posten til å kjøre det samme formatet.
- Skriv ut en kopi av fakturaen til en nettverksskriver.

I dette tilfellet må du konfigurere forskjellige ER-mål for ER-formatet som kjører, og du må velge mål for forskjellige utskriftsbehandlingsposter.

## <a name="prerequisites"></a>Forutsetninger

Før du kan begynne, må funksjonen **Tillat konfigurasjon av ER-mål per utskriftsbehandlingselement** være aktivert i arbeidsområdet [Funksjonsbehandling](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace). Kildekoden må også endres for å tillate konfigurasjon av navngitte ER-mål i gjeldende Finance-forekomst og for å aktivere den [nye](er-apis-app10-0-21.md) ER-API-en.

I tillegg må ER-konfigurasjonen for **Fritekstfaktura (Excel)** [importeres](er-download-configurations-global-repo.md) til finansforekomsten.

## <a name="configure-a-new-er-destination"></a>Konfigurer et nytt ER-mål

1. Gå til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. Velg en faktura for kundekontoen **US-001**.
3. På siden **Fritekstfaktura**, på **Faktura**-fanen, i gruppen **Utskriftsbehandling**, velger du **Utskriftsbehandling**.
4. På siden **Oppsett for utskriftsbehandling** utvider du **Modul - kunder** \> **Dokumenter** \> **Fritekstfaktura**, velger **Original**-posten og gjør deretter følgende:

    1.  Ta hensyn til gjeldende innstillinger for den valgte posten:
        -   Standard SSRS-rapport, **FreeTextInvoice.Report** er valgt i feltet **Rapportformat**.
        -   **\<Default\>**-navnet vises i **Mål**-feltet, med informasjon om at et egendefinert mål ikke er valgt for den tilordnede SSRS-rapporten. 
    2.  I **Rapportformat**-feltet velger du ER-formatkonfigurasjonen **Tilpasset fritekstfaktura (Excel)**.
        -   Navnet på **Mål**-feltet endres til **Målnavn**.
        -   **\<No named destination\>**-navnet vises i **Målnavn**-feltet, med informasjon om at et navngitt mål ikke er valgt for det tilordnede ER-formatet.
    3.  Velg pilknappen til høyre for **Målnavn**-feltet.    
    4. PÅ siden **Navngitt mål for elektronisk rapportering**, i **Navn**-feltet, angir du **Hovedmål**.
    5. Velg **Lagre**.
    6. På hurtigfanen **Filmål** [konfigurerer](er-destination-type-email.md) du målet **E-post** for **Rapport**-komponenten.
    7. Lukk siden **Navngitt mål for elektronisk rapportering**.
    8. På siden **Oppsett for utskriftsbehandling**, i feltet **Målnavn**, velger du det navngitte målet **Hovedmål**.

    ![Konfigurer et navngitt ER-mål for det valgte ER-formatet og tilordne det til en konfigurert utskriftsbehandlingspost på oppsettsiden for utskriftsbehandling](./media/er-named-destinations-01.gif)

    Du har nå konfigurert det navngitte ER-målet **Hovedmål** for formatet **Fritekstfaktura (Excel)** og tilordnet det til utskriftsbehandlingsposten **Original** under **Modul - kunder** \> **Dokumenter** \> **Fritekstfaktura**.

5. Utvid **Modul -kunder** \> **Konto - US-001** \> **Fritekstfaktura**, velg **Original**-posten, og følg deretter disse trinnene:

    1. Velg og hold (eller høyreklikk på) posten, og velg deretter **Overstyring**.
    2. Velg pilknappen til høyre for **Målnavn**-feltet.
    3. På siden **Navngitt mål for elektronisk rapportering** velger du **Ny** i handlingsruten.
    4. I feltet **Navn** angir du **US-001-mål**.
    5. På hurtigfanen **Filmål** [konfigurerer](er-destination-type-print.md) du målet **Skriver** for **Rapport**-komponenten.
    6. Lukk siden **Navngitt mål for elektronisk rapportering**.
    7. På siden **Oppsett for utskriftsbehandling**, i feltet **Målnavn**, velger du det navngitte målet **US-001-mål**.

    ![Konfigurer et navngitt ER-mål for det valgte ER-formatet og tilordne det til den konfigurerte utskriftsbehandlingsposten på oppsettsiden for utskriftsbehandling](./media/er-named-destinations-02.gif)

    Du har nå konfigurert det navngitte ER-målet **US-001-mål** for formatet **Fritekstfaktura (Excel)** og tilordnet det til utskriftsbehandlingsposten **Original** under **Modul - kunder** \> **Konto - US-001** \> **Fritekstfaktura**.

Når en fritekstfaktura behandles nå, kjøres ER-formatet **Fritekstfaktura (Excel)** og én av følgende hendelser skjer:

- Hvis fritekstfakturaen er for en annen kunde enn US-001, sendes det genererte dokumentet med e-post.
- Hvis fritekstfakturaen er for kunden US-001, blir det genererte dokumentet skrevet ut.

> [!NOTE]
> Når et navngitt mål ikke er definert for en utskriftsbehandlingspost som behandles ved kjøretid, brukes de standard ER-målene hvis de er tilgjengelige for ER-formatet som kjører.

> [!IMPORTANT]
> På siden **Mål for elektronisk rapportering** (**Organisasjonsadministrasjon** \> **Elektronisk rapportering** \> **Mål for elektronisk rapportering**), hvis du velger et ER-format som minst ett navngitt mål er konfigurert for, blir du varslet om tilstedeværelsen av navngitte mål.
>
> ![Varsling om at det finnes konfigurerte navngitte mål for det valgte ER-formatet på siden Mål for elektronisk rapportering](./media/er-named-destinations-03.png)
>
> Hvis du sletter standardmålet, blir også alle navngitte mål slettet. Hvis de navngitte målene ble valgt for utskriftsbehandlingsposter, avbrytes valget av disse navngitte målene.

## <a name="copy-an-existing-er-destination-as-a-new-named-destination"></a>Kopier et eksisterende ER-mål som et nytt navngitt mål

Når standard navngitte ER-mål er tilgjengelig for et ER-format, kan det brukes som en mal for nye ER-mål. Hvis du vil opprette et nytt ER-mål som er basert på standardmålet, velger du **Kopier fra standard** på siden **Navngitt mål for elektronisk rapportering**. Det nye målet kalles **Standard**. Du kan gjenta dette trinnet så mange ganger du vil.

Du kan velge et hvilket som helst eksisterende navngitt mål som en mal for et nytt navngitt mål. Hvis du vil opprette et nytt navngitt ER-mål som er basert på et valgt navngitt mål, velger du **Kopier** på siden **Navngitt mål for elektronisk rapportering**. Det nye målet har samme navn som det valgte navngitte målet, men suffikset "Kopi" er lagt til. Du kan gjenta dette trinnet så mange ganger du vil.

## <a name="security-considerations"></a>Sikkerhetshensyn

Du kan bare definere navngitte ER-mål på siden **Oppsett for utskriftsbehandling** hvis du har [tillatelse](../sysadmin/role-based-security.md#permissions) til å utføre denne oppgaven. Du kan få tillatelse hvis [plikten](../sysadmin/role-based-security.md#duties) **Konfigurer mål for elektronisk rapporteringsformat** er tilordnet til en av [sikkerhetsrollene](../sysadmin/role-based-security.md#security-roles) dine. Hvis du vil ha mer informasjon, se [Sikkerhetshensyn](electronic-reporting-destinations.md#security-considerations).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Mål for elektronisk rapportering (ER)](electronic-reporting-destinations.md)

[API-endringer for elektronisk rapporteringsrammeverk for Application update 10.0.17](er-apis-app10-0-17.md)

[API-endringer for elektronisk rapporteringsrammeverk for Application update 10.0.21](er-apis-app10-0-21.md)

[Endre kode for å gjøre det mulig for brukere å konfigurere og bruke navngitte ER-mål](er-api-named-destinations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
