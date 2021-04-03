---
title: Aktiver endringsstyring på eksisterende produkter
description: Dette emnet beskriver hvordan du kan aktivere endringsbehandling for eksisterende produkter. Den beskriver også tilfeller der evnen til å aktivere endringsbehandling er begrenset.
author: t-benebo
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-02
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 8b9f34f5980937da62610d9668a95816ba6054ef
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500868"
---
# <a name="enable-change-management-on-existing-products"></a>Aktiver endringsstyring på eksisterende produkter

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet beskriver hvordan du kan aktivere endringsbehandling for eksisterende produkter. Den beskriver også tilfeller der evnen til å aktivere endringsbehandling er begrenset.

Når du aktiverer endringsbehandling for et eksisterende produkt, kan du opprette versjoner av produktet og spore endringer som gjøres i det gjennom hele produktets levetid. Derfor kan du spore disse endringene ved hjelp av endringsordrer. Hvis du vil aktivere endringsbehandling, må du konvertere de relevante produktene til *byggeteknikkvarer* (også omtalt som tekniske produkter). Byggeteknikkprodukter er produkter som er versjonsstyrt og administrert gjennom endringsadministrasjon. Det formidles en veiviser som leder deg gjennom konverteringsprosessen.

## <a name="turn-on-the-feature-in-your-system"></a>Aktivere funksjonen i systemet

Hvis du vil bruke denne funksjonen, må du utføre følgende oppgaver:

