---
title: Produktklargjøring
description: I dette emnet finner du informasjon om hvordan du kan bruke klargjøringskontroller til å sikre at de nødvendige hoveddataene fullføres for et produkt før det brukes i transaksjoner.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 58b5a35800ab464f25868c6756b16f25d14d8d78
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/29/2020
ms.locfileid: "4434864"
---
# <a name="product-readiness"></a>Produktklargjøring

[!include [banner](../includes/banner.md)]

Du an bruke klargjøringskontroller til å sikre at alle de nødvendige hoveddataene er angitt for et produkt før det brukes i transaksjoner. Når det brukes klargjøringskontroller, er en bruker eller et team ansvarlig for å validere bestemte forhåndsdefinerte produktrelaterte data. Hvis det er en åpen klargjøringskontroll for et produkt, kan ikke produktet frigis eller brukes i transaksjoner.

Avmerkingsboksen **Aktiv** for et teknisk produkt, en variant eller en versjon er bare tilgjengelig etter at alle de påkrevde dataene er angitt og kontrollert, og etter at alle klargjøringskontrollene er behandlet. På dette tidspunktet kan produktet, versjonen eller varianten frigis til andre firmaer og brukes i transaksjoner. Du kan opprette klargjøringskontroller for nye produkter, nye varianter og nye tekniske versjoner.

## <a name="types-of-readiness-checks"></a>Typer klargjøringskontroller

Det finnes tre typer klargjøringskontroller:

- **Systemkontroll** – Systemet bekrefter om det finnes en gyldig post. Posten kan for eksempel være en aktiv stykkliste.
- **Manuell kontroll** – En bruker bekrefter om posten er gyldig. En klargjøringskontroll kan for eksempel kreve validering av standard ordreinnstillinger. I noen tilfeller, for eksempel når produktet fremdeles utvikles og derfor ikke vil bli plassert på lager, kreves det ingen standard ordreinnstillinger. Standard ordreinnstillinger kan imidlertid være nødvendige for et annet produkt av samme type, fordi produktet kan holdes på lager. Brukeren er ansvarlig for å vite hvordan de skal avgjøre om det kreves en klargjøringskontroll.
- **Sjekkliste** – Brukeren svarer på en rekke spørsmål fra en sjekkliste, og systemet fastsetter om svarene oppfyller forventningene. Sjekklisten kan ha et hvilket som helst emne. Den kan for eksempel brukes til å fastslå om markedsføringsmateriell eller produktdokumentasjon er fullført.

## <a name="how-readiness-checks-are-created-for-a-new-product-variant-or-version"></a>Slik opprettes klargjøringskontroller for et nytt produkt, en ny variant eller en versjon

Når du oppretter et nytt teknisk **produkt**, bestemmer systemet om det er konfigurert en policy for klargjøringskontroll for kategorien for teknisk produkt. (Policyer for klargjøringskontroll kan brukes på det frigitte produktnivået, det frigitte variantnivået og nivået for teknisk versjon.) Hvis en policy er konfigurert, skjer følgende hendelser:

- Klargjøringskontroller opprettes for produktet i henhold til gjeldende policy.
- Den tekniske versjonen er satt til inaktiv for å blokkere produktet fra å bli brukt. Alle versjonene for det bestemte produktet som er involvert, angis som inaktive.

Hvis det opprettes en ny **variant** for et produkt, kontrollerer systemet om det er definert klargjøringskontroller i kategorien for teknisk produkt. (Klargjøringskontroller kan brukes på det frigitte variantnivået og nivået for teknisk versjon.) Hvis en klargjøringskontroll er konfigurert, skjer følgende hendelser:

- Klargjøringskontroller er opprettet for produktet.
- Den tekniske versjonen er satt til inaktiv for å blokkere produktet fra å bli brukt.

Hvis det opprettes en ny teknisk **versjon** for et produkt, kontrollerer systemet om det er definert klargjøringskontroller i kategorien for teknisk produkt. (Klargjøringskontroller kan brukes på nivået for teknisk versjon.) Hvis en klargjøringskontroll er konfigurert, skjer følgende hendelser:

- Klargjøringskontroller er opprettet for produktet.
- Den tekniske versjonen er satt til inaktiv for å blokkere produktet fra å bli brukt.

## <a name="view-readiness-checks"></a>Vis klargjøringskontroller

### <a name="view-open-readiness-checks-for-a-product-or-product-version"></a>Vis åpne klargjøringskontroller for et produkt eller en produktversjon

Du finner de åpne klargjøringskontrollene for et produkt ved å åpne siden **Detaljer om frigitte produkter**. I handlingsruten, i **Produkt**-kategorien og **Klargjøringskontroller**-gruppen, velger du **Klargjøringskontroller**.

Hvis du vil finne de åpne klargjøringskontrollene for en produktversjon, åpner du **Tekniske versjoner**-siden for et frigitt produkt og velger en versjon. I handlingsruten, i **Produkt**-kategorien og **Sjekkliste**-gruppen, velger du **Klargjøringskontroller**.

