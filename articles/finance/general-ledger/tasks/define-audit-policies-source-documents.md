---
title: Definere overvåkingspolicyer for kildedokumenter
description: Dette emnet forklarer hvordan du angir og kjører overvåkingspolicyregler.
author: ryansandness
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba720fd1bbbbf8b4f3b936d65d9d7840432f291a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446477"
---
# <a name="define-audit-policies-for-source-documents"></a>Definere overvåkingspolicyer for kildedokumenter

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du angir og kjører overvåkingspolicyregler. Eksemplet bruker reiseregninger med utgiftstypen hotell. Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF. Revisorrollen inneholder de riktige tillatelsene for å kunne utføre disse oppgavene.

1. I navigasjonsruten går du til **Moduler > Arbeidsområde for overvåking > Oppsett > Type policyregel**.
2. Velg **Ny**.
3. Skriv inn en verdi i feltet **Regelnavn**.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. I **Spørringsnavn**-feltet velger du **Utgiftsrapportlinje**
6. I **Spørringstype**-feltet velger du **Mengde**
7. Velg **Juridisk enhet** i **Juridisk enhet**-feltet
8. I feltet **Referanse til dokumentdato** velger du **Endringsdato og -klokkeslett**
9. Velg **Lagre**.
10. I navigasjonsruten går du til **Moduler > Arbeidsområde for overvåking > Oppsett > Overvåkingspolicyer**.
11. Velg **Ny**.
12. Skriv inn en verdi i **Navn**-feltet.
13. Utvid delen **Policyorganisasjoner**.
14. Velg **Contoso Entertainment System USA** i treet, og velg deretter **Legg til**.
15. Velg **Contoso Consulting USA** i treet, og velg deretter **Legg til**.
16. Velg **Contoso Retail USA** i treet, og velg deretter **Legg til**.
17. Skjul delen **Policyorganisasjoner**.
18. Utvid delen **Policyregler**.
19. I listen finner og velger du policyregelen som ble opprettet tidligere.
20. Velg **Opprett policyregel**.
21. Angi dato og klokkeslett i feltet **Gyldighetsdato**.
22. Velg **Filter**.
23. Velg raden for **Utgiftskategori** i listen, og angi detaljene til **Hotell**.
24. Angi eller velg en verdi i **Kriterier**-feltet.
25. Velg fanen **Mengde**.
26. Velg **Legg til**.
27. I listen velger du en feltverdi av **transaksjonsbeløpet**.
28. Angi eller velg en verdi i **Felt**-feltet.
29. Velg **Summer** i **AggregateFunction**-feltet.
30. Velg **Grupper etter**-fanen.
31. Velg **Legg til**.
32. Velg en verdi for **Ansatt** i listen.
33. Velg **Legg til**.
34. Velg en verdi for **Utgiftskategori** i listen.
35. Angi eller velg en verdi i **Felt**-feltet.
36. Velg kategorien **Har**.
37. Velg **Legg til**.
38. Velg **Transaksjonsbeløp**.
39. Angi eller velg en verdi i **Felt**-feltet.
40. Velg **Summer** i **AggregateFunction**-feltet.
41. I **Kriterier**-feltet angir du `>2000`.
42. Velg **OK**.
43. Velg **Test**.
44. Angi dato og klokkeslett i feltet **Startdato for dokumentutvalg**.
45. Angi dato og klokkeslett i feltet **Sluttdato for dokumentutvalg**.
46. Velg **Kjør test**.
47. Klikk **Overvåkingspolicy** i handlingsruten.
48. Velg **Tilleggsalternativer**.
49. Angi dato og klokkeslett i **Startdato**-feltet.
50. Angi dato og klokkeslett i **Sluttdato**-feltet.
51. Velg **Parti**.
52. Vis delen **Kjør i bakgrunnen**.
53. Velg **Ja** i feltet **Satsvis behandling**.
54. Velg **OK**.
55. I navigasjonsruten går du til **Moduler > Arbeidsområde for overvåking > Overvåkingssaker**.
56. Finn og velg ønsket post i listen.
57. Vis delen **Tilknytninger**.
58. Finn og velg ønsket post i listen.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]