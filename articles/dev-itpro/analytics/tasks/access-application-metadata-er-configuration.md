---
title: Få tilgang til programmetadata ved hjelp av ER-konfigurasjon
description: Trinnene i dette emnet forklarer hvordan en RCS-bruker (Regulatory Configuration Service) kan utforme en ny modelltilordning for elektronisk rapportering (ER) ved å bruke metadataene i Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b95b41b27cecd4c71ed7646f329cf5736a01b561
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727035"
---
# <a name="access-application-metadata-by-using-er-configuration"></a>Få tilgang til programmetadata ved hjelp av ER-konfigurasjon

[!include [task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en RCS-bruker (Regulatory Configuration Service) i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan utforme en ny modelltilordning for elektronisk rapportering (ER) ved å bruke metadataene i programmet Dynamics 365 for Finance and Operations. Du får tilgang til programmetadata ved å bruke en ER-metadatakonfigurasjon som inneholder et eksempelsett med metadata som gir tilgang til utenrikshandelstransaksjoner. For å fullføre disse trinnene må du først fullføre trinnene i emnet [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md). Deretter fullfører du trinnene i emnet [(ER) Klargjøre programmetadataene som skal brukes i RCS](prepare-application-metadata-rcs.md) i Finance and Operations.

## <a name="prerequisites"></a>Forutsetninger
1. Gå til **Alle arbeidsområder** > **Elektronisk rapportering**. 
2. Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**. Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md). 

## <a name="import-metadata-configuration"></a>Importere metadatakonfigurasjon 
1. Klikk på **Metadatakonfigurasjoner**. 
2. Importer ER-metadatakonfigurasjonen som inneholder metadata fra programmet Finance and Operations, som er konfigurert slik at elektroniske dokumenter genereres for utenrikshandel. Denne ER-metadatakonfigurasjonen har blitt eksportert som en XML-fil mens trinnene i prosedyren [(ER) Klargjøre programmetadataene som skal brukes i RCS](prepare-application-metadata-rcs.md) har blitt fullført. 
3. Klikk på **Veksle**. 
4. Klikk på **Last fra XML-fil**. 
5. Klikk på **Bla gjennom**, og velg filen Foreign trade metadata.xml. 
6. Klikk **OK**. 
7. Lukk siden. 

## <a name="create-data-model-configuration"></a>Opprette en datamodellkonfigurasjon
1. Klikk på **Rapporteringskonfigurasjoner**. 
2. Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen. 
3. I **Navn**-feltet skriver du inn «Utenrikshandelsmodell». 
4. Klikk **Opprett konfigurasjon**. 
5. Klikk **Utforming**. 
6. Klikk på **Ny** for å åpne nedtrekksdialogen. 
7. Skriv inn «Rot» i **Navn**-feltet. 
8. Klikk **Legg til**. 
9. Klikk på **Ny** for å åpne nedtrekksdialogen. 
10. Skriv inn «Transaksjon» i **Navn**-feltet. 
11. Velg **Postliste** i **Varetype**-feltet. 
12. Klikk **Legg til**. 
13. Klikk på **Ny** for å åpne nedtrekksdialogen. 
14. I **Navn**-feltet skriver du inn «Artikkelkode». 
15. Velg **Streng** i **Varetype**-feltet. 
16. Klikk **Legg til**. 
17. Klikk på **Ny** for å åpne nedtrekksdialogen. 
18. Skriv inn «Fakturert beløp» i **Navn**-feltet. 
19. Velg **Faktisk** i **Varetype**-feltet. 
20. Klikk **Legg til**. 
21. Klikk på **Ny** for å åpne nedtrekksdialogen. 
22. Skriv inn «Dato» i **Navn**-feltet. 
23. Velg **Dato** i **Varetype**-feltet. 
24. Klikk **Legg til**. 
25. Klikk på **Rotreferanse**. 
26. Klikk **OK**. 
27. Klikk **Lagre**. 
28. Lukk siden. 
29. Klikk på **Endre status**. 
30. Klikk på **Fullført**. 
31. Klikk **OK**. 

## <a name="create-model-mapping-configuration"></a>Opprette en modelltilordningskonfigurasjon 
1. Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen. 
2. I **Ny**-feltet angir du «Modelltilordning basert på datamodellen Utenrikshandelsmodell». 
3. I **Navn**-feltet skriver du inn «Utenrikshandelstilordning». 
4. Klikk **Opprett konfigurasjon**. 
5. Utvid delen **Forutsetninger**. 
6. Klikk **Rediger**. 
7. Klikk på **Ny**. 
8. Merk den valgte raden i listen. 
9. Velg **Konfigurasjon** i feltet **Nødvendig komponenttype**. 
10. Velg konfigurasjonen **Metadata for utenrikshandel**. 
11. Klikk **Lagre**. 
12. Vi har lagt til referansen i versjon 1 av konfigurasjonen Metadata for utenrikshandel. Programmetadata fra denne konfigurasjonen tilbys mens denne modelltilordningen utformes. 
13. Lukk siden. 
14. Klikk **Utforming**. 
15. Klikk **Utforming**. 
16. I treet velger du **Dynamics 365 for Operations\Tabellposter**. 
17. Klikk på **Legg til rot**. 
18. I **Navn**-feltet skriver du inn «Intrastat». 
19. Velg **Intrastat**-tabellposter. 
20. Klikk **OK**. 

> [!NOTE]
> Bare to tabeller ble tilbudt siden bare to tabeller ble lagt til i settet med metadata som brukes for øyeblikket. 

21. Klikk på **Bind**. 
22. Utvid **Intrastat** i treet. 
23. Velg **Intrastat\AmountMST** i treet. 
24. Utvid **Transaksjon = Intrastat** i treet. 
25. Velg **Transaksjon = Intrastat \ Fakturert beløp** i treet. 
26. Klikk på **Bind**. 
27. Velg **Intrastat\TransDate** i treet. 
28. Velg **Transaksjon = Intrastat\Dato** i treet. 
29. Klikk på **Bind**. 
30. Utvid **Intrastat\>Relasjoner** i treet. 
31. Utvid **Intrastat\>Relasjoner\IntrastatCommodity** i treet. 
32. Velg **Intrastat\>Relasjoner\IntrastatCommodity\Kode** i treet. 
33. Velg **Transaksjon = Intrastat\Artikkelkode** i treet. 
34. Klikk på **Bind**. 
35. Klikk på **Valider**. 

> [!NOTE]
> Vi har bundet elementer i datamodellen til elementer i datakildene som er beskrevet, ved å bruke detaljer i programmetadataene fra ER-metadatakonfigurasjonen det henvises til. 
36. Klikk **Lagre**. 
37. Lukk siden. 
38. Lukk siden. 
39. Når du må utvide det eksisterende settet med metadata, kan du gjøre det i Finance and Operations. Du kan deretter eksportere den nye, fullførte versjonen av ER-metadatakonfigurasjonen fra Finance and Operations, importere den til RCS og oppdatere forutsetningene for den konfigurerte modelltilordningskonfigurasjon slik at den henviser til en ny versjon av den importerte metadatakonfigurasjonen. 

> [!NOTE]
> Denne måten å hente informasjon om programmetadata på er den eneste tilgjengelige for lokalt distribuerte programmer (når lokale forretningsdata (LBD) eller en lokal distribusjonsmodell brukes for Dynamics 365 for Finance and Operations).
        
