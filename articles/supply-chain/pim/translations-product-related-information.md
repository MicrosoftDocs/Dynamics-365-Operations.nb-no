---
title: Vanlige spørsmål for produktrelaterte oversettelser
description: Dette emnet beskriver hvordan du administrerer oversettelser for produkter, produktdimensjonsverdier og produktattributter.
author: cvocph
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList, EcoResProductListPage, EcoResProductVariants, EcoResProductDetailsExtended, EcoResProductCreate, EcoResProductDetails, RetailSizeGroupTable, RetailStyleGroupTable, RetailColorGroupTable, PCTranslationLanguageLookup, EcoResProductCategory
audience: Application User
ms.reviewer: kamaybac
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29c191a3dcdb13ba54be3077d7e24706673bc14be659d39595e199fff0176930
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758502"
---
# <a name="product-related-translations-faq"></a>Vanlige spørsmål for produktrelaterte oversettelser

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du administrerer oversettelser for produkter, produktdimensjonsverdier og produktattributter. 

## <a name="what-product-related-data-can-be-translated"></a>Hvilke produktrelaterte data kan oversettes?

Du kan opprette oversettelser for følgende produktrelaterte informasjon:
-   Navn og beskrivelser av produktene.
-   Beskrivelser, egendefinerte navn og hjelpetekst for produktattributtverdier.
-   Navn og beskrivelser for produktdimensjonsverdier.

Du kan oversette den produktrelaterte informasjonen til et annet språk som er tilgjengelig fra siden **Tekstoversettelse**. Hvis du vil ha mer informasjon, kan du se **Hvordan oppretter jeg oversettelser for produktrelatert informasjon?**.

## <a name="where-can-i-view-the-translated-information"></a>Hvor kan jeg vise den oversatte informasjonen?
Du kan vise oversettelser av produktrelatert informasjon i et eksternt kildedokument, for eksempel en faktura, som bruker et språk der oversettelsene som er tilgjengelige.

## <a name="how-do-i-create-translations-for-product-related-information"></a>Hvordan oppretter jeg oversettelser for produktrelatert informasjon?
Hvis du vil opprette transaksjoner for et produkt, gjør du følgende:
1.  Klikk på **Behandling av produktinformasjon** &gt; **Felles** &gt; **Frigitte produkter**.
2.  Velg et produkt, og i handlingsruten i **Språk**-gruppen klikker du på **Oversettelser**.
3.  På siden **Tekstoversettelse**, i **Språk**-feltet, velger du et språk. Hvis du vil legge til flere språk, utvider du **Språk**-feltet, og klikker deretter på **OK**.
4.  I gruppen **Oversatt tekst** skriver du inn oversettelser i feltene **Beskrivelse** og **Produktnavn**.

Hvis du vil opprette transaksjoner for produktattributter, gjør du følgende:
1.  Klikk på **Behandling av produktinformasjon** &gt; **Felles** &gt; **Frigitte produkter**.
2.  Under **Oppsett** klikker du **Attributter** og deretter **Attributter**.
3.  På **Attributter**-siden klikker du **Oversett**.
4.  På siden **Tekstoversettelse**, i **Språk**-feltet, velger du et språk. Hvis du vil legge til flere språk, utvider du **Språk**-feltet, og klikker deretter på **OK**.
5.  I gruppen **Oversatt tekst** skriver du inn oversettelser i feltene **Beskrivelse** **Egendefinert navn** og **Hjelpetekst**.

Hvis du vil opprette transaksjoner for produktdimensjonsverdier, gjør du følgende:
1.  Klikk på **Behandling av produktinformasjon** &gt; **Felles** &gt; **Frigitte produkter**.
2.  Velg et produkt, og klikk deretter **Produktdimensjoner**.
3.  Velg én av koblingene for produktdimensjonene: **Konfigurasjoner**, **Størrelser**, **Farger** eller **Stil**.
4.  Velg en dimensjonsverdi, og klikk deretter **Oversett**.
5.  På siden **Tekstoversettelse**, i **Språk**-feltet, velger du et språk. Hvis du vil legge til flere språk, utvider du **Språk**-feltet, og klikker deretter på **OK**.
6.  I gruppen **Oversatt tekst** skriver du inn oversettelser i feltene **Navn** og **Beskrivelse**.

## <a name="can-the-names-of-product-variants-be-translated"></a>Kan navnene på produktvarianter oversettes?
Produktvarianter er basert på dimensjonene til et frigitt produkt. Navn på produktvarianter er basert på en kombinasjon av dimensjonsverdier. Når dimensjonsverdiene som er knyttet til en produktvariant, oversettes, vises navnet på produktvarianten i den oversatte versjonen.  

