---
title: Definere leverandørfakturapolicyer
description: Dette emnet forklarer hvordan du konfigurerer leverandørfakturapolicyer.
author: ShivamPandey-msft
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c088f6e3fea7c218cfd2108d0f279bccf1292772
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816202"
---
# <a name="set-up-vendor-invoice-policies"></a>Definere leverandørfakturapolicyer

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer leverandørfakturapolicyer. Leverandørfakturapolicyer kjøres når du posterer en leverandørfaktura ved hjelp av Leverandørfaktura-siden, og når du åpner siden for brudd på leverandørfakturapolicy. Du kan også konfigurere av arbeidsflyt for leverandørfaktura for å kjøre leverandørfakturapolicyer hver gang du sender en faktura til arbeidsflyten. 

- Leverandørfakturapolicyer gjelder ikke for fakturaer som ble opprettet i fakturaregisteret eller fakturajournalen.  
- Validering av fakturakontroll bruker ikke leverandørfakturapolicyer, men defineres i stedet på siden Leverandørparametere.  
- Denne registreringen bruker demonstrasjonsfirmaet USMF. Rollen regnskapssjef leverandørreskontro eller regnskapssjef kan utføre disse trinnene. Før du begynner, må du kontrollere at konfigurasjonsnøkkelen for fakturasamsvar er valgt.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Forberede oppretting av leverandørfakturapolicyer
1. Gå til **Navigasjonsrute > Moduler > Leverandører > Oppsett > Leverandørparametere**.
2. Velg **Fakturavalidering**-fanen.
3. Merk av eller fjern merket for **Oppdater fakturahodestatus automatisk**.
4. Velg **OK**.
5. Velg et alternativ i feltet **Poster faktura med avvik**.
6. Lukk siden.
7. Gå til **Navigasjonsrute > Moduler > Leverandører > Policyoppsett > Leverandørfakturapolicyer**.
8. Velg **Parametre**.
9. Velg **Legg til**.
10. Lukk siden for å gå tilbake til startsiden.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Opprette policyregeltyper for leverandørfakturaer
1. Gå til **Navigasjonsrute > Moduler > Leverandører > Policyoppsett > Policyregeltyper for leverandørfaktura**.
2. Velg **Ny**.
3. Angi verdier i feltene **Regelnavn** og **Beskrivelse**.
4. I feltet **Spørringsnavn** velger du rullegardinknappen for å åpne oppslaget, og velg deretter den ønskede posten.
5. Velg **Lagre**.
6. Lukk siden for å gå tilbake til startsiden.

## <a name="define-a-vendor-invoice-policy"></a>Definere en leverandørfakturapolicy
1. Gå til **Navigasjonsrute > Moduler > Leverandører > Policyoppsett > Leverandørfakturapolicyer**.
2. Velg **Ny**.
3. Angi verdier i feltene **Navn** og **Beskrivelse**.
4. Vis eller skjul delen **Policyorganisasjoner**.
5. Velg **Contoso Entertainment System USA** i treet.
6. Velg **Legg til**.
7. Vis eller skjul delen **Policyregler**.
8. Velg **Opprett policyregel**.
9. Skriv inn en verdi i feltet **Beskrivelse av policyregel**.
10. Velg **Filter**.
11. Velg **Legg til**. Velg den ønskede posten.
12. I feltene **Tabell**, **Avledet tabell** og **Felt** velger eller angir du alternativer fra rullegardinmenyene.
13. Lukk siden.
14. Skriv inn en verdi i **Kriterier**-feltet.
15. Velg **OK**.
16. Velg **OK**.
17. Lukk sidene for å gå tilbake til startsiden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]