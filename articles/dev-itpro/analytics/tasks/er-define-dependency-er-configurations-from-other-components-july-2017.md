--- 
title: Definere avhengigheten av konfigurasjoner fra andre komponenter for elektronisk rapportering (ER)
description: "For å fullføre disse trinnene, må du først fullføre trinnene i oppgaven TV-guiden ER behandle modellen tilordning konfigurasjoner, og du må ha tilgang til Microsoft Dynamics livssyklus tjenester (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7de5fbcaa9f287752e3ae4834eb48d622d263579
ms.openlocfilehash: 890f035a291dbec936594ceeabc5de284d160ad4
ms.contentlocale: nb-no
ms.lasthandoff: 10/25/2017

---
# <a name="define-the-dependency-of-configurations-from-other-components-for-electronic-reporting-er"></a>Definere avhengigheten av konfigurasjoner fra andre komponenter for elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

For å fullføre disse trinnene, må du først fullføre trinnene i oppgaven TV-guiden ER behandle modellen tilordning konfigurasjoner, og du må ha tilgang til Microsoft Dynamics livssyklus tjenester (LCS).

Denne fremgangsmåten viser hvordan du utformer en konfigurasjon for elektronisk rapportering (ER) og angi dens avhengighet fra andre programvarekomponenter, slik at du kan bidra til å sikre at konfigurasjonen skal lastes ned til en bestemt versjon av Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. I dette eksemplet skal du opprette nødvendige ER-konfigurasjoner for eksempelfirmaet Litware, Inc. 

Denne fremgangsmåten er ment for brukere som har den systemansvarlige eller elektronisk rapportering utvikler-rolle tilordnet. Trinnene kan utføres i et hvilket som helst firma ettersom ER-konfigurasjoner deles mellom firmaer. 

1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
    * Kontroller at konfigurasjonstreet inneholder konfigurasjonen "Eksempel på datamodell" og underordnede elementer. Hvis ikke, fullfører du trinnene i oppgaven TV-guiden ER behandle modelltilordningskonfigurasjoner, og start veiledningen på nytt.   

## <a name="define-the-dependency-of-er-configurations-from-other-components"></a>Definere avhengigheten av ER-konfigurasjoner fra andre komponenter
1. Utvid 'Sample data model' i treet.
2. Velg 'Sample data model\Sample mapping' i treet.
    * Vi valgte utkastversjonen av konfigurasjon for tilordning av tilordning av prøven. Nå vil vi definerer sin avhengighet fra andre programvarekomponenter. Dermed regnes som en forutsetning for å kontrollere nedlastingen av denne konfigurasjonen versjon fra en database ER og noen ytterligere bruk av denne versjonen.   
3. Utvid seksjonen Forutsetninger.
    * Legg merke til at gruppen Forutsetninger for implementasjoner er lagt til automatisk i dette trinnet. Denne gruppen inneholder den nødvendige komponenten som refererer til den overordnede data konfigurasjonen og har Implementering-flagget aktivert. Dette flagget angir at tilordningskonfigurasjonen "Eksempel på tilordning" regnes som implementeringen av datamodellen "Eksempel på datamodell". Denne komponenten tvinger ER til å laste ned tilordningskonfigurasjonen "Eksempel på tilordning" fra et ER-lager hver gang modellkonfigurasjonen "Eksempel på datamodell" lastes ned.   
4. Klikk Rediger.
    * Enkelt avhengig av gjeldende versjon av en konfigurasjon fra en programvarekomponent som kan angis ved hjelp av definisjonen av komponentens type, og enten versjonen komponent eller et intervall av versjoner for komponenten.  
    * Ønsket avhengigheter kan grupperes. Når gruppering-type for "All" er valgt, regnes betingelsen avhengighet av denne gruppen oppfylles når betingelsene avhengighet fra denne gruppen og underordnede gruppen oppfylles. Når gruppering-type for "Én" er valgt, regnes betingelsen avhengighet av denne gruppen oppfylles når minst én avhengighetsbetingelse fra denne gruppen oppfylles.   
5. Klikk Ny.
6. Velg den nødvendige komponenten for produktet.
7. Velg Microsoft Dynamics 365 for Operations (1611).
8. Skriv inn '[7.1.1541.3036,8)' i Versjon-feltet.
    * [7.1.1541.3036,8)  
    * Du angir avhengigheter blir evaluert når denne konfigurasjonen lastes ned fra en hvilken som helst ER repositoriet. Denne versjonen av konfigurasjonen skal lastes ned fra repositoriet ER når versjon 1 av "eksempel datamodellen-konfigurasjonen er enten allerede er på plass eller lastet ned på forhånd. Hvis det er lastet ned på forhånd, må være fullført i Finans og operasjonene, versjonen av disse må være 7.1.1541.3036 eller senere, men må ikke overskride overordnet versjon 8.   
9. Klikk Lagre.
10. Lukk siden.
11. Klikk Endre status.
12. Klikk Fullført.
13. Klikk OK.
14. Velg 'Sample data model\Sample mapping (alternative)' i treet.
15. Klikk Rediger.
16. Klikk Ny.
17. Velg den nødvendige komponenten for produktet.
18. Velg Microsoft Dynamics AX 7.0 RTW.
19. Skriv inn '[7.0.1265.3015,7.1)' i Versjon-feltet.
    * [7.0.1265.3015,7.1)  
    * Avhengigheter blir evaluert når denne konfigurasjonen lastes ned fra en hvilken som helst ER repositoriet. Denne versjonen av konfigurasjonen skal lastes ned fra repositoriet ER når versjon 1 av "eksempel datamodellen-konfigurasjonen er enten allerede er på plass eller lastet ned på forhånd. Hvis det er lastet ned på forhånd, må det være fullført i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, versjonen må være 7.0.1265.3015 eller senere, men må ikke overskride underordnet versjon 1.   
