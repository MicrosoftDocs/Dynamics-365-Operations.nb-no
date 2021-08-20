---
title: Endre formater for å generere dokumenter med programdata
description: Dette emnet beskriver hvordan du utformer konfigurasjoner for rapportering for å generere et elektronisk dokument og oppdatere programdata.
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 312a49fc524cc7359d2c1815597214656df11c018034da384d30bfb9d9efee4b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752417"
---
# <a name="modify-formats-to-generate-documents-that-have-application-data"></a>Endre formater for å generere dokumenter med programdata

[!include [banner](../../includes/banner.md)]

For å fullføre trinnene i denne fremgangsmåten, må du først fullføre prosedyren "ER generere dokumenter med oppdatering av programdata (del 3: endre modell og tilordning)".

Trinnene i denne fremgangsmåten forklarer hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere et elektronisk dokument og oppdatere programdata. I denne fremgangsmåten skal du endre ER-konfigurasjonene for ikke bare å bruke dem til å generere elektroniske dokumenter, men også til å oppdatere programdata. Denne fremgangsmåten er opprettet for brukere med rollen som systemansvarlig eller elektronisk rapportering utvikler. Disse trinnene kan fullføres ved hjelp av DEMF-datasettet.


## <a name="modify-format-to-collect-details-of-reporting"></a>Endre formatet for å samle inn informasjon for rapportering
1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Utvid 'Intrastat (modell)' i treet.
3. Velg 'Intrastat (modell)\Intrastat (format)' i treet.
4. Klikk på Utforming.
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
34. Klikk på Legg til for å åpne nedtrekksdialogen.
35. Velg 'Datakilde\Element' i treet.
36. Skriv inn Filnavn i Navn-feltet.
    * Filnavn  
37. Velg Streng i Datatype-feltet.
38. Klikk på OK.
39. Velg 'Fil\Deklarasjon\Data\Element' i treet.
40. Klikk på Legg til vare.
41. Skriv inn "Artikkelpost-ID" i Navn-feltet.
    * Artikkelpost-ID  
42. Velg Int64 i Datatype-feltet.
43. Klikk på OK.
44. Klikk på fanen Tilordning.
45. Velg 'Fil\Deklarasjon\Data\Filnavn' i treet.
46. Klikk på Bind.
47. Utvid noden 'model' i treet.
48. Utvid 'modell\Transaksjoner' i treet.
49. Velg 'Fil\Deklarasjon\Data\Element = modell.Transaksjoner\Artikkelpost-ID' i treet.
50. Velg 'modell\Transaksjoner\Artikkelpost-ID' i treet.
51. Klikk på Bind.
52. Klikk på Lagre.

## <a name="modify-format-to-memorize-details-of-reporting"></a>Endre formatet for å lagre informasjon for rapportering

1. Klikk på Tilordne format til modell.
2. Klikk på Ny.
3. I feltet Definisjon, angir eller velger du rotelementet "For oppdatering av programdata".
    * For oppdatering av programdata.
4. Skriv inn "Tilordning til å oppdatere data" i Navn-feltet.
    * Tilordning til å oppdatere data  
5. Klikk på Lagre.
    * Denne tilknytningen definerer hvordan detaljene for Intrastat-rapporten samles i datamodellen, strukturen som er angitt av valgte rotelementet "For oppdatering av programdata". Disse opplysningene, tilordningen modellen med samme rotelementet "For oppdatering av programdata" og retningen "til mål' vil bli brukt for oppdateringen av programdata. Programdataene oppdatering starter umiddelbart etter at utgående Intrastat-rapporten genereres. Programdataoppdateringen kan hoppes over under kjøring, men datamodellen må være tom (som inneholder listen over tomme oppføringer).
6. Klikk på Utforming.
    * Formatet for utgående Intrastat-rapport legges til som standard som en datakilde for tilordning av denne modellen.  
    * Bind elementene i den utformede rapporten (presentert som en datakilde) til elementer i datamodellen, som er filtrert basert på den valgte modellens rotelement.  
7. Utvid "Arkivhode" i treet.
8. Utvid 'Arkivhode\Arkivlinjer' i treet.
9. Utvid 'format' i treet.
10. Utvid 'format\Deklarasjon: XML-element(Declaration)' i treet.
11. Utvid 'format\Deklarasjon: XML-element(Declaration)\Data: XML-element 1..* (Data)' i treet.
12. Utvid 'format\Deklarasjon: XML-element(Declaration)\Data: XML-element 1..* (Data)\Element: XML-element 0..* (Item)' i treet.
13. Utvid 'format\Deklarasjon: XML-element(Declaration)\Data: XML-element 1..* (Data)\Element: XML-element 0..* (Item)\Dim3: XML-Element 1..1 (Amount)' i treet.
14. Utvid 'format\Deklarasjon: XML-element(Declaration)\Data: XML-element 1..* (Data)\Element: XML-element 0..* (Item)\Dim4: XML-Element 1..1 (Item)' i treet.
15. Velg 'Arkivhode\Antall linjer' i treet.
16. Klikk på Rediger.
17. Velg 'Liste\COUNT' i treet.
18. Klikk på Legg til funksjon.
19. Utvid 'format' i treet.
20. Utvid 'format\Deklarasjon: XML-element(Declaration)' i treet.
21. Utvid `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)` i treet.
22. Velg `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)` i treet.
23. Klikk på Legg til datakilde.
24. I Formel-feltet skriver du inn 'COUNT(format.Declaration.Data.Item)'.
    * COUNT(format.Declaration.Data.Item)  
25. Klikk på Lagre.
26. Lukk siden.
27. Velg 'Arkivhode\Filnavn' i treet.
28. Velg 'format\Deklarasjon: XML-element(Declaration)\Data: XML-element 1..* (Data)\Filnavn: Elementstreng(File name)' i treet.
29. Klikk på Bind.
30. Velg `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)\number: String(number)` i treet.
31. Velg 'Arkivhode\Arkivlinjer\Varenummer' i treet.
32. Klikk på Bind.
33. Velg `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)\value: Numeric Real(value)` i treet.
34. Velg 'Arkivhode\Arkivlinjer\Beløp' i treet.
35. Klikk på Bind.
36. Velg `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Commodity rec ID: Item Int64(Commodity rec ID)` i treet.
37. Velg 'Arkivhode\Arkivlinjer\Artikkelpost-ID' i treet.
38. Klikk på Bind.
39. Velg 'Arkivhode\Arkivlinjer' i treet.
40. Velg `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)` i treet.
41. Klikk på Bind.
42. Velg "Arkivhode" i treet.
43. Velg `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)` i treet.
44. Klikk på Bind.
45. Klikk på Lagre.
46. Lukk siden.
47. Lukk siden.
48. Lukk siden.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]