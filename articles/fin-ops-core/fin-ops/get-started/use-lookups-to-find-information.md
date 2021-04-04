---
title: Finne informasjon ved hjelp av oppslag
description: Mange felt har oppslag som kan hjelpe deg å finne riktig og ønsket verdi. Flere forbedringer er lagt til oppslag som gjør disse kontrollene mer brukervennlige og gjør brukere mer produktive. I dette emnet du vil lære mer om disse nye oppslagsfunksjonene og får flere nyttige tips for bruke oppslag i systemet på best mulig måte.
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ae5f31c2cc46bf395acfbd053168e88aa69ebdc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566300"
---
# <a name="find-information-by-using-lookups"></a>Finne informasjon ved hjelp av oppslag

[!include [banner](../includes/banner.md)]

Mange felt har oppslag som kan hjelpe deg å finne riktig og ønsket verdi. Flere forbedringer er lagt til oppslag som gjør disse kontrollene mer brukervennlige og gjør brukere mer produktive. I dette emnet du vil lære mer om disse nye oppslagsfunksjonene og får flere nyttige tips for bruke oppslag i systemet på best mulig måte.

## <a name="responsive-lookups"></a>Responsive oppslag

Ved samhandling med en oppslagskontroll i tidligere versjoner, måtte brukere utføre en eksplisitt handling for å åpne rullegardinmenyen. Dette var for eksempel å skrive inn en stjerne (\*) i kontrollen for å filtrere oppslaget basert på gjeldende verdi i kontrollen, klikke på rullegardinlisten eller hurtigtasten bruke **Alt**+**pil ned**. Oppslagskontrollene er endret på følgende måter for å fungere bedre med gjeldende webfremgangsmåter:

- Rullegardinmenyer for oppslag åpnes nå automatisk etter en liten pause i skrivingen, med innholdet i rullegardinmenyen filtrert basert på verdien i oppslagskontrollen.

    Legg merke til at den gamle virkemåten for automatisk åpning av rullegardinlisten etter å ha skrevet inn en stjerne (\*) er fjernet.

- Når rullegardinmenyen for oppslag er åpnet, skjer følgende:

    - Markøren forblir i oppslagskontrollen (i stedet for å flytte fokus til rullegardinmenyen), slik at du kan fortsette å gjøre endringer i verdien i kontrollen. Brukeren kan imidlertid fortsatt bruke **pil opp** og **pil ned** til å endre rader i på rullegardinmenyen, og Skriv inn for å merke gjeldende rad på rullegardinmenyen.
    - Innholdet på rullegardinmenyen justeres etter at verdien i oppslagskontrollen er endret.

Anta for eksempel at et oppslagsfelt kalles **By**.

Når fokus er i **By**-feltet, kan du begynne å søke etter byen som du vil bruke, ved å skrive inn noen få bokstaver, for eksempel "col." Når at har sluttet å skrive, åpnes oppslaget automatisk, filtrert etter byene som begynner med "col".

[![Eksempel på forutseende oppslag](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)

Markøren er på dette tidspunktet fremdeles i oppslagsfeltet. Hvis du fortsetter å skrive slik at verdien er "colum", justeres innholdet oppslag automatisk for å gjenspeile den siste verdien i kontrollen.

![Eksempel på oppdatering av oppslagsfilter](./media/updatefilterlookupexample.png)

Selv om fokus fremdeles er i oppslagskontrollen, kan du også bruke **pil opp** eller **pil ned** til å merke raden som du vil velge. Hvis du trykker på **Angi**, velges den merkede raden fra oppslaget, og verdien i kontrollen oppdateres.

![Endre valg i oppslag](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a>Skrive inn mer enn ID-er

Ved angivelse av data, er det naturlig for brukere å prøve å identifisere en enhet, for eksempel en kunde eller leverandør, etter navnet i stedet for en identifikator som representerer enheten. Mange (men ikke alle) oppslag tillater nå kontekstbasert dataregistrering. Denne kraftige funksjonen lar brukere skrive inn ID-en eller det tilsvarende navnet, i oppslagskontrollen.

La oss for eksempel se på **Kundekonto**-feltet ved oppretting av en salgsordre. Dette feltet viser **konto-ID** for kunden, men en bruker foretrekker vanligvis å angi et **kontonavn** i stedet for en **konto-ID** for dette feltet ved oppretting av en salgsordre, for eksempel "Forest Wholesales" i stedet for "US-003".

Hvis brukeren begynte å skrive inn en **konto-ID** i oppslagskontrolle, åpnes rullegardinmenyen automatisk som beskrevet i den forrige delen, og brukeren ser oppslaget som vist nedenfor.

[![Kontekstavhengig oppslag når det angis en kundekonto-ID](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)

Brukeren kan imidlertid nå også angi begynnelsen på et **kontonavnet**. Hvis dette blir funnet, vil brukeren se oppslaget nedenfor. Legg merke til hvordan **Navn**-kolonnen flyttes slik at det er den første kolonnen i oppslaget, og hvordan oppslaget sorteres og filtreres basert på **Navn**-kolonnen.

[![Kontekstavhengig oppslag når det angis et kundenavn](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a>Bruke kolonneoverskriftene i rutenett for mer avansert filtrering og sortering

Oppslagsforbedringene som er beskrevet i de forrige to delene, forbedre betydelig brukeres mulighet til å navigere i oppslagsradene basert på et "begynner med"-søk for **ID**- eller **Navn**-feltet i oppslaget. Det finnes imidlertid situasjoner der mer avansert filtrering (eller sortering) er nødvendig for å finne den riktige raden. I slike tilfeller må brukeren bruke filtrerings- og sorteringsalternativene i kolonneoverskriftene i rutenettet i oppslaget. Anta for eksempel at en ansatt angir en salgsordrelinje som må riktig "kabel" som produkt. Det er ikke særlig nyttig å skrive inn "kabel" i **Varenummer**-kontrollen, fordi det ikke finnes produktnavn som begynner med "kabel".

![Oppslag med tomt element](./media/emptyitemlookup.png)

Brukeren må i stedet fjerne verdien i oppslagskontrollen, åpne rullegardinmenyen for oppslaget og filtrere rullegardinmenyen ved hjelp av kolonneoverskriften i rutenett, som vist nedenfor. En bruker som bruker mus (eller berøring) kan ganske enkelt klikk på (eller berøre) en kolonneoverskrift for å få tilgang til filtrerings- og sorteringsalternativene for den aktuelle kolonnen. En bruker som bruker tastatur trenger bare å trykke på **Alt**+**Pil** **ned** en gang til for å flytte fokus til rullegardinmenyen, og deretter kan brukeren bruker Tab-tasten for å gå til riktig kolonne og trykke på **Ctrl**+**G** for å åpne rullegardinmenyen for kolonneoverskriften i rutenettet.

[![Oppslag for rutenettfilterelement](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)

Når filteret er brukt (se bildet nedenfor), kan brukeren søke etter og merke raden som vanlig.

![Elementoppslag med filterredigering](./media/filtereditemlookup.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]