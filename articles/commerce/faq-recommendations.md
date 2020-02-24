---
title: Vanlige spørsmål om produktanbefalinger
description: Dette emnet inneholder informasjon om prosesser og verktøy som du kan bruke til å feilsøke problemer som er knyttet til produktanbefalinger eller de tilhørende resultatene.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7951f92ef68a7a782f2874d7b73d7e45eba0afba
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003033"
---
# <a name="product-recommendations-faq"></a>Vanlige spørsmål om produktanbefalinger


[!include [banner](includes/banner.md)]

Dette emnet inneholder informasjon om prosesser og verktøy som du kan bruke til å feilsøke problemer som er knyttet til [produktanbefalinger](product-recommendations.md) eller de tilhørende resultatene.

## <a name="best-practices"></a>Anbefalte fremgangsmåter
Det er svært viktig å bruke konseptet med produktstandarder og varianter. Fornuftig gruppering av varianter til en overordnet produktstandard hjelper listealgoritmene og tjenesten med å opprette bedre modeller. I tillegg kan tjenesten bare tjene én forekomst av et produkt i stedet for å legge inn alle nært relaterte varianter i en liste. Når alle nært relaterte varianter plasseres i en liste, kan det oppstå feil eller duplikate resultater.

## <a name="why-are-products-missing-from-my-recommendation-lists"></a>Hvorfor mangler produkter fra anbefalingslistene mine?

Hvis en vare mangler i en produktanbefalingsliste, kan det være et problem med produktkonfigurasjonen. Det kan for eksempel hende at det finnes feil produktstartdato eller -sluttdato, at en dimensjon ikke er riktig konfigurert, eller at produktet ikke er i det riktige kanalsortimentet osv.

Hvis en vare mangler i en anbefalingsliste som er basert på kunstig intelligens-maskinopplæring (AI-ML), kan det hende at varen ikke passer til kriteriene i anbefalingslisten, eller at det ikke er nok kjøpstransaksjoner til at anbefalingslisten kan vises dem.

Vi anbefaler at du kontrollerer disse trinnene:
1. **Kontroller at produktanbefalinger er aktivert i HK.** Hvis du vil ha mer informasjon om hvordan du aktiverer denne tjenesten, kan du se [Aktiver produktanbefalinger](enable-product-recommendations.md).
1. **Kontroller at det er angitt nøkkelproduktegenskaper.** Produktsortimenter må for eksempel være angitt til **Inkluder**.
1. **For nyassorterte produkter kan det ta opptil 3 timer før produktet begynner å bli vist i den nye listen.**
1. **Hvis et produkt fremdeles ikke vises i Stjerneskudd, Bestselgere, Folk liker også eller Ofte kjøpt sammen, kan det hende at produktet ikke har nok transaksjoner.** I dette tilfellet kan du enten vente på at flere transaksjoner skal forekomme, standard anbefalingslisteparameterne eller bruke manuell innblanding til å endre resultatene for anbefalingsproduktlisten. Hvis du vil ha mer informasjon om anbefalingsparametere, kan du se [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).
1. **Sørg for at produktet oppfyller anbefalingskriteriene for listen.** Hvis du vil ha mer informasjon om produktanbefalingsparametere, kan du se [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a>Hvordan kan jeg forhindre at det returneres dårlige anbefalinger?

Anbefalingslister krever et stort volum med transaksjoner for å gi resultater. Derfor er det viktig at brukerne oppgir alle historiske transaksjonsdata.

I tillegg har produkter uten transaksjoner eller med få transaksjoner vanligvis ikke **Folk liker også**- eller **Ofte kjøpt sammen**-resultater, og de vises ikke i anbefalingslistene **Stjerneskudd** eller **Bestselgere**. Denne situasjonen kan ofte oppstå for svært nye produkter eller for gamle produkter som ikke kjøpes så ofte. Populære nye elementer har ikke dette problemet.

Vi anbefaler at du følger disse trinnene:
1. **Sørg for at produktet oppfyller anbefalingskriteriene for denne listen.** Hvis du vil ha mer informasjon om produktanbefalingsparametere, kan du se Endre resultater for AI-ML-basert produktanbefaling.
1. **Hvis produktet er nytt, kan du vurdere å endre en anbefalingsliste til produktet har flere transaksjoner.** Hvis du vil ha mer informasjon om hvordan du endrer anbefalingslisteresultater, kan du se [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).


- **Sørg for at produktet oppfyller anbefalingskriteriene for denne listen.** Hvis du vil ha mer informasjon om produktanbefalingsparametere, kan du se [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).
- **Hvis produktet er nytt, kan du vurdere å endre en anbefalingsliste til produktet har flere transaksjoner**. Hvis du vil ha mer informasjon om hvordan du endrer anbefalingslisteresultater, kan du se [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a>Kan jeg fjerne et produkt, men likevel se det i butikken?

Du kan justere lister som genereres av algoritmer, hvis et forretningsbehov oppstår. Hvis et produkt fjernes fra en anbefalingsliste, vil produktet imidlertid forbli synlig i butikken. Hvis du vil ha mer informasjon om hvordan du endrer produktanbefalingsresultater, kan du se [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).

Hvis du må blokkere en vare fra å bli oppdaget i butikken, må du endre verdien for **Varesortimenter** til **Utelat**.

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a>Hvordan legger jeg til en liste på en e-handelsside?

Hvis du vil ha informasjon om hvordan du legger til produktanbefalingssider på e-handelsområdet, se [Legge til lister over produktanbefalinger på sider](add-reco-list-to-page.md).

## <a name="how-do-i-enable-recommendations-on-pos"></a>Hvordan aktiverer jeg anbefalinger for salgssted?

Når du har aktivert produktanbefalinger, må du legge til anbefalingspanelet til salgsstedets kontrollskjerm. Se [denne funksjonsdokumentasjonen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen) hvis du vil ha mer informasjon om hvordan du legger til anbefalinger-panelet i oppsettet for salgsstedsenheten.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over produktanbefalinger](product-recommendations.md)

[Aktiver produktanbefalinger](enable-product-recommendations.md)

[Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md)
