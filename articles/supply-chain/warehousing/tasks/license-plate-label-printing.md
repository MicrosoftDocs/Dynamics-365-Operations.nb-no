---
title: Aktivere utskrift av nummerskiltetikett
description: Dette emnet viser hvordan du aktiverer automatisk utskrift av en SSCC-etikett (Serial Shipping Container Code) etter at den siste varen er plukket fra lageret i en arbeidsprosess for salgsplukk.
author: perlynne
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5580edb3324f76f04140bd6793bddaace5fadcf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977119"
---
# <a name="enable-license-plate-label-printing"></a>Aktivere utskrift av nummerskiltetikett

[!include [banner](../../includes/banner.md)]

Dette emnet viser hvordan du aktiverer automatisk utskrift av en SSCC-etikett (Serial Shipping Container Code) etter at den siste varen er plukket fra lageret i en arbeidsprosess for salgsplukk. Du kan kjøre denne prosedyren i demonstrasjonsdataselskapet USMF. Hvis du skal kjøre det på dine egne data, må du ha en nummerserie som er definert for nummerskilt. Du må definere en etikettskriver før du begynner. Gå til Organisasjonsstyring > Oppsett > Nettverksskrivere. I handlingsruten velger du Alternativer, og deretter klikker du Last ned installasjonsprogram for dokumentrutingsagent. Kjør installasjonsprogrammet og kontroller at du har en fungerende skriver satt til Aktiv før du fortsetter med prosedyren.


## <a name="set-up-the-gs1-company-prefix"></a>Angi GS1-firmaprefikset
1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Lagerstyringsparametere**.
2. I feltet **GS1-firmaprefiks** angir du det 7-sifrede GS1-firmanummeret.
3. Velg **Lagre**.
4. Lukk siden.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>Konfigurasjon av nummerserien for SSCC-skiltnummeret
1. Gå til **Navigasjonsrute > Moduler > Organisasjonsadministrasjon > Nummerserier > Nummerserier**.
2. Velg et alternativ i **Område**-feltet.
3. Velg et alternativ i **Referanse**-feltet.
4. Skriv inn en verdi i feltet **Firma.**
5. Utvid seksjonen **Segmenter**.
6. Velg **Rediger**.
7. Merk den første raden i tabellen **Segmenter**.
8. Velg **Fjern**.
9. Velg **Fjern**.
10. Velg **Lagre**.
11. Lukk siden.

## <a name="create-the-document-route-layout"></a>Opprett dokumentruteoppsettet
1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Dokumentruting > Dokumentrutingsoppsett**. Aktiver SSCC-oppsettet.  
2. Velg **Ny**.
3. Skriv inn en verdi i feltet **Oppsett-ID**.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Velg **Sett inn i slutten av teksten**.
6. Velg **Lagre**.
7. Lukk siden.

## <a name="set-up-the-document-routing"></a>Konfigurer dokumentrutingen
1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Dokumentruting > Dokumentruting**.
2. Velg et alternativ i feltet **Arbeidsordretype**.
3. Velg **Ny**.
4. Skriv inn en verdi i **Lager**-feltet.
5. Skriv inn en verdi i **Navn**-feltet.
6. Velg **Ny**.
7. Angi eller velg en verdi i feltet **Oppsett-ID**.
8. I **Navn**-feltet angir du navnet på skriveren du vil bruke.
9. Velg **Lagre**.
10. Lukk siden.

## <a name="create-mobile-device-menu"></a>Opprett mobilenhetsmeny
1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Mobilenhet > Menyelementer på mobilenheten**.
2. Velg **Ny**.
3. Skriv inn en verdi i feltet **Menyelementnavn**.
4. Skriv inn en verdi i **Tittel**-feltet.
5. Velg et alternativ i **Modus**-feltet.
6. Velg **Ja** i feltet **Bruk eksisterende arbeid**.
7. Velg **Ja** i **Generer nummerskilt**-feltet.
8. Utvid **Arbeidsklasser**-delen.
9. Velg **Ny**.
10. Skriv inn en verdi i feltet **Arbeidsklasse-ID**.
11. Velg **Lagre**.
12. Lukk siden.
13. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Mobilenhet > Meny på mobilenheten**.
14. Velg menyelementet du opprettet tidligere, i treet.
15. Velg **Rediger**.
16. Velg pilen for å legge til menyelementet i menyen.
17. Velg **Lagre**.
18. Lukk siden.

## <a name="update-a-work-template"></a>Oppdater en arbeidsmal
1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Oppsett > Arbeid > Arbeidsmaler**.
2. Velg **Rediger**.
3. Velg **Ny**.
4. Velg **Skriv ut** i **Arbeidstype**-feltet.
5. Angi eller velg en verdi i feltet **Arbeidsklasse-ID**.
6. Velg **Flytt opp**.
7. Velg **Lagre**.
8. Lukk siden.