1. Aktiver funksjonen for endringsbehandling i ingeniørvirksomhet og konfigurasjonsnøkkelen som beskrevet i [Oversikt over styring av teknisk endring](product-engineering-overview.md).
1. Aktiver funksjonen *Aktiver endringsbehandling for eksisterende produkter* i funksjonsstyring. Hvis du vil ha mer informasjon, kan du se [Oversikt over funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="restrictions-and-limitations"></a>Begrensninger og avmålinger

Ikke alle produkttyper kan konverteres til alle andre typer. Følgende begrensninger og avmålinger gjelder:

- Når du konverterer et produkt til et teknisk produkt, forblir det et *produkt*. Det blir ikke en *produktstandard*.
- Når du konverterer en hovedprodukt som har et bestemt sett dimensjoner, vedlikeholdes disse dimensjonene etter endringen. Hvis du for eksempel konverterer en hovedprodukt som har størrelsesdimensjonen, vil det beholde størrelsesdimensjonen.

Hvis du har et atskilt produkt, kan du derfor bare endre det til et teknisk produkt som ikke sporer produktdimensjonen i transaksjoner (det vil si versjonsdimensjonen som ikke brukes). Se de gjenstående delene i dette emnet hvis du vil ha mer informasjon om dette.

## <a name="prepare-for-conversion-by-creating-all-required-engineering-product-categories"></a>Klargjøre for konvertering ved å opprette alle nødvendige produktkategorier for ingeniørvirksomhet

En *kategori for teknisk produkt* må tilordnes hvert tekniske produkt. Du gjør denne tilordningen når du kjører veiviseren **Konverter til teknisk produkt**. Kategorier for teknisk produkt må finnes for alle relevante standardprodukter *før* du kan konvertere disse produktene.

Kategorien for teknisk produkt danner et grunnlag for oppretting av et teknisk produkt, og den fastsetter et sett med standardverdier og policyer. Kategorien for det tekniske produktet må samsvare produktet du tilordner den til. Produkttypen og dimensjonsgruppen må for eksempel samsvare med både produktet og dens kategori for teknisk produkt. Hvis du vil ha mer informasjon, kan du se [Tekniske versjoner og kategorier for teknisk produkt](engineering-versions-product-category.md).

> [!IMPORTANT]
> Veiviseren **Konverter til teknisk produkt** kan bare konvertere produkt til tekniske produkter der versjonen ikke er spores i transaksjoner. Derfor må alternativet **Spor versjon i transaksjoner** settes til *Nei* for kategorier for teknisk produkt som du oppretter for å konvertere eksisterende produkter.

Hvis du vil ha mer informasjon om hvordan du oppretter kategorier for teknisk produkt, kan du se [Tekniske versjoner og kategorier for teknisk produkt](engineering-versions-product-category.md).

## <a name="run-the-convert-to-engineering-product-wizard"></a>Kjøre veiviseren Konverter til teknisk produkt

Veiviseren **Konverter til teknisk produkt** hjelper deg med å konvertere én eller flere eksisterende produkter til tekniske produkter. Den konverterer produktene til tekniske produkter (versjonsprodukter) der versjonen ikke spores i transaksjoner (det vil si versjonsdimensjonen som ikke er brukt). Når konverteringen er fullført, kan du styre produktene ved hjelp av Styring av teknisk endring.

Konverteringen er permanent. Derfor kan du ikke tilbakeføre den senere. 

Hvert konverterte tekniske produkt vil fortsatt bli frigitt i de samme firmaene som det opprinnelige produktet ble frigitt i. Stykklisten (BOM) for tekniske produkter og ruter blir imidlertid frigitt automatisk til disse firmaene.

Følg denne fremgangsmåten for å kjøre veiviseren **Konverter til teknisk produkt** og konvertere et produkt til et teknisk produkt.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. I rutenettet merker du av for hvert produkt du vil konvertere.
1. I handlingsruten velger du **Konverter til teknisk produkt** i gruppen **Styring av teknisk endring** i fanen **Utvikle**.
1. Den første siden i veiviseren er siden **Velkommen**. Hvis du ikke allerede er kjent med konverteringsprosessen, må du være nøye når du leser informasjonen på denne siden. Når du er klar til å fortsette, velger du **Neste**.
1. Siden **Velg detaljer for produktene som skal konverteres**, viser hvert produkt du valgte før du åpnet veiviseren. Inspiser listen. Bruk knappen **Ny** og **Slett** på verktøylinjen til å legge til eller fjerne produkter etter behov.
1. Bruk følgende felt øverst i rutenettet til å tilordne standardverdier til hvert produkt som vises. (Du kan endre disse verdiene for enkeltprodukter etter at omregningen er fullført.) Standardverdier tilordnes ikke produkter der en relevant verdi allerede er tilordnet.

    - **Standard teknisk kategori** – Velg en første kategori for teknisk produkt som skal tilordnes til hvert oppførte produkt. Kategorien du velger, brukes bare for produkter som er kompatible med den.
    - **Standardversjon** – Angi den første produktversjonen som skal tilordnes hvert oppførte produkt. Hvert tekniske produkt har minst én teknisk versjon.
    - **Standard livssyklusstatus** – Velg den opprinnelige livssyklusstatusen for produktet som skal tilordnes hvert oppførte produkt.
    - **Gjeldende stykkliste vil være en del av teknisk produkt** – Merk av i denne avmerkingsboksen hvis gjeldende stykkliste for hvert oppførte produkt skal brukes som en stykkliste for det tekniske produktet.

    Se neste trinn for mer informasjon om produktinnstillinger.

1. Gå gjennom hvert produkt som er oppført i rutenettet, og vurder hvor godt standardverdiene du tilordnet, gjelder for det. For hver rad kan du se gjennom følgende informasjon og angi alle relevante felt:

    - **Produktnummer** – Produktnummeret.
    - **Produktnavn** – Produktnavnet.
    - **Teknisk kategori** – Velg kategorien for teknisk produkt som produktet skal tilhøre etter at det er konvertert. Det må allerede finnes en passende kategori for hvert produkt, slik det ble forklart i den forrige delen av dette emnet. Du må tilordne en kategori til hvert produkt.
    - **Versjon** – Angi den første produktversjonen som skal tilordnes til produktet etter at det er konvertert. Du kan for eksempel velge et nummer som passer i nummerserien som kategorien allerede bruker. Hver tekniske versjon lagrer de tekniske data som er relevante for denne versjonen. Hvis du vil ha mer informasjon, kan du se [Tekniske versjoner og kategorier for teknisk produkt](engineering-versions-product-category.md).
    - **Tilstand for produktlivssyklus** – Velg produktlivssyklusstatusen som produktet skal være i etter at det er konvertert. Med produktlivssyklustilstanden kan du bestemme hvilke transaksjoner som er tillatt for en angitt teknisk versjon. Hvis du vil ha mer informasjon, kan du se [Produktstatuser og transaksjoner](product-lifecycle-state-transactions.md).
    - **Har stykkliste** – En avmerket avmerkingsboks angir at produktet har en stykkliste. Innstillingen for denne avmerkingsboksen kan hjelpe deg med å velge verdi for avmerkingsboksen **Gjeldende stykkliste vil være en del av teknisk produkt**.
    - **Gjeldende stykkliste vil være en del av teknisk produkt** – Merk av i denne avmerkingsboksen hvis stykklisten for produktet skal brukes som en stykkliste for det tekniske produktet. Stykklisten administreres deretter ved hjelp av Styring av teknisk endring. Hvis produktet ikke har en stykkliste, eller hvis du foretrekker å opprette en stykkliste for det konverterte produktet manuelt senere, fjerner du merket i denne avmerkingsboksen.
    - **Har feil** – En avmerket avmerkingsboks angir at produktoppsettet har én eller flere feil. Det kan for eksempel hende at produkttypen eller dimensjonsgruppen ikke samsvarer i kategorien. Produkter som inneholder feil, blir hoppet over og ikke konvertert.

1. Når du er ferdig, velger du **Valider** på verktøylinjen for å validere produktoppsettet. For hver rad oppdateres avmerkingsboksen **Har feil** slik at den viser produktets status. Juster verdiene til oppsettet for hvert produkt er uten feil.
1. Når alle produktene er satt opp riktig, velger du **Neste** for å fortsette.
1. Siden **Bekreft valg** viser antallet produkter som ikke inneholder feil i oppsettet, og som derfor er klare for konvertering. Det viser også antall produkter som blir hoppet over på grunn av feil. Hvis du vil kjøre konverteringen som en satsvis jobb, setter du alternativet **Kjør satsvis** til *Ja*.
1. Velg **Fullfør** for å bruke innstillingene og begynne å konvertere produktene til tekniske produkter.

> [!NOTE]
> Hvis systemet er konfigurert til å godta produkter manuelt før de frigis, må du godta hvert konverterte produkt ved å bruke siden **Åpne produktutgivelser** i de aktuelle firmaene. Hvis du vil ha mer informasjon, kan du se [Les gjennom og godta produktet før du frigir det i det lokale firmaet](engineering-scenarios.md#accept).
