---
title: Klargjøre programspesifikke metadata for RCS og ER
description: Dette emnet forklarer hvordan du klargjør programspesifikke metadata for Regulatory Configuration Service (RCS) og elektronisk rapportering (ER).
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3a540676ba11bc3c0fb7855a2fdaff998819dfbe
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849691"
---
# <a name="prepare-application-specific-metadata-for-rcs"></a>Klargjøre programspesifikke metadata for RCS

[!include[banner](../includes/banner.md)]

Dette emnet går gjennom eksempler på følgende oppgaver:

- [Klargjøre programmetadataene som kan brukes i RCS](#prepare-application-metadata-that-can-be-used-in-rcs)
- [Få tilgang til programmetadata ved hjelp av en ER-konfigurasjon](#access-application-metadata-by-using-an-er-configuration)
- [Få tilgang til programmetadata ved hjelp av tilkoblede programmer](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a>Klargjøre programmetadataene som kan brukes i RCS

Fremgangsmåten nedenfor viser hvordan en bruker av Finance and Operations som har rollen **Systemansvarlig** eller **Utvikler av elektronisk rapportering**, kan lage en ER-konfigurasjon (elektronisk rapportering) som inneholder metadata for programmet Microsoft Dynamics 365 for Finance and Operations, og som brukes til å utforme ER-modelltilordningskonfigurasjoner i Regulatory Configuration Service (RCS). Eksemplet på ER-modelltilordningskonfigurasjon som lages i dette eksemplet, brukes til å få tilgang til utenrikshandelstransaksjoner.

I dette eksemplet ønsker du å bruke RCS til å utforme en ER-løsning for Finance and Operations som skal brukes til å generere elektroniske dokumenter som inneholder informasjon fra forretningsdomenet for utenrikshandel. Hvis du vil angi tilordningen mellom ER-datamodellen og kildene til nødvendige data, må du ha tilgang til programmetadata for Finance and Operations i RCS. Du må derfor konfigurere en ny ER-metadatakonfigurasjon som en del av utformingen av ER-løsningen, og som inneholder alle metadataene som kreves for å kunne generere ER-rapporter for det valgte forretningsdomenet.

> [!NOTE]
> I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i et hvilket som helst firma.

1. Gå til **Organisasjonsstyring \> Arbeidsområder \> Elektronisk rapportering**.
2. Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**. Hvis du ikke ser denne konfigurasjonsleverandøren, fullfører du fremgangsmåten [Opprette en konfigurasjonsleverandør og merke den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. Velg **Metadatakonfigurasjoner**.
4. Velg **Opprett konfigurasjon**.
5. Skriv inn et navn i **Navn**-feltet i rullegardinboksen. I dette eksemplet angir du **Metadata for utenrikshandel**.
6. Velg **Opprett konfigurasjon**.
7. Velg **Utforming**.
8. Velg **Legg til**.

    > [!NOTE]
    > Du kan velge alle metadata for hele programmet eller for merkede modeller eller moduler. I begge tilfeller må du være oppmerksom på at følgende metadata blir lagt til automatisk: tabeller med poster, opplistinger og utvidede datatyper (EDT-er). Når det kreves flere typer metadata, må de legges til manuelt.

Du må legge til enkelte metadata som er knyttet til utenrikshandelstransaksjoner, og velge metadataelementer manuelt.

9. Velg **Legg til datakilde \> Tabellposter**.
10. Filtrer etter verdien **Intrastat** i **Navn**-feltet.
11. Velg **Intrastat**-tabellposten.
12. Velg **OK**.

Du må legge til metadatainformasjon om Intrastat-tabellen med poster.

13. Velg **Tabellposter Intrastat \> \>Relasjoner \> IntrastatCommodity (Tabellposter EcoResCategory)** i treet.
14. Velg **Legg til metadata**.

    > [!NOTE]
    > Metadata om nødvendige relasjoner for den valgte tabellen med poster må legges til manuelt.

15. Velg **Legg til datakilde**.
16. Velg **Opplisting**.
17. Filtrer etter verdien **IntrastatDirection** i **Navn**-feltet.
18. Velg opplistingsposten **IntrastatDirection**.
19. Velg **OK**.
20. Velg **Lagre**.
21. Lukk siden.
22. Fullfør kladdeversjonen av metadatakonfigurasjonen:

    1. Velg **Endre status \> Fullført**.
    2. Velg **OK**.
    3. Velg fullført versjon 1.

23. Eksporter den fullførte versjonen av metadatakonfigurasjonen fra programmet som en XML-fil:

    1. Velg **Veksle \> Eksporter som XML-fil**.
    2. Velg **OK**.

ER-metadatakonfigurasjonen du laget, lagres som filen **Foreign trade metadata.xml**. Du kan nå importere den til RCS, slik at den kan brukes som kilden til metadata for forretningsdomenet for utenrikshandel i Finance and Operations. Basert på denne informasjonen kan du angi tilordningen mellom programmetadata og ER-datamodellen.

## <a name="access-application-metadata-by-using-an-er-configuration"></a>Få tilgang til programmetadata ved hjelp av en ER-konfigurasjon

Fremgangsmåten nedenfor viser hvordan en RCS-bruker som har rollen **Systemansvarlig** eller **Utvikler av elektronisk rapportering**, kan utforme en ny ER-modelltilordning ved hjelp av metadata fra programmet Finance and Operations. Du får tilgang til programmetadata ved å bruke en ER-metadatakonfigurasjon som inneholder et eksempelsett med metadata som gir tilgang til utenrikshandelstransaksjoner.

Før du kan fullføre denne fremgangsmåten, må du først fullføre følgende fremgangsmåter:

- [Opprette en konfigurasjonsleverandør og merke den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [Klargjøre programmetadataene som kan brukes i RCS](#prepare-application-metadata-that-can-be-used-in-rcs)

1. Gå til **Alle arbeidsområder \> Elektronisk rapportering**.
2. Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**. Hvis du ikke ser denne konfigurasjonsleverandøren, fullfører du fremgangsmåten [Opprette en konfigurasjonsleverandør og merke den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. Importer ER-metadatakonfigurasjonen som inneholder metadata for programmet Finance and Operations, og som er konfigurert slik at elektroniske dokumenter genereres for det utenlandske forretningsdomenet. Du laget denne ER-metadatakonfigurasjonen og eksporterte den som en XML-fil i fremgangsmåten [Klargjøre programmetadataene som kan brukes i RCS](#prepare-application-metadata-that-can-be-used-in-rcs) tidligere i dette emnet.

    1. Velg **Metadatakonfigurasjoner**.
    2. Velg **Veksle**.
    3. Velg **Last fra XML-fil**.
    4. Bla gjennom for å velge filen **Foreign trade metadata.xml**.
    5. Velg **OK**.
    6. Lukk siden.

4. Opprett en datamodellkonfigurasjon:

    1. Velg **Rapporteringskonfigurasjoner**.
    2. Velg **Opprett konfigurasjon**.
    3. Skriv inn **Utenrikshandelsmodell** i **Navn**-feltet i rullegardinboksen.
    4. Velg **Opprett konfigurasjon**.
    5. Velg **Utforming**.
    6. Velg **Ny** for å åpne nedtrekksdialogen.

        1. Skriv inn **Rot** i **Navn**-feltet.
        2. Velg **Legg til**.
    
    7. Velg **Ny** for å åpne nedtrekksdialogen.

        1. Skriv inn **Transaksjon** i **Navn**-feltet.
        2. Velg **Postliste** i **Varetype**-feltet.
        3. Velg **Legg til**.
 
    8. Velg **Ny** for å åpne nedtrekksdialogen.

        1. I **Navn**-feltet skriver du inn **Artikkelkode**.
        2. Velg **Streng** i **Varetype**-feltet.
        3. Velg **Legg til**.

    9. Velg **Ny** for å åpne nedtrekksdialogen.

        1. Skriv inn **Fakturert beløp** i Navn-feltet.
        2. Velg **Faktisk** i **Varetype**-feltet.
        3. Velg **Legg til**.

    10. Velg **Ny** for å åpne nedtrekksdialogen.

        1. Skriv inn **Dato** i **Navn**-feltet.
        2. Velg **Dato** i **Varetype**-feltet.
        3. Velg **Legg til**.
 
    11. Velg **Legg til \> Rotreferanse**.
    12. Velg **OK**.
    13. Velg **Lagre**.
    14. Lukk siden.
    15. Velg **Endre status \> Fullført**.
    16. Velg **OK**.

5. Opprett en modelltilordningskonfigurasjon:

    1. Velg **Opprett konfigurasjon**.
    2. I **Ny**-feltet i rullegardinboksen skriver du inn **Modelltilordning basert på datamodellen Utenrikshandelsmodell**.
    3. I **Navn**-feltet angir du **Utenrikshandelstilordning**.
    4. Velg **Opprett konfigurasjon**.
    5. Velg **Rediger** i hurtigfanen **Forutsetninger**.
    6. Velg **Ny**.
    7. Velg **Konfigurasjon** i feltet **Nødvendig komponenttype**.
    8. Velg konfigurasjonen **Metadata for utenrikshandel**.
    9. Velg **Lagre**. Legg merke til at referansen er lagt til i versjon 1 av konfigurasjonen **Metadata for utenrikshandel**. Programmetadata fra denne konfigurasjonen tilbys når modelltilordningen er utformet.
    10. Lukk siden.
    11. Velg **Utforming**.
    12. Velg **Utforming**.
    13. Velg **Dynamics 365 for Operations \> Tabellposter** i treet.
    14. Velg **Legg til rot**.
    15. Angi **Intrastat** i **Navn**-feltet.
    16. Velg **Intrastat**-tabellposter.
    17. Velg **OK**.

        > [!NOTE]
        > Bare to tabeller tilbys, fordi bare to tabeller ble lagt til i settet med metadata som brukes for øyeblikket.

    18. Velg **Bind**.
    19. Velg **Intrastat \> AmountMST** i treet.
    20. Velg **Transaksjon = Intrastat \> Fakturert beløp** i treet.
    21. Velg **Bind**.
    22. Velg **Intrastat \> TransDate** i treet.
    23. Velg **Transaksjon = Intrastat \> Dato** i treet.
    24. Velg **Bind**.
    25. Velg **Intrastat \> \>Relasjoner \> IntrastatCommodity \> Kode** i treet.
    26. Velg **Transaksjon = Intrastat \> Artikkelkode** i treet.
    27. Velg **Bind**.
    28. Velg **Valider**.

        > [!NOTE]
        > Etter at valideringen er fullført, har du bundet elementer i datamodellen til elementer i datakildene som er beskrevet, ved å bruke detaljer i programmetadataene fra ER-metadatakonfigurasjonen det henvises til.

    29. Velg **Lagre**.

Du kan utvide det eksisterende settet med metadata i Finance and Operations etter behov. Du kan deretter eksportere den nye, fullførte versjonen av ER-metadatakonfigurasjonen fra Finance and Operations, importere den til RCS og oppdatere forutsetningene for den konfigurerte modelltilordningskonfigurasjon slik at den henviser til en ny versjon av den importerte metadatakonfigurasjonen.

> [!NOTE]
> Denne metoden for å hente informasjon om programmetadata er den eneste tilgjengelige metoden for programmer som er distribuert lokalt (det vil si når lokale forretningsdata \[LBD\] eller en lokal distribusjonsmodell brukes til Finance and Operations).

## <a name="access-application-metadata-by-using-connected-applications"></a>Få tilgang til programmetadata ved hjelp av tilkoblede programmer

Fremgangsmåten nedenfor viser hvordan en RCS-bruker som har rollen **Systemansvarlig** eller **Utvikler av elektronisk rapportering**, kan utforme en ny ER-modelltilordning ved hjelp av metadata for programmet Finance and Operations. Du får tilgang til programmetadata på nettet ved å bruke et RCS-tilkoblet program. Et ER-modelltilordningseksempel blir konfigurert for å gi tilgang til utenrikshandelstransaksjoner.

For å kunne fullføre denne fremgangsmåten må du først fullføre fremgangsmåten [Opprette en konfigurasjonsleverandør og merke den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md) i RCS. Hvis du ikke har fullført fremgangsmåten [Få tilgang til programmetadata ved hjelp av en ER-konfigurasjon](#access-application-metadata-by-using-an-er-configuration) tidligere i dette emnet ennå, går du til siden [Oppgaveveiledninger for elektronisk rapportering for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) for å laste ned følgende ER-konfigurasjonsfiler på forhånd og lagre dem lokalt: **Foreign trade metadata.xml**, **Foreign trade model.xml** og **Foreign trade mapping.xml**.


### <a name="get-required-er-configurations"></a>Hente nødvendige ER-konfigurasjoner

Hvis du allerede har fullført fremgangsmåten [Få tilgang til programmetadata ved hjelp av en ER-konfigurasjon](#access-application-metadata-by-using-an-er-configuration) tidligere i dette emnet, har du allerede alle nødvendige ER-konfigurasjoner (konfigurasjonene for metadata, modell og tilordning for utenrikshandel) i gjeldende RCS-forekomst. I så fall kan du hoppe over denne fremgangsmåten.

1. Gå til **Alle arbeidsområder \> Elektronisk rapportering**.
2. Velg **Rapporteringskonfigurasjoner**.
3. Last inn konfigurasjonsfilene **Foreign trade metadata.xml**, **Foreign trade model.xml** og **Foreign trade mapping.xml**, og gjenta følgende fremgangsmåten for hver av dem:

    1. Velg **Veksle**.
    2. Velg **Last fra XML-fil**.
    3. Velg **Bla gjennom** og velg en fil.
    4. Velg **OK**.

### <a name="register-the-connection-with-finance-and-operations"></a>Registrere tilkoblingen til Finance and Operations

1. Gå til **Alle arbeidsområder \> Elektronisk rapportering**.
2. Velg **Tilkoblede programmer**.
3. Kontroller at det konfigurerte programmet er basert på Microsoft Azure, og at det er tilgjengelig generelt for RCS-brukere. Den gjeldende RCS-brukeren må ha tilgang til det konfigurerte programmet som registreres som en bruker av dette programmet, i en rolle som gir vedkommende tilgangsrettigheter til programmets metadata.
4. Velg **Ny**.
5. I **Navn**-feltet angir du **MyConnectedApp** som navnet på det tilkoblede programmet.
6. I **Program**-feltet angir du URL-adressen til programmet.
7. I **Leietaker**-feltet angir du leverandøren av programmet.
8. Velg **Lagre**. 
9. Når du kontrollerer tilkoblingen til det konfigurerte programmet, velger du koblingen **Klikk her for å koble til det valgte eksterne programmet** på siden **Koble til eksternt program**. 
10. Velg **Kontroller tilkobling** for å validere tilgang til det konfigurerte programmet.
11. Velg **Lukk**.

Etter at du har fullført denne fremgangsmåten og valideringen av tilkoblingen har lykkes, oppdateres versjons- og leietakerdetaljene for det konfigurerte programmet i gjeldende rutenett.

### <a name="review-the-existing-model-mapping-configuration"></a>Se gjennom den eksisterende modelltilordningskonfigurasjonen

1. Gå til **Alle arbeidsområder \> Elektronisk rapportering**.
2. Velg **Rapporteringskonfigurasjoner**.
3. Velg **Utenrikshandelsmodell \> Utenrikshandelstilordning** i treet.
4. Velg hurtigfanen **Forutsetninger**.

    > [!NOTE]
    > Denne tilordningen henviser til metadatakonfigurasjonen for øyeblikket. Programmetadata fra denne konfigurasjonen tilbys når denne modelltilordningen er utformet.

4. Velg **Utforming**.
5. Velg **Utforming**.
6. Velg **Dynamics 365 for Operations \> Tabellposter** i treet.
7. Velg **Legg til rot**.
8. Angi eller velg en verdi i **Tabell**-feltet.

    > [!NOTE]
    > Denne tilordningen henviser til metadatakonfigurasjonen for øyeblikket. Programmetadata fra denne konfigurasjonen tilbys når denne modelltilordningen er utformet.

9. Velg **Avbryt**.

### <a name="assign-the-connected-application-to-a-model-mapping"></a>Tilordne det tilkoblede programmet til en modelltilordning

1. Velg **Rediger**.
2. Velg programmet **MyConnectedApp** i feltet **Tilkoblet program**.

    > [!NOTE]
    > Denne tilordningen henviser til metadataene i det valgte tilkoblede programmet. Hvis en tilordning henviser til metadatakonfigurasjonen og det tilkoblede programmet samtidig, brukes metadataene for det tilkoblede programmet.

3. Velg **Utforming**.
4. Velg **Utforming**.
5. Velg **Dynamics 365 for Operations \> Tabellposter** i treet.
6. Velg **Legg til rot**.
7. Angi eller velg en verdi i **Tabell**-feltet.

    > [!NOTE]
    > På dette stadiet er det flere enn to programtabeller som tilbys, fordi denne tilordningen bruker alle metadataene i det tilkoblede programmet som er tilordnet til den.

8. Velg **Avbryt**.
9. Velg **Valider**.

Du har nå bundet elementer i datamodellen til elementer i datakildene som er beskrevet, ved å bruke detaljer i metadataene for det tilkoblede programmet som er tilordnet til denne tilordningen.

Når du må evaluere denne modelltilordningen ved å bruke metadataene for en annen versjon av programmet, registrerer du et nytt tilkoblet program, tilordner det til denne modelltilordningen og validerer det mot de nye metadataene.

## <a name="additional-resources"></a>Tilleggsressurser

Du kan også spille av oppgaveveiledningen **Klargjøre programmetadataene som kan brukes i RCS** i Finance and Operations samt oppgaveveiledningene **Få tilgang til programmetadata ved hjelp av en ER-konfigurasjon** og **Få tilgang til programmetadata ved hjelp av tilkoblede programmer** i RCS. Disse oppgaveveiledningene kan lastes ned fra siden [Oppgaveveiledninger for elektronisk rapportering for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).