### <a name="view-open-readiness-checks-that-are-assigned-to-you"></a>Vis åpne klargjøringskontroller som er tilordnet til deg

Hvis du vil vise de åpne klargjøringskontrollene som er tilordnet deg, følger du en av disse fremgangsmåtene.

- Gå til **Behandling av teknisk endring \> Felles \> Produktklargjøring \> Min åpne klargjøringskontroller**.
- Gå til **Behandling av produktinformasjon \> Arbeidsområder \> Produktklargjøring for stykkproduksjon**.

Oppsettet som angir hvem det er tilordnet klargjøringskontroller til, gjøres for kategorien for teknisk produkt. Klargjøringskontroller kan tilordnes til en person eller et team. Hvis det er tilordnet en klargjøringskontroll til et team, er det én person i teamet som må behandle klargjøringskontrollen. Hvis du vil ha mer informasjon, kan du se [Tekniske versjoner og kategorier for teknisk produkt](engineering-versions-product-category.md).

## <a name="process-open-readiness-checks"></a>Behandle åpne klargjøringskontroller

### <a name="process-system-and-manual-readiness-checks"></a>Behandle systemklargjøringskontroller og manuelle klargjøringskontroller

Når du har åpnet siden **Klargjøringskontroller**, kan du vise emnet for systemklargjøringskontroller og manuelle klargjøringskontroller ved å velge **Vis relatert informasjon** i handlingsruten. Deretter kan du fullføre eller validere dataene for klargjøringskontrollen. Åpne klargjøringskontroller har **statusverdien** *Ventende*. Denne statusen angir at klargjøringskontrollen fortsatt skal behandles. Hvis du vil behandle en klargjøringskontroll, gjør du ett av følgende.

- I handlingsruten velger du **Kontroller/fullfør** for å se gjennom og fullføre klargjøringskontrollen. Når du er ferdig, oppdateres feltet **Status** til *Bestått*.
- I handlingsruten velger **Hopp over** hvis du vil hoppe over en klargjøringskontroll som ikke er obligatorisk. Du kan for eksempel definere en klargjøringskontroll for prisberegninger. Du bestemmer imidlertid å hoppe over denne kontrollen mens produktet fremdeles befinner seg i utformingsfasen. I dette tilfellet oppdateres feltet **Status** til *Hoppet over*.

Avhengig av konfigurasjonen til klargjøringspolicyen, når feltet **Status** for en klargjøringskontroll oppdateres til *Bestått*, kan det være nødvendig med et ekstra trinn for å godkjenne klargjøringskontrollen. I så fall velger du **Godkjenning** for å fullføre klargjøringskontrollen. Dette godkjenningstrinnet er alltid obligatorisk når du hopper over klargjøringskontrollen.

Når alle de åpne klargjøringskontrollene for et nytt produkt, variant eller versjon er behandlet og godkjent som påkrevd, blir varen automatisk aktiv og dermed klar til bruk.

### <a name="process-checklist-readiness-checks"></a>Behandle klargjøringskontroller for sjekkliste

Hvis du vil åpne en sjekkliste, åpner du siden **Klargjøringskontroller**, og deretter velger du **Start sjekkliste** i handlingsruten. Når du har fullført sjekklisten, validerer systemet om klargjøringskontrollen er bestått, basert på innstillingene i spørreskjemaet. Hvis kontrollen er bestått, oppdateres feltet **Status** til *Bestått*. Hvis klargjøringskontrollen ikke er obligatorisk, kan du hoppe over den. I dette tilfellet oppdateres feltet **Status** til *Hoppet over*.

Avhengig av konfigurasjonen til klargjøringspolicyen, når feltet **Status** for en klargjøringskontroll oppdateres til *Bestått*, kan det være nødvendig med et ekstra trinn for å godkjenne klargjøringskontrollen. I så fall velger du **Godkjenning** for å fullføre klargjøringskontrollen. Dette godkjenningstrinnet er alltid obligatorisk når du hopper over klargjøringskontrollen.

Når alle de åpne klargjøringskontrollene for et nytt produkt, variant eller versjon er behandlet og godkjent som nødvendig, blir varen automatisk aktiv og dermed klar til bruk.

## <a name="create-and-manage-product-readiness-policies"></a>Opprett og behandle policyer for produktklargjøring

Bruk policyer for produktklargjøring til å administrere klargjøringskontrollene som gjelder for et produkt. Fordi en klargjøringspolicy er tilordnet den tekniske kategorien, vil alle kontrollene i klargjøringspolicyen gjelde for alle tekniske produkter som er basert på den tekniske kategorien. Hvis du vil ha mer informasjon, kan du se [Tekniske versjoner og kategorier for teknisk produkt](engineering-versions-product-category.md).

Hver klargjøringspolicy inneholder et sett med klargjøringskontroller. Når en klargjøringspolicy er tilordnet en kategori for teknisk produkt, vil alle produktene som er opprettet fra denne kategorien for teknisk produkt, ha klargjøringskontrollene som er angitt i klargjøringspolicyen.

Hvis du vil arbeide med produktklargjøringspolicyer, går du til **Behandling av teknisk endring \> Oppsett \> Produktklargjøringspolicyer**. Følg deretter ett av disse trinnene.

