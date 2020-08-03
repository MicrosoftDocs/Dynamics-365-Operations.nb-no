---
title: Varer med to bruksområder
description: Dette emnet forklarer hvordan du holder rede på produkter som er identifisert som varer med to bruksområder, lagrer sertifikatnumre for hvert relevante produkt og målland og skriver ut gyldige sertifikatnumre på relevante fakturaer, følgesedler og/eller salgsordrer.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0847dc1ce01a6e6f4f8b72db115445f75de4aac2
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596261"
---
# <a name="dual-use-goods"></a>Varer med to bruksområder

[!include [banner](../includes/banner.md)]

Bruk av varer med to bruksområder er vanligvis varer som har både sivile og militær bruksområder. Et kjemikalie kan for eksempel brukes som gjødsel eller et eksplosiv. Mange land har spesielle bestemmelser som gjelder for eksport, import og transport av varer med to bruksområder. Derfor er det viktig at firmaer som er involvert i den internasjonale handelen av varer med to bruksområder, holder oversikt over de ulike policyene og sertifikatene.

Funksjonen for to bruksområder hjelper firmaer med å holde rede på produkter som er identifisert som varer med to bruksområder, lagrer sertifikatnumre for hvert relevante produkt og målland og skriver ut gyldige sertifikatnumre på relevante fakturaer, følgesedler og/eller salgsordrer. Den bidrar til å sikre at når produktene sendes, inkluderer de alltid oppdaterte sertifiseringer.

Tenk deg følgende scenario:

1. Siden for **landoppsett for flerbruk** i systemet angir at forsendelser til Frankrike krever en sertifisering.
2. Siden **Detaljer om frigitt produkt** for produkt X-100 angir at varen har to bruksområder. Samlet angir kode, kategori, gruppe og regime eksportkontrollklassifiseringen som produktet tilhører.
3. Siden for **sertifikater for to bruksområder** inneholder et sertifikat for produkt X-100 når det sendes til Frankrike. Dette sertifikatet utløper 1. januar 2020.
4. 17. juni 2020 oppretter du en salgsordre for et kundefirma som er basert i Frankrike, og ordren inkluderer produkt X-100.
5. Når du lagrer salgsordren, finner systemet følgende informasjon:

    1. Tar ordren med varer som har to bruksområder?
    2. Hvis ordren inneholder varer med to bruksområder, må mållandet kreve sertifikater for to bruksområder?
    3. Hvis landet krever sertifikater for to bruksområder, finnes det et gyldig sertifikat for hver vare for to bruksområder for mållandet?

6. Ordren inkluderer produkt X-100, produktet sendes til Frankrike, og det finnes et fransk sertifikat for produktet. Sertifikatet er imidlertid utløpt. Du får derfor følgende advarsel: "Sertifikater for to bruksområder for ett eller flere flerbruksvarer i denne salgsordren er ikke gyldig. Vil du fortsette med bekreftelsen?"

Dette emnet forklarer hvordan du konfigurerer alle innstillingene som kreves for å konfigurere flerbruksvarer og støtte dette scenariet.

## <a name="define-dual-use-requirements-for-each-relevant-country"></a>Definere flerbrukskrav for hvert aktuelle land

Forskjellige land har ulike krav til flerbruksvarer. Du bruker siden for **landoppsett for flerbruk** for å holde oversikt over landene som krever og ikke krever et sertifikat. Informasjonen du angir her, kontrolleres når du oppretter salgsordrer, og du vil bli minnet på å gi de nødvendige sertifiseringene.

Følg denne fremgangsmåten for å angi flerbruksinformasjon for ulike land.

1. Gå til **Behandling av produktinformasjon \> Oppsett \> Produktoverensstemmelse \> Flerbruksprodukter \> Landsoppsett for flerbruk**.
2. Velg et eksisterende landsoppsett for å redigere det, eller velg **Ny** i handlingsruten for å opprette et nytt landsoppsett.
3. Angi følgende verdier for det valgte eller det nye landsoppsettet.

    | Felt | beskrivelse |
    |---|---|
    | Land/område | Velg landet du vil spore krav for. |
    | Sertifikat obligatorisk | Merk av i denne avmerkingsboksen for land som krever en sertifisering for flerbruksvarer. Fjern merket for land som ikke krever denne sertifiseringen. |

## <a name="create-dual-use-categories"></a>Opprette kategorier for flerbruk

