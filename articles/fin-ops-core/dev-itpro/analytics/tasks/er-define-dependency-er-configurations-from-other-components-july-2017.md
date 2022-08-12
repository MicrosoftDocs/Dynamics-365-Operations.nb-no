---
title: Definere avhengigheten av ER-konfigurasjonene i andre komponenter
description: Denne artikkelen beskriver hvordan du utformer en konfigurasjon for elektronisk rapportering (ER) og angir avhengigheten fra andre programvarekomponenter.
author: NickSelin
ms.date: 07/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aceb883e9182090a336c4c91aa0022a79495ce40
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111702"
---
# <a name="define-the-dependency-of-er-configurations-on-other-components"></a>Definere avhengigheten av ER-konfigurasjonene i andre komponenter

[!include [banner](../../includes/banner.md)]

For å fullføre disse trinnene, må du først fullføre trinnene i oppgaven TV-guiden ER behandle modellen tilordning konfigurasjoner, og du må ha tilgang til Microsoft Dynamics Lifecycle Services (LCS).

Denne fremgangsmåten viser hvordan du utformer en konfigurasjon for elektronisk rapportering (ER) og angi dens avhengighet fra andre programvarekomponenter, slik at du kan bidra til å sikre at konfigurasjonen skal lastes ned til en bestemt versjon av Finance and Operations. I dette eksemplet skal du opprette nødvendige ER-konfigurasjoner for eksempelfirmaet Litware, Inc. 

Denne fremgangsmåten er ment for brukere som har den systemansvarlige eller elektronisk rapportering utvikler-rolle tilordnet. Trinnene kan utføres i et hvilket som helst firma ettersom ER-konfigurasjoner deles mellom firmaer. 

1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
    * Kontroller at konfigurasjonstreet inneholder konfigurasjonen "Eksempel på datamodell" og underordnede elementer. Hvis ikke, fullfører du trinnene i oppgaven TV-guiden ER behandle modelltilordningskonfigurasjoner, og start veiledningen på nytt.   

## <a name="define-the-dependency-of-er-configurations-from-other-components"></a>Definere avhengigheten av ER-konfigurasjoner fra andre komponenter
1. Utvid 'Sample data model' i treet.
2. Velg 'Sample data model\Sample mapping' i treet.
    * Vi valgte utkastversjonen av konfigurasjon for tilordning av tilordning av prøven. Nå vil vi definerer sin avhengighet fra andre programvarekomponenter. Dermed regnes som en forutsetning for å kontrollere nedlastingen av denne konfigurasjonen versjon fra en database ER og noen ytterligere bruk av denne versjonen.   
3. Utvid seksjonen Forutsetninger.
    * Legg merke til at gruppen Forutsetninger for implementasjoner er lagt til automatisk i dette trinnet. Denne gruppen inneholder den nødvendige komponenten som refererer til den overordnede data konfigurasjonen og har Implementering-flagget aktivert. Dette flagget angir at tilordningskonfigurasjonen "Eksempel på tilordning" regnes som implementeringen av datamodellen "Eksempel på datamodell". Denne komponenten tvinger ER til å laste ned tilordningskonfigurasjonen "Eksempel på tilordning" fra et ER-lager hver gang modellkonfigurasjonen "Eksempel på datamodell" lastes ned.   
4. Klikk på Rediger
    * Enkelt avhengig av gjeldende versjon av en konfigurasjon fra en programvarekomponent som kan angis ved hjelp av definisjonen av komponentens type, og enten versjonen komponent eller et intervall av versjoner for komponenten.  
    * Ønsket avhengigheter kan grupperes. Når gruppering-type for "All" er valgt, regnes betingelsen avhengighet av denne gruppen oppfylles når betingelsene avhengighet fra denne gruppen og underordnede gruppen oppfylles. Når gruppering-type for "Én" er valgt, regnes betingelsen avhengighet av denne gruppen oppfylles når minst én avhengighetsbetingelse fra denne gruppen oppfylles.   
5. Klikk på Ny.
6. Velg den nødvendige komponenten for produktet.
7. Velg Microsoft Dynamics 365 for Operations (1611).
8. Skriv inn '[7.1.1541.3036,8)' i Versjon-feltet.
    * [7.1.1541.3036,8)  
    * Du angir avhengigheter blir evaluert når denne konfigurasjonen lastes ned fra en hvilken som helst ER repositoriet. Denne versjonen av konfigurasjonen skal lastes ned fra repositoriet ER når versjon 1 av "eksempel datamodellen-konfigurasjonen enten allerede er på plass eller lastet ned på forhånd. Hvis det er lastet ned på forhånd, må være fullført i Finance and Operations versjon 7.1.1541.3036 eller nyere, men må ikke overskride hovedversjon 8.   
9. Klikk på Lagre.
10. Lukk siden.
11. Klikk på Endre status.
12. Klikk på Fullført.
13. Klikk på OK.
14. Velg 'Sample data model\Sample mapping (alternative)' i treet.
15. Klikk på Rediger.
16. Klikk på Ny.
17. Velg den nødvendige komponenten for produktet.
18. Velg Microsoft Dynamics AX 7.0 RTW.
19. Skriv inn '[7.0.1265.3015,7.1)' i Versjon-feltet.
    * [7.0.1265.3015,7.1)  
    * Avhengigheter blir evaluert når denne konfigurasjonen lastes ned fra en hvilken som helst ER repositoriet. Denne versjonen av konfigurasjonen skal lastes ned fra repositoriet ER når versjon 1 av "eksempel datamodellen-konfigurasjonen enten allerede er på plass eller lastet ned på forhånd. Hvis den er lastet ned på forhånd, må den fullføres i Microsoft Dynamics 365 Finance, Enterprise edition er versjonen som må være 7.0.1265.3015 eller senere, men må ikke overskride underordnet versjon 1.   
