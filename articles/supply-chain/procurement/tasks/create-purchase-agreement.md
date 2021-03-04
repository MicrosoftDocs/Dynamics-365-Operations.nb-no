---
title: Opprette en kjøpsavtale
description: Dette emnet fører deg gjennom oppretting av en kjøpsavtale.
author: mkirknel
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1edfd4e56910376d0596eec5eff2af888f7dc98d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434351"
---
# <a name="create-a-purchase-agreement"></a>Opprette en kjøpsavtale

[!include [banner](../../includes/banner.md)]

Dette emnet fører deg gjennom oppretting av en kjøpsavtale. Dette gjøres vanligvis av en innkjøpssjef. Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Du må ha definert kjøpsavtaleklassifiseringer før du starter. Når du har opprettet en avtale, kan du bruke den når du oppretter en bestilling, og dette kopierer kjøpsavtalebetingelsene til hodet og linjene i rekkefølgen som er påvirket av avtalen.


## <a name="create-a-new-purchase-agreement"></a>Opprette en ny kjøpsavtale
1. Gå til **Navigasjonsrute > Moduler > Innkjøp og leverandører > Kjøpsavtaler > Kjøpsavtaler**.
2. Klikk på **Ny**.
3. I **Leverandørkonto**-feltet velger du raden i den ønskede posten på rullegardinmenyen.
4. I feltet **Klassifisering av kjøpsavtale** velger du raden i den ønskede posten på rullegardinmenyen.
5. Vis hurtigfanen **Generelt**.
6. Angi en dato i **Utløpsdato**-feltet.

    - Denne utløpsdatoen er standard for alle forpliktelseslinjene og bestemmer hvor lenge hver bestemte forpliktelse er gyldig.  

7. I feltet **Dokumenttittel** skriver du inn et navn for kjøpsavtalen.

    - La feltet **Standardforpliktelse** være satt til **Produktantallsforpliktelse** (eller endre det hvis det ikke er satt til dette).  
    - Standardforpliktelsesverdien bestemmer alternativene på avtalelinjene. Hvis du trenger en ny forpliktelsestype når du oppretter avtalelinjene, må du endre standard forpliktelsen i hodet. Det finnes 4 forskjellige forpliktelser: **Produktantallsforpliktelse** - for et bestemt antall av et produkt; **Produktverdiforpliktelse** - for et bestemt valutabeløp for et produkt; **Verdiforpliktelse for produktkategori** - for et bestemt valutabeløp i en innkjøpskategori der beløpet kan være for en katalogvare eller en ikke-katalogvare; **Verdiforpliktelse** - for et bestemt valutabeløp som kan bli oppfylt av et hvilket som helst produkt eller en hvilken som helst innkjøpskategori.  

8. Velg **OK**.

## <a name="add-a-commitment"></a>Legge til en forpliktelse
1. Velg **Legg til linje**.
2. Velg det ønskede oppslaget fra rullegardinmenyen i **Varenummer**-feltet.
3. Angi et tall i **Antall**-feltet. Dette er det totale antallet som du har avtalt å kjøpe fra leverandøren.  
4. Angi et tall i **Enhetspris**-feltet.
5. Vis delen **Linjedetaljer**.
6. Angi alternativet **Max Maks. håndheves** til **Ja**. **Maks. håndheves**-alternativet begrenser bruken av forpliktelse. Du kan bare kjøpe opptil antallet som er angitt i **Antall**-feltet for linjen.  

## <a name="add-header-conditions"></a>Legge til topptekstbetingelser
1. Velg **Alternativer** i handlingsruten.
2. Velg **Endre visning**.
3. Velg **Topptekstvisning**.
4. Utvid **Vilkår**-delen.
5. Velg det ønskede oppslaget på rullegardinmenyen **Betalingsmåte**. Betalingsbetingelsene fra leverandørkontoen vises her som standard.  
6. Velg det ønskede oppslaget på rullegardinmenyen i feltet **Leveringsmåte**.
7. Klikk rullegardinknappen i feltet **Leveringsbetingelser** for å åpne oppslaget.

## <a name="confirm-and-activate-the-agreement"></a>Kontrollere og aktivere avtalen
1. Klikk **Kjøpsavtale** i handlingsruten.
2. Velg **Bekreftelse**. Angi alternativet **Merk avtale som gyldig** som **Ja**.  
3. Velg **OK**.
4. Klikk **Kjøpsavtale** i handlingsruten.
5. Velg **Innkjøpsavtalebekreftelser**. Med alternativet **Forhåndsvis/Skriv ut** kan du generere et dokument for kjøpsavtalen som du deretter kan skrive ut eller sende til leverandøren. Hvis du oppdaterer avtalen senere, og bekrefter den på nytt, vil begge versjoner vises her.  
6. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]