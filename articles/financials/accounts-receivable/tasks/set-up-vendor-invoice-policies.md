--- 
title: "Definer leverandørfakturapolicyer"
description: "Leverandørfakturapolicyer kjøres når du posterer en leverandørfaktura ved hjelp av Leverandørfaktura-siden, og når du åpner siden for brudd på leverandørfakturapolicy."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f51c117da75a0382a38e75154ecef758f9a5d6c1
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-vendor-invoice-policies"></a>Definer leverandørfakturapolicyer

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


