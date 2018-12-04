--- 
title: "Definere overvåkingspolicyer for kildedokumenter"
description: "Denne fremgangsmåten viser hvordan du angir og kjører overvåkingspolicyregler."
author: ryansandness
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4b05f744120e940bfea3e92b8aac3e41fc8151d9
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="define-audit-policies-for-source-documents"></a>Definere overvåkingspolicyer for kildedokumenter

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du angir og kjører overvåkingspolicyregler. Eksemplet bruker reiseregninger med utgiftstypen hotell. Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF. Revisorrollen inneholder de riktige tillatelsene for å kunne utføre disse oppgavene.

1. Gå til Arbeidsområde for overvåking > Oppsett > Type policyregel.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Regelnavn.
4. Skriv inn en verdi i feltet Beskrivelse.
5. I Spørringsnavn-feltet velger du Utgiftsrapportlinje
6. I Spørringstype-feltet velger du Mengde
7. Velg Juridisk enhet i Juridisk enhet-feltet.
8. I feltet Referanse til dokumentdato velger du Endringsdato og -klokkeslett
9. Klikk Lagre.
10. Gå til Arbeidsområde for overvåking > Oppsett > Overvåkingspolicyer.
11. Klikk Ny.
12. Skriv inn en verdi i Navn-feltet.
13. Utvid delen Policyorganisasjoner.
14. Velg "Contoso Entertainment System USA" i treet.
15. Klikk Legg til.
16. Velg "Contoso Consulting USA" i treet.
17. Klikk Legg til.
18. Velg "Contoso Retail USA" i treet.
19. Klikk Legg til.
20. Skjul delen Policyorganisasjoner.
21. Utvid delen Policyregler.
22. I listen finner og velger du policyregelen som ble opprettet tidligere.
23. Klikk Opprett policyregel.
24. Angi dato og klokkeslett i feltet Gyldighetsdato.
25. Klikk Filter.
26. Velg raden for Utgiftskategori i listen, og angi detaljene til Hotell
27. Angi eller velg en verdi i Kriterier-feltet.
28. Klikk kategorien Mengde.
29. Klikk Legg til.
30. I listen velger du en feltverdi av transaksjonsbeløpet
31. Angi eller velg en verdi i Felt-feltet.
32. Velg Summer i AggregateFunction-feltet.
33. Klikk kategorien Grupper etter.
34. Klikk Legg til.
35. Velg en verdi for Ansatt i listen. 
36. Klikk Legg til.
37. Velg en verdi for Utgiftskategori i listen.
38. Angi eller velg en verdi i Felt-feltet.
39. Klikk kategorien Har.
40. Klikk Legg til.
41. Velg Transaksjonsbeløp
42. Angi eller velg en verdi i Felt-feltet.
43. Velg Summer i AggregateFunction-feltet.
44. Skriv inn >2000 i Kriterier-feltet.
45. Klikk OK.
46. Klikk Test.
47. Angi dato og klokkeslett i feltet Startdato for dokumentutvalg.
48. Angi dato og klokkeslett i feltet Sluttdato for dokumentutvalg.
49. Klikk Kjør test.
50. Klikk Overvåkingspolicy i handlingsruten.
51. Klikk Tilleggsalternativer.
52. Angi dato og klokkeslett i Startdato-feltet.
53. Angi dato og klokkeslett i Sluttdato-feltet.
54. Klikk Parti.
55. Utvid Kjør i bakgrunnen.
56. Velg Ja i feltet Satsvis behandling.
57. Klikk OK.
58. Gå til Arbeidsområde for overvåking > Overvåkingssaker.
59. Finn og velg ønsket post i listen.
60. Klikk koblingen i den valgte raden i listen.
61. Vis delen Tilknytning.
62. Finn og velg ønsket post i listen.
63. Klikk koblingen i den valgte raden i listen.