**Eksempel**  

Produktet er en t-skjorte som kommer i ulike størrelser og farger, og variantnavnene som er basert på følgende detaljer:
-   Produktnummer: \#3
-   Dimensjoner: Størrelse og farge
-   Endre størrelse på dimensjonsverdier: Small, Medium, Large
-   Fargedimensjonsverdier: Rød, Grønn, Svart

Navnet på en produktvariant som er basert på dimensjonsverdiene Liten og Rød, er **\#3:Liten:Rød**.  

En kunde ønsker å kjøpe noen små, røde t-skjorter, og navnet på t-skjorten må vises på fransk på fakturaen. Du oversetter dimensjonsverdiene, liten og rød, til fransk, og navnet på produktvarianten er **\#3:Petit:Rouge**.
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Tips</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hvis du vil angi foretrukket språk for en kunde, gjør du følgende:
<ol><br/><li>Klikk på <strong>Salg og markedsføring</strong> &gt; <strong>Felles</strong> &gt; <strong>Kunder</strong> &gt; <strong>Alle</strong> <strong>kunder</strong>.</li>
<li>Dobbeltklikk en kundekonto for å åpne <strong>Kunder</strong>-siden. I fanen <strong>Generelt</strong>, i <strong>Språk</strong>-feltet, velger du <strong>språket</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>Hva skjer hvis en kunde har et foretrukket språk som det ikke finnes oversettelser for?
Hvis oversettelser ikke er tilgjengelige på kundens foretrukne språk, vises navnene og beskrivelsene på det globale språket for firmaet ditt.

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>Kan jeg administrere oversettelser for en rekke dimensjonsverdier samtidig?
Dimensjonsverdier er produktspesifikk, og du kan administrere oversettelser for dimensjonsverdier for hvert produkt. Hvis du imidlertid oppretter en dimensjonsverdigruppe og oppretter oversettelser for verdiene i verdigruppen, blir det enklere å administrere oversettelsene.   

**Eksempel**  

Firmaet ditt produserer t-skjorter i ulike stiler, og hver stil er tilgjengelig i størrelsene liten, middels og stor. Størrelsene samles i én dimensjonsverdigruppe. Når du legger til en ny t-skjortestil, kan du knytte den til dimensjonsverdigruppen som brukes for størrelser, slik at alle størrelsene er tilgjengelige for produktet. Du kan også legge til eller endre oversettelser for størrelsene i dimensjonsverdigruppen når som helst.  

En dimensjonsverdi som er tilknyttet et produkt gjennom en dimensjonsvariantgruppe, må vedlikeholdes fra produktvariantgruppen.   
Hvis du vil opprette en dimensjonsverdigruppe, gjør du følgende:
1.  Klikk på **Behandling av produktinformasjon** &gt; **Oppsett** &gt; **Variantgrupper**.
2.  Velg **Størrelse** **grupper**, **Fargegrupper** eller **Stilgrupper**.
3.  Klikk på **Ny**, og skriv deretter inn et navn på gruppen i **Størrelses** **gruppe**, **Fargegruppe** eller **Stilgruppe**-feltet. Klikk på **Størrelser**, **Farger** eller **Stiler** for å opprette linjer for gruppene.
4.  På siden **Størrelse** **gruppe** linjer, **Farge** **gruppe** **linjer** eller **Stilgruppelinjer** klikker du på **Ny**, og deretter oppretter du størrelsene, fargene og stilene for gruppene.

Hvis du vil administrere oversettelser for verdier i en dimensjonsverdigruppe, gjør du følgende:
1.  Følg den forrige fremgangsmåten for å opprette en dimensjonsverdigruppe for åpne siden **Størrelsesgruppelinjer**, **Fargegruppelinjer** eller **Stilgruppelinjer**.
2.  Klikk på **Tekstoversettelse**. På siden **Tekstoversettelse**, i gruppen **Oversatt tekst**, skriver du inn oversettelsene i feltene **Navn** og **Beskrivelse**.

## <a name="when-can-translations-of-product-related-information-be-managed"></a>Når kan oversettelser av produktrelatert informasjon håndteres?
Oversettelser av produktrelatert informasjon kan håndteres når som helst. Når oversettelser oppdateres for en dimensjonsverdi som er knyttet til et produkt, oppdateres produktinformasjonen, uavhengig av om produktet har transaksjoner.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]