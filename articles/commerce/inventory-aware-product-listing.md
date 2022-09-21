---
title: Beholdningsfølsom produktoversikt
description: Denne artikkelen beskriver hvordan organisasjoner kan konfigurere produktoversiktssider på e-handelsnettstedet for Microsoft Dynamics 365 Commerce slik at de er beholdningsfølsomme.
author: boycez
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-23
ms.openlocfilehash: 2a65dedf2da62fcd92169077d75a0f3b7832a86d
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473746"
---
# <a name="inventory-aware-product-listing"></a>Beholdningsfølsom produktoversikt

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan organisasjoner kan konfigurere produktoversiktssider på e-handelsnettstedet for Microsoft Dynamics 365 Commerce slik at de er beholdningsfølsomme. Produktoversiktssider omfatter kategorimålsider og søkeresultatsider.

Kunder forventer vanligvis at produktoppdaging er beholdningsfølsom over hele e-handelsnettstedet, slik at de kan avgjøre hva de skal gjøre hvis et produkt ikke er på lager. Kategorien [Commerce-modulbibliotek](starter-kit-overview.md) og søkeresultatmodulene kan konfigureres slik at du kan ta med lagerdata. På denne måten kan de gi følgende funksjonalitet:

- Vis etiketter på lagernivå sammen med produkter.
- Skjul produkter ikke på lager fra produktlisten.
- Flytt produkter som ikke er på lager, nederst på produktlistesider.
- Støtt lagerbasert produktfiltrering.

Hvis du vil aktivere disse funksjonene, må du først aktivere funksjonen **Forbedret produktoppdaging for e-handel slik at de er beholdningsfølsomme** i Commerce headquarters.

> [!NOTE]
> I Commerce versjon 10.0.29 og nyere er funksjonen **Forbedret produktoppdaging for e-handel slik at de er beholdningsfølsomme** aktivert som standard.

## <a name="set-up-product-attribute-for-inventory-availability"></a>Definer produktattributter for lagertilgjengelighet

Beholdningsfølsom produktoversikt bruker rammeverket for produktattributter. Det er en forutsetning at et dedikert produktattributt opprettes for å registrere lagertilgjengelighetsdata.

Følg denne fremgangsmåten for å definere et produktattributt for lagertilgjengelighet i Commerce headquarters.

1. Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Produkter og beholdning \> Fyll ut produktattributter med lagernivå**.
1. Skriv inn et egendefinert navn for det dedikerte produktattributtet som skal opprettes for å registrere lagerdata, i feltet **Produktattributt og type navn** i dialogboksen **Fyll ut produktattributter med lagernivå**.
1. I feltet **Lagertilgjengelighet basert på** velger du antallstypen som lagernivåberegningen skal baseres på: **Fysisk tilgjengelig** eller **Totalt tilgjengelig**.
1. Sett alternativet **Satsvis behandling** til **Ja**.
1. Velg **OK**.

> [!NOTE]
> For å oppnå en konsekvent beregning av lagernivå på tvers av sidene på e-handelsnettstedet må du sørge for at du velger samme antallstype både i feltet **Lagertilgjengelighet basert på** for jobben **Fyll ut produktattributter med lagernivå** og i innstillingen **Beholdningsnivå basert på** i Commerce-områdebygger.

Etter at det dedikerte produktattributtet er opprettet, er neste trinn å konfigurere attributtet for nettkanalen.

Følg denne fremgangsmåten for å konfigurere attributtet for nettkanalen i Commerce headquarters.

1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Kanalkategorier og produktattributter**.
1. Velg nettkanalen du vil aktivere den beholdningsfølsomme produktoversikten for.
1. Velg og åpne en tilknyttet attributtgruppe, og legg til det nye produktattributtet i den.
1. Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**, og kjør jobben **1150** (**Katalog**). Vi anbefaler at du planlegger denne jobben som en satsvise prosess som kjører med samme frekvens som jobben **Fyll ut produktattributter med lagernivå**.

> [!NOTE]
> I Commerce versjon 10.0.26 og tidligere må du også velge **Angi attributtmetadata** etter at du har lagt til produktattributtet for lagertilgjengelighet i en attributtgruppe, og deretter aktivere alternativene **Vis attributter i kanal**, **Kan hentes**, **Kan justeres** og **Kan spørres** for det nye produktattributtet.

## <a name="configure-the-display-behavior-for-out-of-stock-products-on-product-listing-pages"></a>Konfigurer visningsvirkemåten for produkter som ikke er på lager, på produktoversiktssider

Etter at alle de foregående konfigurasjonstrinnene er fullført, vil presiseringer på kategori- og søkeresultatsider ha et alternativ for lagerbasert filter. Det vises en etikett på lagernivå for hver produktflis som vises på siden.

Kategori- og søkeresultatsiden viser produkter på hovednivå, ikke på produktvariantnivå. Lagernivået som vises sammen med hvert produkt, er et aggregert lagernivå som fastsettes av lagernivået for alle variantene av et produkt. Lagernivået for en variant blir beregnet basert på lagerbeholdningen for denne varianten i standardlageret til nettkanalen i Commerce headquarters. Lagernivået for et hovedprodukt har to mulige verdier som representerer tilstandene «på lager» og «ikke på lager». Et hovedprodukt betraktes som ikke på lager når alle variantene er ikke på lager. Hvis ikke betraktes det som å være på lager. Etiketten for verdien hentes fra definisjonen for [lagernivå](inventory-buffers-levels.md). Hvis lagernivå ikke er definert, er standardetikettene (på engelsk) **Tilgjengelig** og **Utsolgt**.

Du kan konfigurere innstillingen **Lagerinnstillinger for produktlistesider** i Commerce-områdebygger for å styre hvordan kategori- og søkeresultatsiden viser produkter som ikke er på lager. For mer informasjon, se [Bruke beholdningsinnstillinger](inventory-settings.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
