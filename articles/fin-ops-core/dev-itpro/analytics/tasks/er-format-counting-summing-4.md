---
title: ER Konfigurere format for å utføre telling og summering (del 4 - Kjøre format)
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4256864db8af5d2851c1203c1a85d79fd270b6a8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184905"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4-run-format"></a>ER Konfigurere format for å utføre telling og summering (del 4: Kjøre format)

[!include [task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata. Denne fremgangsmåten kan utføres i firmaet DEMF.

For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Konfigurere format for å utføre telling og summering (del 3: Bruke beregninger for å lage utdata)".

Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a>Teste denne konfigurasjonen for generering av Intrastat-rapporter
1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
2. Klikk Rapporteringskonfigurasjoner.
3. Utvid Intrastat-modell i treet.
4. Utvid Intrastat-modell\Intrastat (DE) i treet.
5. Velg Intrastat-modell\Intrastat (DE)\Intrastat (DE) med telling og summering i treet.
6. Klikk Konfigurasjoner i handlingsruten.
7. Klikk Brukerparametere.
8. Velg Ja i feltet Kjøringsinnstillinger.
9. Klikk OK.
10. Klikk Rediger.
11. Velg Ja i feltet Kjøringsutkast.
12. Klikk Lagre.
13. Gå til Avgift > Oppsett > Utenrikshandel > Utenrikshandelsparametere.
14. Utvid delen Elektronisk rapportering.
15. Velg konfigurasjonen Intrastat (DE) med telling og summering.
16. Velg konfigurasjonen Intrastat (DE) med telling og summering.
17. Klikk Lagre.
18. Lukk siden.
19. Gå til Avgift > Deklareringer > Utenrikshandel > Intrastat.
20. Klikk Utlevering.
21. Klikk Rapport.
    * Kjør prosessen for generering av Intrastat-rapport.  
22. Angi datoen som 2000-01-01 i feltet Fra dato.
    * Definer start- og sluttdatoer for rapporteringsperioden som inkluderer eksisterende på skjematransaksjonene.  
23. Angi datoen som 2022-12-31 i feltet Til dato.
    * Definer start- og sluttdatoer for rapporteringsperioden som inkluderer eksisterende på skjematransaksjonene.  
24. Velg Ankomster i feltet Retning.
25. Velg Ja i feltet Generer fil.
26. Klikk OK.
    * Se gjennom de opprettede utdataene med summeringslinjene på slutten.  
27. Klikk Ny.
28. Merk den valgte raden i listen.
29. Velg Fordelinger i feltet Retning.
30. Angi eller velg en verdi i Varenummer-feltet.
31. Angi eller velg en verdi i feltet Artikkel.
32. Sett vekt til 10.
33. Sett fakturabeløp til 10 000.
34. Sett statistisk beløp til 10 000.
35. Klikk Utlevering.
36. Klikk Rapport.
37. Velg Fordelinger i feltet Retning.
38. Klikk OK.
    * Se gjennom de opprettede utdataene med summeringslinjene på slutten. Vær oppmerksom på at det har blitt endret sammenlignet med første kjøring.  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a>Kjøre denne konfigurasjonen i feilsøkingsmodus for å gå gjennom innsamlede tellings- og summeringsdata
1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Utvid Intrastat-modell i treet.
3. Utvid Intrastat-modell\Intrastat (DE) i treet.
4. Velg Intrastat-modell\Intrastat (DE)\Intrastat (DE) med telling og summering i treet.
5. Klikk Konfigurasjoner i handlingsruten.
6. Klikk Brukerparametere.
7. Velg Ja i feltet Kjør i feilsøkingsmodus.
8. Klikk OK.
9. Lukk siden.
10. Gå til Avgift > Deklareringer > Utenrikshandel > Intrastat.
11. Klikk Utlevering.
12. Klikk Rapport.
13. Klikk OK.
14. Lukk siden.
15. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
16. Utvid Intrastat-modell i treet.
17. Utvid Intrastat-modell\Intrastat (DE) i treet.
18. Velg Intrastat-modell\Intrastat (DE)\Intrastat (DE) med telling og summering i treet.
19. Klikk Feilsøkingslogger.
    * Vær oppmerksom på at det er opprettet en feilsøkingsloggpost for kjøringen av den valgte konfigurasjonen.  
20. Klikk Vedlegg.
21. Klikk Åpne.
    * Se gjennom den opprettede XML-filen som inneholder tellings- og summeringsdetaljer som ble samlet inn under kjøringen av den valgte konfigurasjonen.  
