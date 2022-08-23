---
title: Få tilgang til programmetadata ved hjelp av tilkoblede programmer
description: Trinnene i denne artikkelen forklarer hvordan en bruker av Regulatory Configuration Service kan utforme en ny modelltilordning for elektronisk rapportering ved å bruke metadata.
author: kfend
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: 1a935b96e247978fc2b2f9449d403c92bff35f17
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267880"
---
# <a name="access-application-metadata-by-using-connected-applications"></a>Få tilgang til programmetadata ved hjelp av tilkoblede programmer

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en RCS-bruker (Regulatory Configuration Service) i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan utforme en ny modelltilordning for elektronisk rapportering (ER) ved å bruke metadataene i økonomi og drift. Du får tilgang til programmetadata på nettet ved å bruke det RCS-tilkoblede programmet. Et ER-modelltilordningseksempel blir konfigurert for å gi tilgang til utenrikshandelstransaksjoner. For å fullføre disse trinnene må du først fullføre trinnene i RCS i artikkelen [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md). Hvis du ikke har fullført trinnene i artikkelen [Få tilgang til programmetadata ved hjelp av ER-konfigurasjon](access-application-metadata-er-configuration.md), laster du ned [siden med eksempler på elektronisk rapportering](https://download.microsoft.com/download/0/4/e/04e13839-e423-442b-a6c2-dd35b1045c2d/Dynamics%20365%20for%20Finance%20and%20Operations%208.1%20Electronic%20reporting%20task%20guides.zip) og lagrer følgende ER-konfigurasjoner: Foreign trade metadata.xml, Foreign trade model.xml, Foreign trade mapping.xml og deretter fullfører du trinnene i fremgangsmåten.

## <a name="prerequisites"></a>Forutsetninger
1. Gå til **Alle arbeidsområder** > **Elektronisk rapportering**. 
2. Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**. Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md). 

## <a name="get-required-er-configurations"></a>Hente nødvendige ER-konfigurasjoner
1. Klikk på **Rapporteringskonfigurasjoner**. 
2. Hvis du allerede har fullført trinnene i prosedyren [Få tilgang til programmetadata ved hjelp av en ER-konfigurasjon](access-application-metadata-er-configuration.md), har du allerede alle nødvendige ER-konfigurasjoner (konfigurasjoner for metadata, modell og tilordning for utenrikshandel) i gjeldende RCS-forekomst. Du kan hoppe over alle gjenstående trinn i denne underoppgaven. 
3. Klikk på **Veksle**. 
4. Klikk på **Last fra XML-fil**. 
5. Klikk på **Bla gjennom**, og velg filen **Foreign trade metadata.xml**. 
6. Klikk på **OK**. 
7. Klikk på **Veksle**. 
8. Klikk på **Last fra XML-fil**. 
9. Klikk på **Bla gjennom**, og velg filen **Foreign trade model.xml**. 
10. Klikk på **OK**. 
11. Klikk på **Veksle**. 
12. Klikk på **Last fra XML-fil**. 
13. Klikk på **Bla gjennom**, og velg filen **Foreign trade mapping.xml**. 
14. Klikk på **OK**. 

## <a name="register-a-connected-application"></a>Registrere et tilkoblet program
1. Lukk siden. 
2. Lukk siden. 
3. Gå til **Alle arbeidsområder** > **Elektronisk rapportering**. 
4. Klikk på **Tilkoblede programmer**. 
5. Kontroller at det konfigurerte programmet er basert på Azure, og at det er tilgjengelig for gjeldende RCS-bruker. Det kreves også at den gjeldende RCS-brukeren har tilgang til det valgte programmet og er registrert som en bruker av dette programmet, i en rolle som gir vedkommende tilgangsrettigheter til programmets metadata. 
6. Klikk på **Ny**. 
7. Skriv inn «MyConnectedApp» i **Navn**-feltet. 
8. I **Program**-feltet skriver du inn «https://mycompany.operations.dynamics.com». 
9. I **Leietaker**-feltet skriver du inn «mycompany.onmicrosoft.com». 
10. Klikk på **Lagre**. 
11. Når du kontrollerer tilkoblingen til det konfigurerte programmet, klikker du på koblingen **Klikk her for å koble til det valgte eksterne programmet** på siden **Koble til eksternt program**. 
12. Klikk på **Kontroller tilkobling**. 
13. Klikk på **Lukk**. 
14. Etter at valideringen av tilkoblingen har lykkes, oppdateres versjons- og leietakerdetaljene for det konfigurerte programmet i gjeldende rutenett. 

## <a name="review-existing-model-mapping-configuration"></a>Se gjennom eksisterende modelltilordningskonfigurasjon
1. Lukk siden. 
2. Klikk på **Rapporteringskonfigurasjoner**. 
3. Utvid **Utenrikshandelsmodell** i treet. 
4. Velg **Utenrikshandelsmodell\Utenrikshandelstilordning** i treet. 
5. Utvid delen **Forutsetninger**. 

    > [!NOTE]
    > Denne tilordningen henviser til metadatakonfigurasjonen for øyeblikket. Programmetadata fra denne konfigurasjonen tilbys mens denne modelltilordningen utformes. 

6. Klikk på **Utforming**. 
7. Klikk på **Utforming**. 
8. I treet velger du **Dynamics 365 for Operations\Tabellposter**. 
9. Klikk på **Legg til rot**. 
10. Angi eller velg en verdi i **Tabell**-feltet. 

    > [!NOTE]
    > Denne tilordningen henviser til metadatakonfigurasjonen for øyeblikket. Programmetadata fra denne konfigurasjonen tilbys mens denne modelltilordningen utformes. 

11. Klikk på **Avbryt**. 
12. Lukk siden. 
13. Lukk siden. 

## <a name="assign-connected-application-to-model-mapping"></a>Tilordne tilkoblet program til modelltilordning 
1. Klikk på **Rediger**. 
2. Velg programmet **MyConnectedApp**. 

    > [!NOTE]
    > Denne tilordningen henviser for øyeblikket til metadataene i det valgte tilkoblede programmet. Når den samme tilordningen henviser til metadatakonfigurasjonen og det tilkoblede programmet samtidig, brukes metadata for det tilkoblede programmet. 

3. Klikk på **Utforming**. 
4. Klikk på **Utforming**. 
5. I treet velger du **Dynamics 365 for Operations\Tabellposter**. 
6. Klikk på **Legg til rot**. 
7. Angi eller velg en verdi i **Tabell**-feltet. 

    > [!NOTE]
    > Nå ble flere enn to programtabeller tilbudt siden denne tilordningen bruker alle metadataene i det tilkoblede programmet som er tilordnet for den. 

8. Klikk på **Avbryt**. 
9. Klikk på **Valider**. 

    > [!NOTE]
    > Vi har bundet elementer i datamodellen til elementer i datakildene som er beskrevet, ved å bruke detaljer i metadata for det tilkoblede programmet som er tilordnet for denne tilordningen. 

10. Lukk siden. 
11. Lukk siden. 

Når du må evaluere denne modelltilordningen ved å bruke metadata for en annen versjon av programmet, registrerer du et nytt tilkoblet program, tilordner det til denne modelltilordningen og validerer det mot de nye metadataene.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

