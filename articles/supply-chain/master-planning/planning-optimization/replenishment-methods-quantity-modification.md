---
title: Etterfyllingsmetoder og antallsendring
description: Dette emnet inneholder informasjon om etterfyllingsmetoder i planleggingsoptimalisering. Det forklarer også hvordan flere bestillingsantall for et produkt påvirker resultatet.
author: crytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19853bdb3c469dbfea3a3a0165a9cb5f47e73122cc695de3535a58f6e65e7933
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759533"
---
# <a name="replenishment-methods-and-quantity-modification"></a>Etterfyllingsmetoder og antallsendring

[!include [banner](../../includes/banner.md)]

Dette emnet inneholder informasjon om etterfyllingsmetoder i planleggingsoptimalisering. Det forklarer også hvordan flere bestillingsantall for et produkt påvirker resultatet.

Etterfyllingsmetoder kalles også dekningsmetoder og metoder for justering av partistørrelse.

## <a name="coverage-codes"></a>Dekningskoder

Planleggingsoptimalisering kan konfigureres til å bruke forskjellige metoder for etterfylling. Etterfyllingsmetodene er teknikker som systemet bruker til å beregne behov for et produkt. Etterfyllingsmetoder defineres av dekningskoder som du kan definere på enten dekningsgruppen eller produktet.

Følgende dekningskoder kan brukes i planleggingsoptimalisering:

- **Periode** – Etterfyllingsmetoden kombinerer alt behovet for en periode i én ordre for produktet. Ordren vil bli planlagt for den første dagen i perioden, og antallet vil oppfylle nettobehovet i den etablerte perioden. Perioden begynner med det første behovet for produktet og dekker den definerte tidslengden. Neste periode starter med de neste behovene til produktet. *Periode*-dekningskoden brukes ofte for ikke-forutsigbare lagertrekk, sesongprodukter eller produkter med høy kostnad. Illustrasjonen nedenfor viser et eksempel.

    ![Eksempel på bruk av Periode-dekningskode.](./media/coverage-code-period.png "Eksempel på bruk av Periode-dekningskode")

- **Behov** – I etterfyllingsmetoden oppretter systemet et bestillingsforslag, en overføring eller en produksjonsordre per behov for produktet. Denne metoden brukes for kostbare produkter som har uregelmessig etterspørsel. Dekningskoden *Behov* brukes ofte for konfigurerbare produkter eller bestillingsscenarier. Illustrasjonen nedenfor viser et eksempel.

    ![Eksempel på bruk av Behov-dekningskode.](./media/coverage-code-requirement.png "Eksempel på bruk av Behov-dekningskode")

- **Min/maks** – Etterfyllingsmetoden er basert på lagernivået. Den definerer etterfyllingen av lager opptil et bestemt nivå når det forutsagte lagerbeholdningsnivået er under en bestemt terskel. Etterfyllingsantallet vil være differansen mellom maksimumsnivået og det forhåndsberegnede nivået. Dekningskoden *Min/maks* brukes ofte til forutsigbare lagertrekk, mest solgte produkter eller billigste produkter. Illustrasjonen nedenfor viser et eksempel.

    ![Eksempel på bruk av Min/maks-dekningskode.](./media/coverage-code-min-max.png "Eksempel på bruk av Min/maks-dekningskode")

- **Manuell** – I etterfyllingsmetoden foreslår ikke systemet kjøps-, overførings- eller produksjonsordrer for produktet. I stedet er det planleggeren for produktet som er ansvarlig for å opprette de nødvendige ordrene for etterfylling av produktet. Den *manuelle* dekningskoden brukes ofte for produkter som systemgenererte planlagte bestillinger ikke er ønsket for.

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a>Virkningen av ordreantallet fra standardordreinnstillinger

På siden **Standard ordreinnstillinger** for et frigitt produkt kan du angi følgende antallsinnstillinger i hurtigkategoriene **Bestilling**, **Lager** og **Salgsordre**. (Hurtigkategorien **Lager** brukes for både overføringsordrer og produksjonsordrer.)