20. Klikk på Lagre.
21. Lukk siden.
22. Klikk på Endre status.
23. Klikk på Fullført.
24. Klikk på OK.

## <a name="configure-the-er-repository"></a>Konfigurere ER-lageret
1. Lukk siden.
2. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
    * Åpne listen over ER-repositorier for gjeldende ER-leverandør, Litware, Inc.  
3. Merk den valgte raden i listen.
4. Klikk på Repositorier.
5. Klikk på Vis filtre.
6. Angi filterverdien "LCS" i "Typenavn"-feltet ved hjelp av filteroperatoren "inneholder".
    * Hvis LCS-repositoriet allerede er registrert for gjeldende ER-leverandør, kan du hoppe over resten av trinnene i denne delaktivitet. Hvis LCS-repositoriet ikke allerede er registrert, fullfører du resten av trinnene.   
7. Klikk på Legg til for å åpne nedtrekksdialogen.
8. Angi LCS i feltet Type konfigurasjonsrepositorium.
9. Klikk på Opprett repositorium.
10. Angi eller velg en verdi i feltet Prosjekt.
    * Velg ønsket LCS-prosjekt fra oppslaget i feltet "Prosjekt".  
11. Klikk på OK.
12. Lukk siden.

## <a name="upload-configurations-to-lcs"></a>Laste opp konfigurasjoner til LCS
1. Klikk på Rapporteringskonfigurasjoner.
2. Velg 'Sample data model' i treet.
3. Velg den fullførte versjonen av denne konfigurasjonen.
4. Klikk på Endre status.
5. Klikk på Del.
6. Klikk på OK.
    * Versjon 1 av denne konfigurasjon er lastet opp til LCS ved hjelp av prosjektet LCS for ER lageret som tidligere ble konfigurert.   
7. Utvid 'Sample data model' i treet.
8. Velg 'Sample data model\Sample mapping' i treet.
9. Velg den fullførte versjonen av denne konfigurasjonen.
10. Klikk på Endre status.
11. Klikk på Del.
12. Klikk på OK.
    * Versjon 1.1 av denne modelltilordningskonfigurasjon er lastet opp til LCS ved hjelp av prosjektet LCS for ER lageret som tidligere ble konfigurert.   
13. Velg 'Sample data model\Sample mapping (alternative)' i treet.
14. Velg den fullførte versjonen av denne konfigurasjonen.
15. Klikk på Endre status.
16. Klikk på Del.
17. Klikk på OK.
    * Versjon 1.1 av denne modelltilordningskonfigurasjon er lastet opp til LCS ved hjelp av prosjektet LCS for ER lageret som tidligere ble konfigurert.   

## <a name="evaluate-er-configuration-dependencies"></a>Evaluere avhengigheter i ER-konfigurasjonen
Vi skal slette opprettede konfigurasjoner fra systemet og laste dem ned fra LCS repositoriet.  
1. Velg 'Sample data model\Sample mapping' i treet.
2. Klikk på Slett.
3. Klikk på Ja.
4. Velg 'Sample data model\Sample mapping (alternative)' i treet.
5. Klikk på Slett.
6. Klikk på Ja.
7. Velg 'Sample data model\Sample format' i treet.
8. Klikk på Slett.
9. Klikk på Ja.
10. Velg 'Sample data model' i treet.
11. Klikk på Slett.
12. Klikk på Ja.
13. Lukk siden.
    * Åpne listen over ER-repositorier for gjeldende ER-leverandør, Litware, Inc.  
14. Klikk på Repositorier.
15. Klikk på Vis filtre.
16. Angi filterverdien "LCS" i "Typenavn"-feltet ved hjelp av filteroperatoren "inneholder".
17. Klikk på Åpne.
18. Velg 'Sample data model' i treet.
    * Vær oppmerksom på at du kan vise en evaluering av om nødvendige betingelser er oppfylt for hver versjon av ER konfigurasjonene for den gjeldende databasen. Hvis du vil vise denne vurderingen, klikker du boksen forutsetninger.   
19. Klikk på Kontroller forutsetninger.
20. Klikk på Importer.
21. Klikk på Ja.
22. Lukk siden.
23. Lukk siden.
24. Lukk siden.
25. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
26. Utvid 'Sample data model' i treet.
    * Legg merke til at modelltilordningskonfigurasjon "Eksempeltilordning" er lastet ned sammen med konfigurasjonen for de valgte dataene. De to filene lastes ned sammen fordi tilordning av eksemplet er definert som implementerer den valgte datamodellen og fordi den er tilgjengelig for programmet. Eksempel på tilordning (alternativ)-konfigurasjonen er ikke lastet ned fordi betingelsen for den nødvendige programversjonen ikke er oppfylt.   
    * Hvis du logger på Finance and Operations, registrerer samme leverandør, får tilgang til samme LCS-prosjekt og laster ned den samme datamodellkonfigurasjonen, vil konfigurasjonen for eksempeltilordning (alternativ) lastes ned, mens tilordningen av konfigurasjonen for eksempeltilordning vil bli hoppet over.  

## <a name="additional-resources"></a>Tilleggsressurser

[Administrere livssyklus til konfigurasjoner for elektronisk rapportering (ER)](../general-electronic-reporting-manage-configuration-lifecycle.md)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

