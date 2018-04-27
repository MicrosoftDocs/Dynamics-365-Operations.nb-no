--- 
title: "Endre format for å generere dokumenter med programdata"
description: "For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren \"ER generere dokumenter med oppdatering av programdata (del 3: endre modell og tilordning)\"."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6c7455e4293993f297aeede4d9d6a50f25ca6c07
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="modify-format-to-generate-documents-with-application-data"></a>Endre format for å generere dokumenter med programdata

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren "ER generere dokumenter med oppdatering av programdata (del 3: endre modell og tilordning)".

Trinnene i denne fremgangsmåten forklarer hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere et elektronisk dokument og oppdatere programdata. I denne fremgangsmåten skal du endre ER-konfigurasjonene for ikke bare å bruke dem til å generere elektroniske dokumenter, men også til å oppdatere programdata. Denne fremgangsmåten er opprettet for brukere med rollen som systemansvarlig eller elektronisk rapportering utvikler. Disse trinnene kan fullføres ved hjelp av DEMF-datasettet.


## <a name="modify-format-to-collect-details-of-reporting"></a>Endre formatet for å samle inn informasjon for rapportering
1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Utvid 'Intrastat (modell)' i treet.
3. Velg 'Intrastat (modell)\Intrastat (format)' i treet.
4. Klikk Utforming.
5. Utvid 'Fil' i treet.
6. Utvid 'Fil\Deklarasjon' i treet.
7. Velg 'Fil\Deklarasjon\Data' i treet.
8. Velg "Én mange" i feltet Multiplisitet.
    * Konfigurer dette formatelementet hvis du vil arkivere detaljer om Intrastat-rapporteringsprosessen. Dette elementet representerer overskriftsposten i arkivet.  
9. Utvid 'Fil\Deklarasjon\Data' i treet.
10. Velg 'Fil\Deklarasjon\Data\Element' i treet.
11. Velg "Null mange" i feltet Multiplisitet.
    * Konfigurer dette formatelementet hvis du vil arkivere detaljer om Intrastat-rapporteringsprosessen. Dette elementet representerer listen over arkiverte linjer.  
12. Utvid 'Fil\Deklarasjon\Data\Element' i treet.
13. Velg 'Fil\Deklarasjon\Data\Element\Dim1' i treet.
14. Velg Ja i feltet Ekskludert.
    * Du vil ikke arkivere disse dataene, slik at du kan utelate dette formatet elementet fra datakilden for Intrastat-rapportering detaljer.  
15. Utvid 'Fil\Deklarasjon\Data\Element\Dim1' i treet.
16. Utvid 'Fil\Deklarasjon\Data\Element\Dim1\egenskap' i treet.
17. Velg Ja i feltet Ekskludert.
18. Utvid 'Fil\Deklarasjon\Data\Element\Dim1\dato' i treet.
19. Velg Ja i feltet Ekskludert.
20. Velg 'Fil\Deklarasjon\Data\Element\Dim2' i treet.
21. Velg Ja i feltet Ekskludert.
22. Utvid 'Fil\Deklarasjon\Data\Element\Dim2' i treet.
23. Utvid 'Fil\Deklarasjon\Data\Element\Dim2\egenskap' i treet.
24. Velg Ja i feltet Ekskludert.
25. Utvid 'Fil\Deklarasjon\Data\Element\Dim2\kode' i treet.
26. Velg Ja i feltet Ekskludert.
27. Velg 'Fil\Deklarasjon\Data\Element\Dim3' i treet.
    * Flere formatelementer kan ha samme navn. For eksempel DIM. Du kan ikke eksplisitt gjenkjenne dem når du bruker dette formatet som en datakilde for å arkivere Intrastat-rapporteringsdetaljer, så du må definere alternative navn for disse formatelementene.   
28. I Navn-feltet skriver du inn Beløp.
    * Beløp  
29. Velg "Nøyaktig én" i feltet Multiplisitet.
30. Velg 'Fil\Deklarasjon\Data\Element\Dim4' i treet.
31. I Navn-feltet skriver du inn Element.
    * Vare  
32. Velg "Nøyaktig én" i feltet Multiplisitet.
    * I tillegg til utformingselementene format, må følgende Intrastat rapportering detaljer arkiveres: unik post-ID for hver rapportert artikkelvaren og navnet på den genererte filen. Fordi disse dataene ikke vil fylles ut i Intrastat-rapporten, må du legge til formatet som er knyttet til disse elementene for detaljer som kilde for dataelementer.  
33. Velg 'Fil\Deklarasjon\Data' i treet.
34. Klikk Legg til for å åpne nedtrekksdialogen.
35. Velg 'Datakilde\Element' i treet.
36. Skriv inn Filnavn i Navn-feltet.
    * Filnavn  
37. Velg Streng i Datatype-feltet.
38. Klikk OK.
39. Velg 'Fil\Deklarasjon\Data\Element' i treet.
40. Klikk Legg til vare.
41. Skriv inn "Artikkelpost-ID" i Navn-feltet.
    * Artikkelpost-ID  
42. Velg Int64 i Datatype-feltet.
43. Klikk OK.
44. Klikk kategorien Tilordning.
45. Velg 'Fil\Deklarasjon\Data\Filnavn' i treet.
46. Klikk Bind.
47. Utvid noden 'model' i treet.
48. Utvid 'modell\Transaksjoner' i treet.
49. Velg 'Fil\Deklarasjon\Data\Element = modell.Transaksjoner\Artikkelpost-ID' i treet.
50. Velg 'modell\Transaksjoner\Artikkelpost-ID' i treet.
51. Klikk Bind.
52. Klikk Lagre.