Flerbruksvarer må ofte kategoriseres i henhold til ECCN-nummer (eksportkontrollklassifiseringsnummer). ECCN er en alfanumerisk kode som kategoriserer varer basert på faktorer som for eksempel artikkel og teknologi. Siden for **kategorier for flerbruk** hjelper deg med å opprette en liste over kategoriene du bruker, for rapporteringsformål.

Gjør følgende for å konfigurere kategorier for flerbruk.

1. Gå til **Behandling av produktinformasjon \> Oppsett \> Produktoverensstemmelse \> Flerbruksprodukter \> Kategorier for flerbruk**.
2. Velg en eksisterende kategori for å redigere den, eller velg **Ny** i handlingsruten for å opprette en ny kategori.
3. Angi følgende verdier for den valgte eller nye kategorien.

    | Felt | beskrivelse |
    |---|---|
    | Kode for flerbruk | Angi den fullstendige ECCN-koden (for eksempel *3A001*).|
    | Kategori for flerbruk | Angi CCL-kategoridelen (commerce control list) av ECCN-koden. For ECCN-koden *3A001* er denne verdien *3*. |
    | Gruppe for flerbruk | Angi produktgruppedelen av ECCN-koden. For ECCN-koden *3A001* er denne verdien *A*. |
    | Ordning for flerbruk | Angi koden for ordningen for varen. Denne koden identifiserer årsaken til at varen er klassifisert som flerbruksvare. For ECCN-koden *3A001* er denne verdien *001*. |

## <a name="apply-dual-use-categories-to-products"></a>Bruke flerbrukskategorier for produkter

Følg denne fremgangsmåten for å identifisere et produkt som en flerbruksvare og bruke en flerbrukskategori på den.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Velg eller opprett et produkt for å åpne siden **Detaljer om frigitt produkt**.
1. På hurtigfanen **Utenrikshandel** angir du alternativet for **Flerbruksprodukter** til **Ja** for å identifisere det gjeldende produktet som en flerbruksvare.
1. Sett feltet **Kode for flerbruk** til koden som gjelder for det gjeldende produktet. (Du definerte denne koden på siden for **Kategorier for flerbruk**.)

Dette oppsettet kontrolleres når du oppretter en salgsordre.

## <a name="set-up-dual-use-certificates"></a>Angi sertifikater for flerbruk

Du bruker siden for **Sertifikater for flerbruk** til å definere og behandle de nødvendige sertifikatene for flerbruk for hvert produkt og hvert land. Du kan spore detaljene for hvert sertifikat, for eksempel landet og datoene for gyldighet. Du kan også angi alternativer for å angi hvor denne informasjonen skal skrives ut. Informasjonen kan for eksempel skrives ut på fakturaen, følgeseddelen og/eller salgsordren. Dette oppsettet kontrolleres når du oppretter en salgsordre.

1. Gå til **Behandling av produktinformasjon \> Oppsett \> Produktoverensstemmelse \> Flerbruksprodukter \> Sertifikater for flerbruk**.
2. Velg et eksisterende sertifikat for å redigere det, eller velg **Ny** i handlingsruten for å opprette et nytt sertifikat.
3. Angi følgende verdier for det valgte eller nye sertifikatet.

    | Felt | beskrivelse |
    |---|---|
    | Varenummer | Velg varenummeret til flerbruksvaren som dette sertifikatet skal brukes på. |
    | Land/område | Mållandet eller -området der du må bruke dette sertifikatet. |
    | Sertifikatnummer | Nummeret som vises på sertifikatet som er utstedt til leverandøren eller kunden. |
    | Gyldighet | Velg den første datoen når det gjeldende sertifikatet er gyldig.|
    | Utløp | Velg den siste datoen når det gjeldende sertifikatet er gyldig. |
    | Skriv ut på faktura | Merk av i denne avmerkingsboksen for å skrive ut sertifikatnummeret på fakturaer som er adressert til det angitte landet i det angitte datoområdet. |
    | Skrive ut på følgeseddel | Merk av i denne avmerkingsboksen for å skrive ut sertifikatnummeret på følgesedler som er adressert til det angitte landet i det angitte datoområdet. |
    | Skriv ut på salgsordre | Merk av i denne avmerkingsboksen for å skrive ut sertifikatnummeret på salgsordrer som er adressert til det angitte landet i det angitte datoområdet. |
