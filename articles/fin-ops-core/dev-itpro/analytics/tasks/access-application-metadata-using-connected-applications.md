---
title: Få tilgang til programmetadata ved hjelp av tilkoblede programmer
description: Trinnene i dette emnet forklarer hvordan en RCS-bruker (Regulatory Configuration Service) kan utforme en ny modelltilordning for elektronisk rapportering (ER) ved å bruke metadata i Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 751ac21dc056373e1cd89a5149bf38789134e0cc
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682147"
---
# <a name="access-application-metadata-by-using-connected-applications"></a>Få tilgang til programmetadata ved hjelp av tilkoblede programmer

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en RCS-bruker (Regulatory Configuration Service) i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan utforme en ny modelltilordning for elektronisk rapportering (ER) ved å bruke metadata i Finance and Operations. Du får tilgang til programmetadata på nettet ved å bruke det RCS-tilkoblede programmet. Et ER-modelltilordningseksempel blir konfigurert for å gi tilgang til utenrikshandelstransaksjoner. For å fullføre disse trinnene må du først fullføre trinnene i RCS i emnet [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md). Hvis du ikke har fullført trinnene i emnet [Få tilgang til programmetadata ved hjelp av ER-konfigurasjon](access-application-metadata-er-configuration.md), går du til [siden med eksempler på elektronisk rapportering](https://go.microsoft.com/fwlink/?linkid=862266) for å laste ned og lagre følgende ER-konfigurasjoner: Foreign trade metadata.xml, Foreign trade model.xml, Foreign trade mapping.xml og deretter fullføre trinnene i fremgangsmåten.

## <a name="prerequisites"></a>Forutsetninger
1. Gå til **Alle arbeidsområder** > **Elektronisk rapportering**. 
2. Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**. Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md). 

## <a name="get-required-er-configurations"></a>Hente nødvendige ER-konfigurasjoner
1. Klikk på **Rapporteringskonfigurasjoner**. 
2. Hvis du allerede har fullført trinnene i prosedyren [Få tilgang til programmetadata ved hjelp av en ER-konfigurasjon](access-application-metadata-er-configuration.md), har du allerede alle nødvendige ER-konfigurasjoner (konfigurasjoner for metadata, modell og tilordning for utenrikshandel) i gjeldende RCS-forekomst. Du kan hoppe over alle gjenstående trinn i denne underoppgaven. 
3. Klikk på **Veksle**. 
4. Klikk på **Last fra XML-fil**. 
5. Klikk på **Bla gjennom**, og velg filen **Foreign trade metadata.xml**. 
6. Klikk **OK**. 
7. Klikk på **Veksle**. 
8. Klikk på **Last fra XML-fil**. 
9. Klikk på **Bla gjennom**, og velg filen **Foreign trade model.xml**. 
10. Klikk **OK**. 
11. Klikk på **Veksle**. 
12. Klikk på **Last fra XML-fil**. 
13. Klikk på **Bla gjennom**, og velg filen **Foreign trade mapping.xml**. 
14. Klikk **OK**. 

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
10. Klikk **Lagre**. 
11. Når du kontrollerer tilkoblingen til det konfigurerte programmet, klikker du på koblingen **Klikk her for å koble til det valgte eksterne programmet** på siden **Koble til eksternt program**. 
12. Klikk på **Kontroller tilkobling**. 
13. Klikk **Lukk**. 
14. Etter at valideringen av tilkoblingen har lykkes, oppdateres versjons- og leietakerdetaljene for det konfigurerte programmet i gjeldende rutenett. 

## <a name="review-existing-model-mapping-configuration"></a>Se gjennom eksisterende modelltilordningskonfigurasjon
1. Lukk siden. 
2. Klikk på **Rapporteringskonfigurasjoner**. 
3. Utvid **Utenrikshandelsmodell** i treet. 
4. Velg **Utenrikshandelsmodell\Utenrikshandelstilordning** i treet. 
5. Utvid delen **Forutsetninger**. 

    > [!NOTE]
    > Denne tilordningen henviser til metadatakonfigurasjonen for øyeblikket. Programmetadata fra denne konfigurasjonen tilbys mens denne modelltilordningen utformes. 

6. Klikk **Utforming**. 
7. Klikk **Utforming**. 
8. I treet velger du **Dynamics 365 for Operations\Tabellposter**. 
9. Klikk på **Legg til rot**. 
10. Angi eller velg en verdi i **Tabell**-feltet. 

    > [!NOTE]
    > Denne tilordningen henviser til metadatakonfigurasjonen for øyeblikket. Programmetadata fra denne konfigurasjonen tilbys mens denne modelltilordningen utformes. 

11. Klikk på **Avbryt**. 
12. Lukk siden. 
13. Lukk siden. 

## <a name="assign-connected-application-to-model-mapping"></a>Tilordne tilkoblet program til modelltilordning 
1. Klikk **Rediger**. 
2. Velg programmet **MyConnectedApp**. 

    > [!NOTE]
    > Denne tilordningen henviser for øyeblikket til metadataene i det valgte tilkoblede programmet. Når den samme tilordningen henviser til metadatakonfigurasjonen og det tilkoblede programmet samtidig, brukes metadata for det tilkoblede programmet. 

3. Klikk **Utforming**. 
4. Klikk **Utforming**. 
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