---
title: Undersøke/løse unntak
description: Leverandørfakturapolicyer kjøres når du posterer en leverandørfaktura ved hjelp av Leverandørfaktura-siden, og når du åpner siden for brudd på leverandørfakturapolicy.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c6f8c8dcf7a301c7fb2d095658ac96cd4a24dff
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567014"
---
# <a name="researchresolve-exceptions"></a>Undersøke/løse unntak

[!include [task guide banner](../../includes/task-guide-banner.md)]

Leverandørfakturapolicyer kjøres når du posterer en leverandørfaktura ved hjelp av Leverandørfaktura-siden, og når du åpner siden for brudd på leverandørfakturapolicy. Du kan også konfigurere av arbeidsflyt for leverandørfaktura for å kjøre leverandørfakturapolicyer hver gang du sender en faktura til arbeidsflyten. 

Leverandørfakturapolicyer gjelder ikke for fakturaer som ble opprettet i fakturaregisteret eller fakturajournalen. 

Validering av fakturakontroll bruker ikke leverandørfakturapolicyer, men defineres i stedet på siden Leverandørparametere.

Denne registreringen bruker demonstrasjonsfirmaet USMF. Rollen regnskapssjef leverandørreskontro eller regnskapssjef kan utføre disse trinnene. Før du begynner, må du kontrollere at konfigurasjonsnøkkelen for fakturasamsvar er valgt.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Forberede oppretting av leverandørfakturapolicyer
1. Gå til Leverandører > Oppsett > Leverandørparametere.
2. Klikk kategorien Fakturavalidering.
3. Merk av eller fjern merket for Oppdater fakturahodestatus automatisk.
4. Klikk OK.
5. Velg et alternativ i feltet Poster faktura med avvik.
6. Lukk siden.
7. Gå til Leverandører > Policyoppsett > Leverandørfakturapolicyer.
8. Klikk Parametere.
9. Klikk btnAdd.
10. Lukk siden.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Opprette policyregeltyper for leverandørfakturaer
1. Gå til Leverandører > Policyoppsett > Policyregeltyper for leverandørfaktura.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Regelnavn.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk rullegardinknappen i Spørringsnavn-feltet for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
7. Klikk koblingen i den valgte raden i listen.
8. Klikk Lagre.
9. Lukk siden.

## <a name="define-a-vendor-invoice-policy"></a>Definere en leverandørfakturapolicy
1. Gå til Leverandører > Policyoppsett > Leverandørfakturapolicyer.
2. Klikk Ny.
3. Skriv inn en verdi i Navn-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Vis eller skjul delen Policyorganisasjoner.
6. Velg "Contoso Entertainment System USA" i treet.
7. Klikk Legg til.
8. Vis eller skjul delen Policyregler.
9. Klikk Opprett policyregel.
10. Skriv inn en verdi i feltet Beskrivelse av policyregel.
11. Klikk Filter.
12. Klikk Legg til.
13. Merk den valgte raden i listen.
14. Klikk rullegardinknappen i Tabell-feltet for å åpne oppslaget.
15. Klikk koblingen i den valgte raden i listen.
16. Klikk rullegardinknappen i feltet Avledet tabell for å åpne oppslaget.
17. Klikk koblingen i den valgte raden i listen.
18. Klikk rullegardinknappen i Felt-feltet for å åpne oppslaget.
19. Skriv inn en verdi i Felt-feltet.
20. Lukk siden.
21. Skriv inn en verdi i Kriterier-feltet.
22. Klikk OK.
23. Klikk OK.
24. Lukk siden.
25. Lukk siden.