- **Flere** – Planlagte bestillinger vil være et multiplum av dette antallet.

    Hvis for eksempel **Flere**-feltet er satt til *5*, kan en ordre være på antallet på 5, 10, 15, 20 og så videre.

- **Minimumsordre** – Planlagte bestillinger vil ikke være mindre enn den angitte verdien.

    Hvis for eksempel feltet **Minimumsordre** er satt til *10*, opprettes det en planlagt bestilling for et antall på 10, selv om bare fire kreves for å tilfredsstille behovet.

- **Maks. ordreantall** – Planlagte bestillinger vil ikke overstige den angitte verdien. Hvis behovet er mer enn **Maks. ordreantall**-verdien, blir det opprettet flere planlagte bestillinger for å dekke det.

    Hvis for eksempel feltet **Maks. bestillingsantall** er satt til *100*, og behovet er 450, vil det bli opprettet fire planlagte bestillinger for et antall på 100 og en planlagt bestilling på et antall på 50.

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a>Eksempler på etterfylling som bruker Min/maks. dekningskode

Hvis du ikke angir en verdi i **Flere**-feltet for et produkt på siden **Standard ordreinnstillinger**, og hvis du bruker etterfyllingsmetoden *Min/maks.* vil planleggingsoptimalisering etterfylle lageret opptil et bestemt nivå når det forutsagte lagerbeholdningsnivået er under en bestemt terskel.

Hvis du definerer et multiplumsantall for et produkt, endrer etterfyllingsmetoden *Min/maks.* virkemåten og vurderer **Flere**-verdien.

Med andre ord vil planleggingsoptimaliseringen etterfylle lageret opptil det definerte maksimumsnivået når det forutsagte lagernivået er mindre enn det definerte minimumsnivået. Etterfyllingsantallet må imidlertid være et multiplumsantall av **Flere**-verdien.

Hvis etterfyllingsantallet (differansen mellom det maksimale nivået og det forutsagte beholdningsnivået) ikke er et multiplumsantall av det definerte multiplumsantallet, bruker planleggingsoptimalisering den første mulige verdien som, sammen med forventet beholdningsnivå, vil være under maksimumsnivået. Hvis summen er mindre enn minimumsnivået, bruker planleggingsoptimalisering den første verdien som, sammen med forventet lagerbeholdning, vil være over maksimumsnivået.

Følgende delseksjoner gir noen eksempler som viser hvordan multiplumsordreantallet for et produkt påvirker resultatet av *Min/maks.*- etterfyllingsmetoden.

### <a name="example-1"></a>Eksempel 1

Et produkt har følgende konfigurasjon:

- **Dekningskode:** *Min/maks.*
- **Minimum:** *15*
- **Maksimum:** *22*
- **Flere:** *0*

Det er 10 stykker av lagerbeholdningen for produktet, og det er ingen annen etterspørsel eller forsyning.

Når hovedplanleggingen kjøres, opprettes det en planlagt bestilling på 12 stykker for å etterfylle lageret til maksimumsantallet.

### <a name="example-2"></a>Eksempel 2

Et produkt har følgende konfigurasjon:

- **Dekningskode:** *Min/maks.*
- **Minimum:** *15*
- **Maksimum:** *22*
- **Flere:** *5*

Det er 10 stykker av lagerbeholdningen for produktet, og det er ingen annen etterspørsel eller forsyning.

Når hovedplanleggingen kjøres, opprettes det en planlagt bestilling på 10 stykker (fordi 15 stykker etterfylling pluss 10 stykker av lagerbeholdningen vil overskride maksimumsantallet).

### <a name="example-3"></a>Eksempel 3

Et produkt har følgende konfigurasjon:

- **Dekningskode:** *Min/maks.*
- **Minimum:** *21*
- **Maksimum:** *24*
- **Flere:** *5*

Det er 10 stykker av lagerbeholdningen for produktet, og det er ingen annen etterspørsel eller forsyning.

Når hovedplanleggingen kjøres, opprettes den planlagte bestillingen på 15 stykker (fordi 10 stykker etterfylling pluss 10 stykker av lagerbeholdningen vil være mindre enn minimumsantallet).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
