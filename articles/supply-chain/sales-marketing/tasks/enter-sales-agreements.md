---
title: Angi salgsavtaler
description: Dette emnet viser hvordan du oppretter en salgsavtale som forplikter en av kundene dine til å kjøpe et produkt til et avtalt beløp over tid, i bytte mot spesialrabatter.
author: omulvad
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm, SalesAgreementCustomerReferencesPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cdeddc915dc5ebfddf18a5e446f54b028b02325e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260413"
---
# <a name="enter-sales-agreements"></a>Angi salgsavtaler

[!include [banner](../../includes/banner.md)]

Dette emnet viser hvordan du oppretter en salgsavtale som forplikter en av kundene dine til å kjøpe et produkt til et avtalt beløp over tid, i bytte mot spesialrabatter. Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.


## <a name="set-up-sales-agreement-header"></a>Definere topptekst i salgsavtale
1. I navigasjonsruten går du til **Moduler > Salg og markedsføring > Salgsavtaler > Salgsavtaler**.
2. Velg **Ny**.
3. Velg det ønskede oppslaget på rullegardinmenyen i **Kundekonto**-feltet.
4. Velg det ønskede oppslaget på rullegardinmenyen i **Salgsavtaleklassifisering**-feltet.
5. Utvid delen **Generelt**.
6. Velg **Produktverdiforpliktelse** i feltet **Standardforpliktelse**. En forpliktelsestype er et obligatorisk vilkår som du må tilordne til avtalen for å definere hvordan avtalekontrakten skal oppfylles. De fire forhåndsdefinerte typene lar deg definere kundens forpliktelsesmål, uttrykt som et antall eller en verdi. Forpliktelsestypen for antall kan bare brukes for et bestemt produkt, men de verdibaserte typene gjelder for salg av både spesifikke og ikke-spesifikke produkter.  
7. I **Utløpsdato**-feltet kan du sette datoen til en fremtidig dato som du vil at avtalen skal utløpe på.
8. Velg **OK**.

## <a name="set-up-product-value-commitment-lines"></a>Definere produktverdiforpliktelseslinjer
1. Velg **Legg til linje**.
2. Velg det ønskede oppslaget fra rullegardinmenyen i **Varenummer**-feltet. Typen forpliktelse som du har valgt for avtalen, påvirker hva slags informasjon du kan angi for avtalelinjene. For en verdibasert avtale må du for eksempel angi det totale nettobeløpet (i valutaen som er avtalt) som kunden har forpliktet seg til ved kjøpet av varer fra deg. I dette eksemplet vil feltene **Antall** og **Enhet** på linjen være utilgjengelige fordi du oppretter en avtale for kunden om å kjøpe en bestemt verdi av et produkt.   
3. Angi pengebeløpet som kunden har forpliktet seg til å kjøpe, i **Nettobeløp**-feltet.
4. Angi en prosentverdi som skal gjelde for kundens salgsordrelinjer som er knyttet til denne avtalen, i **Rabattprosent**-feltet.
5. Vis delen **Linjedetaljer**.
6. Velg **Ja** i **Maks. håndheves**-feltet.
    - Hvis du velger **Maks. håndheves**, betyr det at totalbeløpet for alle salgsordrelinjene som bruker forpliktelsens spesialpriser, rabatter og/eller betalingsbetingelser, ikke må overskride beløpet som er angitt i forpliktelsen.  
    - Minimums- og maksimumsfrigivelsesbeløpene angir et verdiområde som må selges på hver salgsordre som bruker den valgte avtalen.   
7. Vis delen **Topptekst i salgsavtale**. Med mindre statusen for avtalen er satt til **Gjeldende**, kan ikke salgsordrer knyttes til avtalen, og derfor ikke bidra til oppfyllelse av avtalen. Du kan endre statusen manuelt på dette stadiet. Statusen vil imidlertid vanligvis endres når du bekrefter avtalen for kunden.  
8. Velg **Salgsavtale** i handlingsruten.
9. Velg **Bekreftelse**. Kontroller at alternativet **Merk avtale som gyldig** er satt til **Ja**.  
10. Velg **Ja** i feltet **Skriv ut rapport**.
11. Velg **OK**.
12. Lukk siden. Avtalen er nå gyldig. Du kan begynne å koble kundens ordrer til avtalen for å motregne mot forpliktelsesmålet.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]