- Hvis du vil opprette en ny policy, velger du **Nytt** i handlingsruten, og deretter angir du feltene som beskrevet i følgende underavsnitt.
- Hvis du vil redigere en eksisterende policy, velger du det i listeruten, velger **Rediger** i handlingsruten og angir deretter feltene som beskrevet i følgende underavsnitt.
- Hvis du vil slette en eksisterende policy, velger du den i listeruten, velger **Rediger** i handlingsruten og kontrollerer deretter at alternativet **Aktiv** er satt til **Nei** i hurtigfanen *Generelt*. Velg deretter **Slett** i handlingsruten.

### <a name="header"></a>Hode

Angi følgende felter i toppteksten til en produktklargjøringspolicy.

| Felt | beskrivelse |
|---|---|
| Navn | Angi et navn for policyen. |
| beskrivelse | Angi en beskrivelse av policyen. |

### <a name="general-fasttab"></a>Hurtigfanen Generelt

Angi følgende felter på hurtigfanen **Generelt** til en produktklargjøringspolicy.

| Felt | beskrivelse |
|---|---|
| Produkttype | Velg om policyen gjelder for produkter av typen *Vare* eller *Tjeneste*. Du kan ikke endre denne innstillingen etter at du har lagret posten. |
| Aktive | Bruk dette alternativet til å opprettholde klargjøringspolicyene. Angi til *Ja* for alle klargjøringspolicyene du bruker. Angi til *Nei* for å merke en klargjøringspolicy som inaktiv når den ikke brukes. Legg merke til at du ikke kan deaktivere en klargjøringspolicy som er tilordnet til en kategori for teknisk produkt, og du kan bare slette inaktive frigivelsespolicyer. |

### <a name="readiness-control-fasttab"></a>Hurtigfanen Klargjøringskontroll

Legg til en rad i hurtigfanen **Klargjøringskontroll** for hver type klargjøringskontroll du vil ta med i policyen. Bruk knappene nedenfor på verktøylinjen for hurtigfanen til å legge til og fjerne rader etter behov:

- **Legg til kontroll** – Legg til en standard klargjøringskontroll i policyen. Når du velger denne knappen, vises dialogboksen **Legg til kontroll**. Der kan du velge fra en liste over tilgjengelige kontroller.
- **Legg til eksisterende spørreskjema** – Legg til en tom rad i rutenettet. Du kan deretter tilordne et eksisterende spørreskjema ved å angi feltene i følgende tabell.
- **Kopier** – Legg til en kopi av den valgte raden i rutenettet.
- **Slett** – Slett den valgte raden fra rutenettet.

For hver rad du legger til, angir du følgende felter:

| Felt | beskrivelse |
| --- | --- |
| Prosessområde | Velg området som kontrollen er relatert til. |
| Type | Velg om kontrollen er en systemkontroll, en manuell kontroll eller en sjekkliste (spørreskjema). |
| Navn | Hvis kontrollen er en sjekkliste, angir du et navn. Dette feltet angis automatisk for systemkontroller og manuelle kontroller. |
| beskrivelse | Hvis kontrollen er en sjekkliste, angir du en beskrivelse. For systemkontroller og manuelle kontroller blir dette feltet automatisk angitt, og beskrivelsen forklarer fokuset for kontrollen. |
| Bruk kontroller på | Velg om raden skal generere klargjøringskontroller som svar på et nytt frigitt produkt, en frigitt variant eller en frigitt versjon. |
| Utfør i | Velg om klargjøringskontroller som raden genererer, skal gjelder alle firmaer eller ett firma. |
| Bedrift | Hvis du setter **Utfør i**-feltet til *Ett firma*, velger du firmaet. |
| Eiertype | Velg om klargjøringskontroller som raden genererer, skal tilordnes til en person eller et team. |
| Eier | Velg personen eller teamet som klargjøringskontroller som raden genererer, tilordnes til. |
| Spørreskjema | Velg spørreskjemaet som skal brukes for sjekklisten. Sjekklisten er en lokal sjekkliste i firmaet der klargjøringskontrollen utføres. Systemet må kunne vurdere om sjekklisten er riktig besvart. Sjekklisten må derfor konfigureres slik at det utføres en evaluering basert på riktige svar. Hvis du vil ha mer informasjon om hvordan du oppretter spørreskjemaer, kan du se [Bruke spørreskjemaer](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/using-questionnaires) og det tilknyttede emner. |
| Automatisk godkjenning | Poster for klargjøringskontroll omfatter avmerkingsboksen **Godkjent** som angir godkjenningsstatusen. Merk av for **Automatisk godkjenning** for kontroller som skal settes til godkjent umiddelbart etter at den tilordnede brukeren har fullført dem. Fjern merket i denne avmerkingsboksen for å kreve eksplisitt godkjenning som et ekstra trinn. |
| Obligatorisk | Merk av i denne avmerkingsboksen for kontroller som må fullføres av den tilordnede brukeren. Du kan ikke hoppe over obligatoriske kontroller. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]