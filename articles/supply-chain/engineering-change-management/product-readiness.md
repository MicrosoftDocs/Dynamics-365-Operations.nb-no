---
title: Produktklargjøring
description: I dette emnet finner du informasjon om hvordan du kan bruke klargjøringskontroller til å sikre at de nødvendige hoveddataene fullføres for et produkt før det brukes i transaksjoner.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 12707774c780a0f805deed532af27c3705ea1f55
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500604"
---
# <a name="product-readiness"></a>Produktklargjøring

[!include [banner](../includes/banner.md)]

Du an bruke klargjøringskontroller til å sikre at alle de nødvendige hoveddataene er angitt for et produkt før det brukes i transaksjoner. Når det brukes klargjøringskontroller, er en bruker eller et team ansvarlig for å validere bestemte forhåndsdefinerte produktrelaterte data.

Du kan merke av for **Aktiv** for et teknisk produkt, en variant eller en versjon etter at alle de påkrevde dataene er angitt og kontrollert, og etter at alle klargjøringskontrollene er behandlet. Hvis én eller flere sjekker ikke er behandlet for produktet, versjonen eller varianten, vil du få en ledetekst om at ikke alle kontrollene er fullført når du prøver å merke av for **Aktiv**.

Du kan opprette klargjøringskontroller for tekniske produkter, varianter og versjoner. Du kan også bruke beredskapskontroller på standardprodukter (ikke-tekniske produkter) (se også [Beredskapskontroller av standardprodukter](#standard-products)). 

Du kan bruke standardprodukter i transaksjoner selv om ikke alle beredskapskontroller er fullført. Hvis du har behov for å blokkere et produkt fra å bli brukt i transaksjoner, bruker du livssyklusstatusen. Du kan tilordne en livssyklusstatus som blokkerer et produkt fra å brukes i transaksjoner, og deretter tilordne en ny livssyklusstatus som tillater de nødvendige transaksjonene, når alle beredskapskontroller er fullført.

## <a name="types-of-readiness-checks"></a>Typer klargjøringskontroller

Det finnes tre typer klargjøringskontroller:

- **Systemkontroll** – Systemet bekrefter om det finnes en gyldig post. Posten kan for eksempel være en aktiv stykkliste.
- **Manuell kontroll** – En bruker bekrefter om posten er gyldig. En klargjøringskontroll kan for eksempel kreve validering av standard ordreinnstillinger. I noen tilfeller, for eksempel når produktet fremdeles utvikles og derfor ikke vil bli plassert på lager, kreves det ingen standard ordreinnstillinger. Standard ordreinnstillinger kan imidlertid være nødvendige for et annet produkt av samme type, fordi produktet kan holdes på lager. Brukeren er ansvarlig for å vite hvordan de skal avgjøre om det kreves en klargjøringskontroll.
- **Sjekkliste** – Brukeren svarer på en rekke spørsmål fra en sjekkliste, og systemet fastsetter om svarene oppfyller forventningene. Sjekklisten kan ha et hvilket som helst emne. Den kan for eksempel brukes til å fastslå om markedsføringsmateriell eller produktdokumentasjon er fullført.

<a name="checks-engineering"></a>

## <a name="how-readiness-checks-are-created-for-a-new-engineering-product-variant-or-version"></a>Slik opprettes klargjøringskontroller for et nytt teknisk produkt, en ny variant eller en versjon

Policyer for klargjøringskontroll kan brukes på nivået for frigitt produkt, på nivået for frigitt variant og på nivået for teknisk versjon.

Når du oppretter et nytt *teknisk produkt*, bestemmer systemet om en [policy for beredskapskontroll er gjeldende](#assign-policy). Hvis en beredskapskontrollpolicy er gjeldende, skjer følgende hendelser:

- Klargjøringskontroller opprettes for produktet i henhold til gjeldende policy.
- Den tekniske versjonen er satt til inaktiv for å blokkere produktet fra å bli brukt. Alle ingeniørversjoner for produktet settes til inaktiv.

Hvis det opprettes en ny *variant* for et produkt, kontrollerer systemet om en beredskapskontrollpolicy gjelder for det. (Klargjøringskontroller kan brukes på nivået for frigitte variant og på nivået for teknisk versjon.) Hvis en policy er gjeldende, skjer følgende hendelser:

- Klargjøringskontroller opprettes for produktet i henhold til gjeldende policy.
- Den tekniske versjonen og varianten settes til inaktiv for å blokkere produktet fra å bli brukt.

Hvis en ny teknisk *versjon* opprettes for et produkt, kontrollerer systemet om en beredskapskontrollpolicy gjelder for det. (Klargjøringskontroller kan brukes på nivået for frigitt versjon.) Hvis en policy er gjeldende, skjer følgende hendelser:

- Klargjøringskontroller opprettes for produktet i henhold til gjeldende policy.
- Den tekniske versjonen er satt til inaktiv for å blokkere produktet fra å bli brukt.

> [!NOTE]
> Du kan også sette opp beredskapskontrollpolicyer for standardprodukter (ikke-tekniske). Hvis du vil ha mer informasjon, kan du se [Klargjøringskontroller for standardprodukter](#standard-products) senere i dette emnet.

## <a name="view-readiness-checks"></a>Vis klargjøringskontroller

### <a name="view-open-readiness-checks-for-a-product-or-product-version"></a>Vis åpne klargjøringskontroller for et produkt eller en produktversjon

Du finner de åpne klargjøringskontrollene for et produkt ved å åpne siden **Detaljer om frigitte produkter**. I handlingsruten, i **Produkt**-fanen og **Klargjøringskontroller**-gruppen, velger du **Klargjøringskontroller**.

Hvis du vil finne de åpne klargjøringskontrollene for en produktversjon, åpner du **Tekniske versjoner**-siden for et frigitt produkt og velger en versjon. I handlingsruten, i **Produkt**-fanen og **Sjekkliste**-gruppen, velger du **Klargjøringskontroller**.

### <a name="view-open-readiness-checks-that-are-assigned-to-you"></a>Vis åpne klargjøringskontroller som er tilordnet til deg

Hvis du vil vise de åpne klargjøringskontrollene som er tilordnet deg, følger du en av disse fremgangsmåtene.

- Gå til **Behandling av teknisk endring \> Felles \> Produktklargjøring \> Min åpne klargjøringskontroller**.
- Gå til **Behandling av produktinformasjon \> Arbeidsområder \> Produktklargjøring for stykkproduksjon**.

Oppsettet som angir hvem det er tilordnet klargjøringskontroller til, gjøres for klargjøringspolicyen. Klargjøringskontroller kan tilordnes til en person eller et team. Hvis det er tilordnet en klargjøringskontroll til et team, er det én person i teamet som må behandle klargjøringskontrollen.

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

Bruk policyer for produktklargjøring til å administrere klargjøringskontrollene som gjelder for et produkt. Hver klargjøringspolicy inneholder et sett med klargjøringskontroller. Når en klargjøringspolicy er tilordnet en kategori for teknisk produkt eller et delt produkt, vil alle produktene som er relatert til kategorien eller det delte produktet, ha klargjøringskontrollene som er inkludert i klargjøringspolicyen.

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
| Aktive | Bruk dette alternativet til å opprettholde klargjøringspolicyene. Angi til *Ja* for alle klargjøringspolicyene du bruker. Angi til *Nei* for å merke en klargjøringspolicy som inaktiv når den ikke brukes. Legg merke til at du ikke kan deaktivere en klargjøringspolicy som er tilordnet til en kategori for teknisk produkt eller et delt produkt, og du kan bare slette inaktive frigivelsespolicyer. |

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
| Spørreskjema | Velg spørreskjemaet som skal brukes for sjekklisten. Sjekklisten er en lokal sjekkliste i firmaet der klargjøringskontrollen utføres. Systemet må kunne vurdere om sjekklisten er riktig besvart. Sjekklisten må derfor konfigureres slik at det utføres en evaluering basert på riktige svar. Hvis du vil ha mer informasjon om hvordan du oppretter spørreskjemaer, kan du se [Bruke spørreskjemaer](/dynamicsax-2012/appuser-itpro/using-questionnaires) og det tilknyttede emner. |
| Automatisk godkjenning | Poster for klargjøringskontroll omfatter avmerkingsboksen **Godkjent** som angir godkjenningsstatusen. Merk av for **Automatisk godkjenning** for kontroller som skal settes til godkjent umiddelbart etter at den tilordnede brukeren har fullført dem. Fjern merket i denne avmerkingsboksen for å kreve eksplisitt godkjenning som et ekstra trinn. |
| Obligatorisk | Merk av i denne avmerkingsboksen for kontroller som må fullføres av den tilordnede brukeren. Du kan ikke hoppe over obligatoriske kontroller. |

<a name="assign-policy"></a>

## <a name="assign-readiness-policies-to-standard-and-engineering-products"></a>Tilordne beredskapspolicyer til standardprodukter og tekniske produkter

Når du oppretter et nytt produkt basert på en teknisk kategori, oppretter du både et *frigitt produkt* og et relatert *delt produkt*. Hvordan beredskapspolicyer løses for et frigitt produkt, avhenger av om du har aktivert funksjonen *Produktklargjøringskontroller*. (Hvis du vil ha mer informasjon, kan du se [Klargjøringskontroller for standardprodukter](#standard-products) senere i dette emnet.)

- Når funksjonen for *Produktklargjøringskontroller* er slått *av* på systemet, angis beredskapspolicyen og vises bare på poster for [teknisk kategori](engineering-versions-product-category.md). Hvis du vil vite hvilke policyer som gjelder for et frigitt produkt, kontrollerer systemet feltet **Policy for produktklargjøring** for den relaterte tekniske kategorien. Du kan endre beredskapspolicyen for et eksisterende produkt ved å redigere den tilknyttede tekniske kategorien (ikke det delte produktet).
- Når funksjonen *Produktklargjøringskontroller* er *på*, legger den til et felt **Policy for produktklargjøring** på **Produkt**-siden (der delte produkter er definert) og til **Frigitt produkt**-siden (der verdien er skrivebeskyttet og hentes fra det relaterte delte produktet). Systemet finner beredskapspolicyen for et frigitt produkt ved å kontrollere det relaterte delte produktet. Når du bruker en teknisk kategori til å opprette et nytt teknisk produkt, oppretter systemet både et delt produkt og et frigitt produkt og kopierer en eventuell innstilling for **Policy for produktklargjøring** for den tekniske kategorien til det nye delte produktet. Du kan deretter endre beredskapspolicyen for et eksisterende produkt ved å redigere det relaterte delte produktet (ikke den frigitte tekniske kategorien).

Hvis du vil tilordne en klargjøringspolicy til et delt produkt, gjør du følgende.

1. Gå til **Produktinformasjon \> Produkter \> Produkter**.
1. Åpne eller opprett produktet du vil tilordne en beredskapspolicy til.
1. I hurtigkategorien **Generelt** angir feltet **Policy for produktklargjøring** til navnet på policyen som skal gjelde for produktet.

Hvis du vil tilordne en klargjøringspolicy til en teknisk kategori, følger du disse trinnene.

1. Gå til **Styring av teknisk endring \> Oppsett \> Detaljer om kategori for teknisk produkt**.
1. Åpne eller opprett den tekniske kategorien du vil tilordne en beredskapspolicy til.
1. I hurtigkategorien **Generelt** angir feltet **Policy for produktklargjøring** til navnet på policyen som skal gjelde for den tekniske kategorien.

<a name="standard-products"></a>

## <a name="readiness-checks-on-standard-products"></a>Beredskapskontroller av standardprodukter

Du kan aktivere produktberedskapskontroller for standardprodukter (ikke-tekniske produkter) ved å aktivere funksjonen for *Produktklargjøringskontroller* i Funksjonsbehandling. Denne funksjonen gjør noen små endringer i beredskapskontrollsystemet, slik at det støtter standardprodukter.

### <a name="enable-readiness-checks-on-standard-products"></a>Aktivere beredskapskontroller av standardprodukter

Følg denne fremgangsmåten for å aktivere systemet for beredskapskontroller av standardprodukter.

- Aktiver Styring av teknisk endring i systemet som beskrevet i [Oversikt over styring av teknisk endring](product-engineering-overview.md).
- Bruk [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktivere funksjonen kalt *Produktberedskapskontroller*.

<!-- KFM: This section requires confirmation before publishing

### How readiness checks are created for standard products

When you create a new non-engineering *released product*, the system determines whether a readiness check policy has been set up for the related shared product. If a policy has been set up, the following events occur:

- Readiness checks are created for the released product, according to the applicable policy.
- The released product is blocked from being used until all checks are marked as completed.

If a new *variant* is created for a product, the system checks whether readiness checks have been set up on the related shared product. If a readiness check has been set up, the following events occur:

- Readiness checks are created for the released product, according to the applicable policy.
- The released product is blocked from being used until all checks are marked as completed.

For engineering products, readiness checks are created in the same way that they are created when the *Product readiness checks* feature is turned off. For more information, see the [How readiness checks are created for a new engineering product, variant, or version](#checks-engineering) section earlier in this topic.

-->

### <a name="create-readiness-policies-for-standard-products"></a>Opprette beredskapspolicyer for standardprodukter

Du oppretter beredskapspolicyer for standardprodukter på samme som for tekniske produkter. Se informasjonen tidligere i dette emnet.

### <a name="assign-readiness-policies-to-standard-products"></a>Tilordne beredskapspolicyer til standardprodukter

Hvis du vil tilordne en beredskapspolicy til et standardprodukt, åpner du det relaterte delte produktet og setter feltet **Policy for produktklargjøring** til navnet på policyen som skal gjelde. Hvis du vil ha mer informasjon, kan du se delen [Tilordne beredskapspolicyer til standardprodukter og tekniske produkter](#assign-policy) tidligere i dette emnet.

### <a name="view-and-process-readiness-checks-on-standard-products"></a>Vise og behandle beredskapskontroller av standardprodukter

Når denne funksjonen er aktivert, viser og behandler du beredskapskontroller for standardprodukter på samme vis som du gjør for tekniske produkter. Se informasjonen tidligere i dette emnet.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
