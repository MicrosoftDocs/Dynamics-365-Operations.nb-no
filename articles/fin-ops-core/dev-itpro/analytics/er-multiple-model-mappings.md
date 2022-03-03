---
title: Behandle flere avledede tilordninger for én modellrot
description: Dette emnet beskriver hvordan du kan administrere flere avledede tilordninger som ble konfigurert for én modellrot.
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d71b05b3f2eda93a93f728926e675c040371781e
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2022
ms.locfileid: "8324118"
---
# <a name="manage-several-derived-mappings-for-a-single-model-root"></a>Behandle flere avledede tilordninger for én modellrot

[!include [banner](../includes/banner.md)]

En datamodellkomponent for [elektronisk rapportering (ER)](general-electronic-reporting.md) brukes i alle konfigurerte komponenter for ER-format som datakilde for å generere utgående dokumenter. Hvis du vil beskrive ett bedriftsdomene, konfigurerer du en datamodellkomponent som har mange rotdefinisjoner. 

Hver rotdefinisjon lar deg representere data i dette domenet på måten som passer best for bestemte rapporteringsformål. For hver rotdefinisjon kan du konfigurere en komponent for ER-modelltilordning som en implementering av datamodellen som gjelder spesifikt for Microsoft Dynamics 365 Finance. På denne måten beskriver du hvordan datamodellen skal fylles ut ved kjøretid.