20. Klikk Lagre.
21. Lukk siden.
22. Klikk Endre status.
23. Klikk Fullført.
24. Klikk OK.

## <a name="configure-the-er-repository"></a>Konfigurere ER-lageret
1. Lukk siden.
2. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
    * Åpne listen over ER-repositorier for gjeldende ER-leverandør, Litware, Inc.  
3. Merk den valgte raden i listen.
4. Klikk Repositorier.
5. Klikk Vis filtre.
6. Angi filterverdien "LCS" i "Typenavn"-feltet ved hjelp av filteroperatoren "inneholder".
    * Hvis LCS-repositoriet allerede er registrert for gjeldende ER-leverandør, kan du hoppe over resten av trinnene i denne delaktivitet. Hvis LCS-repositoriet ikke allerede er registrert, fullfører du resten av trinnene.   
7. Klikk Legg til for å åpne nedtrekksdialogen.
8. Angi LCS i feltet Type konfigurasjonsrepositorium.
9. Klikk Opprett repositorium.
10. Angi eller velg en verdi i feltet Prosjekt.
    * Velg ønsket LCS-prosjekt fra oppslaget i feltet "Prosjekt".  
11. Klikk OK.
12. Lukk siden.

## <a name="upload-configurations-to-lcs"></a>Laste opp konfigurasjoner til LCS
1. Klikk Rapporteringskonfigurasjoner.
2. Velg 'Sample data model' i treet.
3. Velg den fullførte versjonen av denne konfigurasjonen.
4. Klikk Endre status.
5. Klikk Del.
6. Klikk OK.
    * Versjon 1 av denne konfigurasjon er lastet opp til LCS ved hjelp av prosjektet LCS for ER lageret som tidligere ble konfigurert.   
7. Utvid 'Sample data model' i treet.
8. Velg 'Sample data model\Sample mapping' i treet.
9. Velg den fullførte versjonen av denne konfigurasjonen.
10. Klikk Endre status.
11. Klikk Del.
12. Klikk OK.
    * Versjon 1.1 av denne modelltilordningskonfigurasjon er lastet opp til LCS ved hjelp av prosjektet LCS for ER lageret som tidligere ble konfigurert.   
13. Velg 'Sample data model\Sample mapping (alternative)' i treet.
14. Velg den fullførte versjonen av denne konfigurasjonen.
15. Klikk Endre status.
16. Klikk Del.
17. Klikk OK.
    * Versjon 1.1 av denne modelltilordningskonfigurasjon er lastet opp til LCS ved hjelp av prosjektet LCS for ER lageret som tidligere ble konfigurert.   

## <a name="evaluate-er-configuration-dependencies"></a>Evaluere avhengigheter i ER-konfigurasjonen
    * Vi skal slette opprettede konfigurasjoner fra systemet og laste dem ned fra LCS repositoriet.  
1. Velg 'Sample data model\Sample mapping' i treet.
2. Klikk Slett.
3. Klikk Ja.
4. Velg 'Sample data model\Sample mapping (alternative)' i treet.
5. Klikk Slett.
6. Klikk Ja.
7. Velg 'Sample data model\Sample format' i treet.
8. Klikk Slett.
9. Klikk Ja.
10. Velg 'Sample data model' i treet.
11. Klikk Slett.
12. Klikk Ja.
13. Lukk siden.
    * Åpne listen over ER-repositorier for gjeldende ER-leverandør, Litware, Inc.  
14. Klikk Repositorier.
15. Klikk Vis filtre.
16. Angi filterverdien "LCS" i "Typenavn"-feltet ved hjelp av filteroperatoren "inneholder".
17. Klikk Åpne.
18. Velg 'Sample data model' i treet.
    * Vær oppmerksom på at du kan vise en evaluering av om nødvendige betingelser er oppfylt for hver versjon av ER konfigurasjonene for den gjeldende databasen. Hvis du vil vise denne vurderingen, klikker du boksen forutsetninger.   
19. Klikk Kontroller forutsetninger.
20. Klikk Importer.
21. Klikk Ja.
22. Lukk siden.
23. Lukk siden.
24. Lukk siden.
25. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
26. Utvid 'Sample data model' i treet.
    * Legg merke til at den tilordning konfigurasjonen for tilordning av eksemplet er lastet ned sammen med konfigurasjonen for valgte dataene. De to filene lastes ned sammen fordi tilordning av eksemplet er definert som implementerer valgte datamodellen og fordi den er tilgjengelig for økonomi og operasjoner. Eksempel på tilordning (alternativ) konfigurasjonen ikke er lastet ned fordi betingelsen for versjonen nødvendige programmet ikke er oppfylt.   
    * Hvis du logger deg på Dynamics 365 for Finance and Operations, Enterprise edition, registrerer samme leverandør, får tilgang til samme LCS-prosjekt og laster ned den samme konfigurasjonen for data, lastes konfigurasjonen for eksempeltilordning (alternativ) ned, mens konfigurasjonen for eksempeltilordning vil bli hoppet over.  