## <a name="modify-format-to-memorize-details-of-reporting"></a>Endre formatet for å lagre informasjon for rapportering
1. Klikk Tilordne format til modell.
2. Klikk Ny.
3. I feltet Definisjon, angir eller velger du rotelementet "For oppdatering av programdata".
    * For oppdatering av programdata  
4. Skriv inn "Tilordning til å oppdatere data" i Navn-feltet.
    * Tilordning til å oppdatere data  
5. Klikk Lagre.
    * Denne tilknytningen definerer hvordan detaljene for Intrastat-rapporten samles i datamodellen, strukturen som er angitt av valgte rotelementet "For oppdatering av programdata". Disse opplysningene, tilordningen modellen med samme rotelementet "For oppdatering av programdata" og retningen "til mål' vil bli brukt for oppdateringen av programdata. Programdataene oppdatering starter umiddelbart etter at utgående Intrastat-rapporten genereres. Legg merke til at programdataene oppdatere kan du hoppe over under kjøring, men datamodellen må være tom (som inneholder listen over tomme oppføringer).   
6. Klikk Utforming.
    * Legg merke til at formatet for utgående Intrastat-rapporten legges til som standard som en datakilde for tilordning av denne modellen.  
    * Bind elementene i rapporten utformet (presentert som en datakilde) elementer i datamodellen, som er filtrert basert på den valgte modellen rotelementet.  
7. Utvid "Arkivhode" i treet.
8. Utvid 'Arkivhode\Arkivlinjer' i treet.
9. Utvid 'format' i treet.
10. Utvid 'format\Deklarasjon: XML-element(Declaration)' i treet.
11. Utvid 'format\Deklarasjon: XML-element(Declaration)\Data: XML-element 1..* (Data)' i treet.
12. Utvid 'format\Deklarasjon: XML-element(Declaration)\Data: XML-element 1..* (Data)\Element: XML-element 0..* (Item)' i treet.
13. Utvid 'format\Deklarasjon: XML-element(Declaration)\Data: XML-element 1..* (Data)\Element: XML-element 0..* (Item)\Dim3: XML-Element 1..1 (Amount)' i treet.
14. Utvid 'format\Deklarasjon: XML-element(Declaration)\Data: XML-element 1..* (Data)\Element: XML-element 0..* (Item)\Dim4: XML-Element 1..1 (Item)' i treet.
15. Velg 'Arkivhode\Antall linjer' i treet.
16. Klikk Rediger.
17. Velg 'Liste\COUNT' i treet.
18. Klikk Legg til funksjon.
19. Utvid 'format' i treet.
20. Utvid 'format\Deklarasjon: XML-element(Declaration)' i treet.
21. Utvid 'format\Deklarasjon: XML-element(Declaration)\Data: XML-element 1..* (Data)' i treet.
22. Velg 'format\Deklarasjon: XML-element(Declaration)\Data: XML-element 1..* (Data)\Element: XML-element 0..* (Item)' i treet.
23. Klikk Legg til datakilde.
24. I Formel-feltet skriver du inn 'COUNT(format.Declaration.Data.Item)'.
    * COUNT(format.Declaration.Data.Item)  
25. Klikk Lagre.
26. Lukk siden.
27. Velg 'Arkivhode\Filnavn' i treet.
28. Velg 'format\Deklarasjon: XML-element(Declaration)\Data: XML-element 1..* (Data)\Filnavn: Elementstreng(File name)' i treet.
29. Klikk Bind.
30. Velg 'format\Deklarasjon: XML-element(Declaration)\Data: XML-element 1..* (Data)\Element: XML-element 0..* (Item)\Dim4: XML-element 1..1 (Item)\nummer: Streng(number)' i treet.
31. Velg 'Arkivhode\Arkivlinjer\Varenummer' i treet.
32. Klikk Bind.
33. Velg 'format\Deklarasjon: XML-element(Declaration)\Data: XML-element 1..* (Data)\Element: XML-element 0..* (Item)\Dim3: XML-element 1..1 (Amount)\verdi: Numerisk real(value)' i treet.
34. Velg 'Arkivhode\Arkivlinjer\Beløp' i treet.
35. Klikk Bind.
36. Velg 'format\Deklarasjon: XML-element(Declaration)\Data: XML-element 1..* (Data)\Element: XML-Element 0..* (Item)\Artikkelpost-ID: Element Int64(Commodity rec id)'.
37. Velg 'Arkivhode\Arkivlinjer\Artikkelpost-ID' i treet.
38. Klikk Bind.
39. Velg 'Arkivhode\Arkivlinjer' i treet.
40. Velg 'format\Deklarasjon: XML-element(Declaration)\Data: XML-element 1..* (Data)\Element: XML-element 0..* (Item)' i treet.
41. Klikk Bind.
42. Velg "Arkivhode" i treet.
43. Velg 'format\Deklarasjon: XML-element(Declaration)\Data: XML-element 1..* (Data)' i treet.
44. Klikk Bind.
45. Klikk Lagre.
46. Lukk siden.
47. Lukk siden.
48. Lukk siden.


