---
title: Undersøke eller løse unntak
description: Leverandørfakturapolicyer kjøres når du posterer en leverandørfaktura ved hjelp av Leverandørfaktura-siden, og når du åpner siden for brudd på leverandørfakturapolicy.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32ff53198f61e1d1af3c437e9488c2a246cf820a
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2022
ms.locfileid: "8110025"
---
# <a name="research-or-resolve-exceptions"></a>Undersøke eller løse unntak

[!include [banner](../../includes/banner.md)]

Leverandørfakturapolicyer kjøres når du posterer en leverandørfaktura ved hjelp av **Leverandørfaktura**-siden, og når du åpner **Policybrudd**-siden for leverandørfaktura. Du kan også konfigurere av arbeidsflyt for leverandørfaktura for å kjøre leverandørfakturapolicyer hver gang du sender en faktura til arbeidsflyten. 

Leverandørfakturapolicyer gjelder ikke for fakturaer som ble opprettet i **Fakturaregister** eller **Fakturajournal**. 

Validering av fakturakontroll bruker ikke leverandørfakturapolicyer, men defineres i stedet på siden **Leverandørparametere**.

Denne registreringen bruker demonstrasjonsfirmaet USMF. Rollen regnskapssjef leverandørreskontro eller regnskapssjef kan utføre disse trinnene. Før du begynner, må du kontrollere at **Konfigurasjonsnøkkel for fakturakontroll** er valgt.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Forberede oppretting av leverandørfakturapolicyer
1. Gå til **Leverandører > Oppsett > Leverandørparametere**.
2. Klikk på fanen **Fakturavalidering**.
3. Merk av eller fjern merket for **Oppdater fakturahodestatus automatisk**.
4. Klikk på **OK**.
5. Velg et alternativ i feltet **Poster faktura med avvik**.
6. Lukk siden.
7. Gå til **Leverandører > Policyoppsett > Leverandørfakturapolicyer**.
8. Klikk på **Parametere**.
9. Klikk på **Legg til**.
10. Lukk siden.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Opprette policyregeltyper for leverandørfakturaer
1. Gå til **Leverandører > Policyoppsett > Policyregeltyper for leverandørfaktura**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i feltet **Regelnavn**.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Klikk på rullegardinknappen i **Spørringsnavn**-feltet for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
7. Klikk på koblingen i den valgte raden i listen.
8. Klikk på **Lagre**.
9. Lukk siden.

## <a name="define-a-vendor-invoice-policy"></a>Definere en leverandørfakturapolicy
1. Gå til **Leverandører > Policyoppsett > Leverandørfakturapolicyer**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i **Navn**-feltet.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Vis eller skjul delen **Policyorganisasjoner**.
6. Velg "Contoso Entertainment System USA" i treet.
7. Klikk på **Legg til**.
8. Vis eller skjul delen **Policyregler**.
9. Klikk på **Opprett policyregel**.
10. Skriv inn en verdi i feltet **Beskrivelse av policyregel**.
11. Klikk på **Filter**.
12. Klikk på **Legg til**.
13. Merk den valgte raden i listen.
14. Klikk på rullegardinknappen i **Tabell**-feltet for å åpne oppslaget.
15. Klikk på koblingen i den valgte raden i listen.
16. Klikk på rullegardinknappen i feltet **Avledet tabell** for å åpne oppslaget.
17. Klikk på koblingen i den valgte raden i listen.
18. Klikk på rullegardinknappen i **Felt**-feltet for å åpne oppslaget.
19. Skriv inn en verdi i **Felt**-feltet.
20. Lukk siden.
21. Skriv inn en verdi i **Kriterier**-feltet.
22. Klikk på **OK**.
23. Klikk på **OK**.
24. Lukk siden.
25. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