Komponenter for ER-modelltilordning kan være i [konfigurasjoner](general-electronic-reporting.md#Configuration) for ER-datamodell og konfigurasjoner for ER-modelltilordning. Én ER-konfigurasjon kan inneholde mange tilordningskomponenter, der hver enkelt er konfigurert for én rotdefinisjon. Én ER-konfigurasjon kan også inneholde bare én tilordningskomponent som er konfigurert for én rotdefinisjon.

Mange konfigurasjonsleverandører kan tilby konfigurasjoner for ER-modelltilordning for samme ER-datamodell. Disse konfigurasjonene for modelltilordning kan inneholde tilordningskomponenter for ulike rotdefinisjoner. Du kan bruke en modelltilordning for én rotdefinisjon som tilbys av én [leverandør](general-electronic-reporting.md#Provider), og bruke en modelltilordning for en annen rotdefinisjon som tilbys av en annen leverandør.

Fremgangsmåtene i dette emnet forklarer hvordan du kan administrere flere konfigurasjoner for ER-modelltilordning for en ER-datamodell når de inneholder ulike modelltilordningskomponenter som er konfigurert for samme rotdefinisjon. 

For å kunne fullføre fremgangsmåtene i dette emnet må du være tilordnet til rollen Systemansvarlig eller Utvikler av elektronisk rapportering.

Alle disse fremgangsmåtene kan utføres i USMF-firmaet. Ingen koding er nødvendig.

## <a name="configure-the-er-framework"></a>Konfigurere ER-rammeverket

Som en bruker i rollen som utvikler av elektronisk rapportering må du [konfigurere minimumssettet](er-quick-start2-customize-report.md#ConfigureFramework) av ER-parametere før du kan begynne å bruke ER-rammeverket til å generere forretningsdokumenter.

## <a name="import-the-standard-er-format-configurations"></a>Importer standard ER-formatkonfigurasjoner

Hvis du vil legge til standard ER-konfigurasjoner i den gjeldende forekomsten av Finance, må du importere dem fra ER- repositoriet som ble konfigurert for den forekomsten. Følg fremgangsmåten i [Last ned ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten](er-download-configurations-global-repo.md) for å importere følgende ER-formatkonfigurasjoner:

- **Fritekstfaktura (Excel)** versjon 220.106
- **Prosjektfaktura (Excel)** versjon 226.27

## <a name="review-the-imported-er-configurations"></a>Se gjennom importerte ER-konfigurasjoner

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner**, i delen **Konfigurasjoner**, velger du flisen **Rapporteringskonfigurasjoner**.
3. I konfigurasjonstreet i venstre rute på **Konfigurasjoner**-siden utvider du **Fakturamodell**.

    ![Se gjennom de importerte konfigurasjoner på Konfigurasjoner-siden.](./media/er-multiple-model-mappings-image1.png)

4. Se gjennom formatet **Fritekstfaktura (Excel)**:

    1. I konfigurasjonstreet i venstre rute velger du **Fritekstfaktura (Excel)**.
    2. Velg **Utforming** i handlingsruten.
    3. Velg **Modell** i listen over datakilder i **Tilordning**-fanen på **Formatutforming**-siden.
    4. Velg **Vis**.
    
       Det gjeldende ER-formatet er konfigurert slik at det bruker rotdefinisjonen **InvoiceCustomer** for **Fakturamodell**. Når dette formatet kjøres og datakilden **Modell** kalles opp, brukes modelltilordningen som er konfigurert for rotdefinisjonen **InvoiceCustomer**, til å få tilgang til programdata og fylle ut datamodellen.

        ![Se gjennom modelldatakilden på Formatutforming-siden.](./media/er-multiple-model-mappings-image2.png)

    6. Lukk **Formatutforming**-siden.

5. Se gjennom innholdet i konfigurasjonen for **Fakturamodelltilordning**:

    1. I konfigurasjonstreet i venstre rute velger du **Fakturamodelltilordning**.
    2. Velg **Utforming** i handlingsruten.
    3. Legg merke til at gjeldende konfigurasjon for ER-modelltilordning på siden **Modell til datakildetilordning** inneholder flere komponenter for modelltilordning:

        + Modelltilordningen **Kundefaktura** er konfigurert for rotdefinisjonen **InvoiceCustomer** for **Fakturamodell**. Når ER-formatet **Fritekstfaktura (Excel)** kjøres, kan derfor modelltilordningen **Kundefaktura** for denne ER-konfigurasjonen velges for å få tilgang til programdata og fylle ut datamodellen.
        + Modelltilordningen **Prosjektfaktura** er konfigurert for rotdefinisjonen **InvoiceProject** for **Fakturamodell**. Når ER-formatet **Prosjektfaktura (Excel)** kjøres, kan derfor modelltilordningen **Prosjektfaktura** for denne ER-konfigurasjonen velges for å få tilgang til programdata og fylle ut datamodellen.

        ![Fakturamodelltilordning på siden Modell til datakildetilordning.](./media/er-multiple-model-mappings-image3.png)

    4. Lukk siden **Tilordning av modell til datakilde**.
    5. I hurtigfanen **Versjoner** velger du **Slett** for å slette alle versjonene av denne ER-konfigurasjonen som er nyere enn versjon 240.175.

6. Se gjennom innholdet i konfigurasjonen for **Modelltilordning for prosjektfaktura (RDP)**:

    1. I konfigurasjonstreet i venstre rute velger du **Modelltilordning for prosjektfaktura (RDP)**.
    2. Velg **Utforming** i handlingsruten.
    3. Legg merke til at den gjeldende konfigurasjonen for ER-modelltilordning på siden **Modell til datakildetilordning** inneholder modelltilordningen **InvoiceProject**, og at denne modelltilordningen er konfigurert for rotdefinisjonen **InvoiceProject** for **Fakturamodell**. Når ER-formatet **Prosjektfaktura (Excel)** kjøres, velger du modelltilordningen **InvoiceProject** for denne ER-konfigurasjonen for å få tilgang til programdata og fylle ut datamodellen.

        ![Modelltilordning for prosjektfaktura på siden Modell til datakildetilordning.](./media/er-multiple-model-mappings-image4.png)

    4. Lukk siden **Tilordning av modell til datakilde**.
    5. I hurtigfanen **Versjoner** velger du **Slett** for å slette alle versjonene av denne ER-konfigurasjonen som er nyere enn versjon 226.35.

## <a name="customize-the-imported-er-configurations"></a>Tilpasse de importerte ER-konfigurasjonene

Denne delen beskriver hvordan du [tilpasser](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration) modelltilordningene som leveres av Microsoft. Det kan for eksempel bli nødvendig med tilpassing for å implementere den egendefinerte logikken din eller legge til manglende bindinger.

### <a name="customize-the-invoice-model-mapping-configuration"></a>Tilpasse konfigurasjonen for Fakturamodelltilordning

1. Velg **Fakturamodelltilordning** i konfigurasjonstreet i venstre rute på **Konfigurasjoner**-siden.
2. Velg **Opprett konfigurasjon** i handlingsruten.
3. Velg **Avled fra navn: Fakturamodelltilordning, Microsoft** i **Ny**-feltet i rullegardinboksen **Opprett konfigurasjon**.
4. I feltet **Navn** angir du **Fakturamodelltilordning (Litware)**.
5. Velg **Opprett konfigurasjon**.
6. [Merk](er-quick-start2-customize-report.md#MarkFormatRunnable) [utkast](general-electronic-reporting.md#component-versioning)versjonen av den avledede tilordningen som tilgjengelig for bruk ved kjøretid:

    1. Velg **Brukerparametere** i gruppen **Avanserte innstillinger** i **Konfigurasjoner**-fanen i handlingsruten.
    2. I dialogboksen **Brukerparametere** setter du **Kjøringsinnstillinger** til **Ja**, og deretter velger du **OK**.
    3. Velg om nødvendig **Rediger** for å gjøre siden redigerbar.
    4. Sett alternativet **Kjør utkast** til **Ja** for konfigurasjonen **Fakturamodelltilordning (Litware)** som for øyeblikket er valgt i konfigurasjonstreet.

7. Velg **Utforming** i handlingsruten for å se gjennom modelltilordningene for denne konfigurasjonen.

    ![Se gjennom fakturamodelltilordningene på siden Modell til datakildetilordning.](./media/er-multiple-model-mappings-image5.png)

    > [!TIP]
    > Du kan nå åpne enhver av komponentene for ER-modelltilordning for denne ER-konfigurasjonen i utformingen for å konfigurere den egendefinerte logikken. Hvis du vil ha mer informasjon, kan du se [Tilpasse modelltilordningskonfigurasjonen](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration).

8. Lukk siden **Tilordning av modell til datakilde**.

Du har nå konfigurasjonene **Fakturamodelltilordning** og **Fakturamodelltilordning (Litware)**, der hver har en modelltilordning som er konfigurert for rotdefinisjonen **InvoiceCustomer**. Tilordne en av modelltilordningene eksplisitt som standard modelltilordning som brukes av ethvert ER-format, for eksempel formatet **Fritekstfaktura (Excel)** som inneholder en modelldatakilde som har rotdefinisjonen **InvoiceCustomer**. Hvis du ikke gjør dette, oppstår følgende unntak for å varsle deg om at ingen standard modelltilordning er eksplisitt tilordnet, når du kjører, redigerer eller validerer et av ER-formatene:
 
> Det finnes flere modelltilordninger for datamodellen \<model name\> ( \<root descriptor\>) i konfigurasjonene \<configuration names separated by commas\>. Angi én av konfigurasjonene som standard.

![Åpne formatet for redigering på Konfigurasjoner-siden.](./media/er-multiple-model-mappings-image6.gif)

### <a name="customize-the-project-invoice-model-mapping-rdp-configuration"></a>Tilpasse konfigurasjonen for Modelltilordning for prosjektfaktura (RDP)

1. Velg **Modelltilordning for prosjektfaktura (RDP)** i konfigurasjonstreet i venstre rute på **Konfigurasjoner**-siden.
2. Velg **Opprett konfigurasjon** i handlingsruten.
3. Velg **Avled fra navn: Modelltilordning for prosjektfaktura (RDP), Microsoft** i **Ny**-feltet i dialogboksen **Opprett konfigurasjon**.
4. I feltet **Navn** angir du **Modelltilordning for prosjektfaktura (Litware)**.
5. Velg **Opprett konfigurasjon**.
6. Sett alternativet **Kjør utkast** til **Ja** for konfigurasjonen **Modelltilordning for prosjektfaktura (Litware)** som for øyeblikket er valgt i konfigurasjonstreet.
7. Velg **Utforming** i handlingsruten for å se gjennom modelltilordningene for denne konfigurasjonen.

    ![Se gjennom de tilpassede modelltilordningene for prosjektfaktura på siden Modell til datakildetilordning.](./media/er-multiple-model-mappings-image7.png)

8. Lukk siden **Tilordning av modell til datakilde**.

Du har nå konfigurasjonene **Fakturamodelltilordning**, **Modelltilordning for prosjektfaktura (RDP)** og **Modelltilordning for prosjektfaktura (Litware)**. Hver av disse konfigurasjonene har en modelltilordning konfigurert for rotdefinisjonen **InvoiceProject**. Tilordne en av modelltilordningene eksplisitt som standard modelltilordning som brukes av ethvert ER-format. Du kan for eksempel bruke formatet **Prosjektfaktura (Excel)** som inneholder en modelldatakilde som har rotdefinisjonen **InvoiceProject**. Hvis du ikke gjør dette, oppstår det et unntak for å varsle deg om at ingen standard modelltilordning er eksplisitt tilordnet, når du kjører eller redigerer et av ER-formatene.

## <a name="select-the-derived-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Velge den avledede konfigurasjonen Fakturamodelltilordning (Litware) som konfigurasjonen som inneholder standard modelltilordninger

1. Velg **Fakturamodelltilordning (Litware)** i konfigurasjonstreet i venstre rute på **Konfigurasjoner**-siden.
2. Sett alternativet **Standard for modelltilordning** til **Ja**.

    ![Angi modelltilordningen som standard modelltilordning på Konfigurasjoner-siden.](./media/er-multiple-model-mappings-image8.png)

    På grunn av denne innstillingen brukes modelltilordningen **Kundefakturakopi** når du kjører **Fritekstfaktura (Excel)**, eller når du redigerer eller validerer den. Modelltilordningen **Kundefaktura** fra konfigurasjonen **Fakturamodelltilordning** ignoreres.

    Du kan nå åpne formatet **Fritekstfaktura (Excel)** for gjennomgang i formatutformingen.

## <a name="select-the-derived-project-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Velge den avledede konfigurasjonen Modelltilordning for prosjektfaktura (Litware) som konfigurasjonen som inneholder standard modelltilordninger

1. Velg **Modelltilordning for prosjektfaktura (Litware)** i konfigurasjonstreet i venstre rute på **Konfigurasjoner**-siden.
2. Sett alternativet **Standard for modelltilordning** til **Ja**.

    I dette tilfellet, og i motsetning til tilfellet som beskrives for konfigurasjonen **Fakturamodelltilordning (Litware)** i forrige del, kan du ikke begynne å bruke modelltilordningen **InvoiceProject Copy** fra konfigurasjonen **Modelltilordning for prosjektfaktura (Litware)**. To konfigurasjoner som inneholder en modelltilordning for rotdefinisjonen **InvoiceProject**, er merket som standardkonfigurasjonen. De har derfor lik prioritet for bruk. Du kan løse dette problemet ved å fullføre de gjenstående trinnene i denne fremgangsmåten.

3. I konfigurasjonstreet i venstre rute velger du **Fakturamodelltilordning (Litware)**.
4. Velg **Utforming** i handlingsruten.
5. På siden **Modell til datakildetilordning** velger du **Rediger** for å gjøre siden redigerbar etter behov.
6. Velg modelltilordningen **Prosjektfakturakopi**, og merk deretter av for **Er slettet** for den.

    ![Angi modelltilordningen som virtuelt slettet på siden Modell til datakildetilordning.](./media/er-multiple-model-mappings-image9.png)

    På grunn av denne innstillingen behandles konfigurasjonen **Fakturamodelltilordning (Litware)** som om den ikke har noen modelltilordning for rotdefinisjonen **InvoiceProject**. Modelltilordningen **InvoiceProject Copy** utstedes som standard. Konfigurasjonen **Modelltilordning for prosjektfaktura (Litware)**, som inneholder denne modelltilordningen, er merket som standardkonfigurasjon. Siden den er merket som standard, har den en høyere prioritet enn modelltilordningen **InvoiceProject** fra konfigurasjonen **Modelltilordning for prosjektfaktura (RDP)**.

## <a name="other-considerations"></a>Andre hensyn

Modelltilordningen **InvoiceProject Copy** i konfigurasjonen **Modelltilordning for prosjektfaktura (Litware)** er utformet for å bruke datakilden **ReportDataProvider**. Datakilden er en del av *Objekt*-typen som refererer til programklassen **PsaProjInvoiceDP**. Denne klassen er implementert som dataleverandøren for SSRS-rapporten (SQL Server Reporting Services) for prosjektfaktura i rammeverket for utskriftsbehandling. Velg denne datakilden som ER-[integreringspunkt](er-apis-app10-0-11.md#api-to-run-a-format-mapping-for-the-generation-of-outbound-documents). Den gjeldende ER-implementeringen for rapporter for utskriftsbehandling tar hensyn til denne innstillingen. Hvis du vil ha mer informasjon, kan du se gjennom kildekoden til programklassen **ERPrintMgmtDataProviderReport**. Tilordningen av datakilden **ReportDataProvider** som integrasjonspunktet for modelltilordning ved kjøretid, tvinger Finance til å behandle denne tilordningskomponenten med en høyere prioritet enn tilordningskomponenten for **InvoiceProject** fra konfigurasjonen **Modelltilordning for prosjektfaktura (RDP)**.

## <a name="see-also"></a>Se også

- [Administrere ER-modelltilordning i separate ER-konfigurasjoner](./tasks/er-manage-model-mapping-configurations-july-2017.md)
- [Konfigurere modelltilordninger for landkontekstavhengig ER](er-country-dependent-model-mapping.md)
- [Endringer i API-en for rammeverket for elektronisk rapportering](er-apis-app10-0-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
