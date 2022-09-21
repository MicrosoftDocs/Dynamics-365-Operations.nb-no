---
title: Prisfunksjoner i salgssted
description: Denne artikkelen beskriver forskjellige pris- og rabattfunksjoner i Microsoft Dynamics 365 Commerce-salgsstedsprogrammet.
author: boycez
ms.date: 08/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-14
ms.openlocfilehash: 210798ac192ee251594ec8ff9d23dab31ec2043e
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473694"
---
# <a name="pricing-functions-in-pos"></a>Prisfunksjoner i salgssted

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver forskjellige pris- og rabattfunksjoner i Microsoft Dynamics 365 Commerce-salgsstedsprogrammet.

Salgsstedsprogrammet for Dynamics 365 Commerce inneholder rike funksjoner som gjør det mulig for førstelinjearbeidere å utføre Store Commerce-operasjoner. Følgende tabell viser funksjonene for pris og rabatt som for øyeblikket er tilgjengelige i programmet.

| Funksjon                       | Salgsstedsoperasjoner |
|--------------------------------|----------------|
| Vis priser                    | [Priskontroll](#price-check) |
| Vis rabatter                 | [Vis alle rabatter](#view-all-discounts)<br>[Vis tilgjengelige rabatter](#view-available-discounts) |
| Overstyr priser                | [Prisoverstyring](#price-override) |
| Bruk eller fjern rabatter      | [Linjerabattbeløp](#line-discount-amount)<br>[Linjerabatt i prosent](#line-discount-percent)<br>[Totalt rabattbeløp](#total-discount-amount)<br>[Total rabattprosent](#total-discount-percent)<br>[Fjern systemrabatter fra transaksjonen](#remove-system-discounts-from-transaction)<br>[Bruk systemrabatter på nytt](#reapply-system-discounts) |
| Bruk eller fjern kuponger        | [Legg til kupongkode](#add-coupon-code)<br>[Fjern kupongkode](#remove-coupon-code) |
| Beregn priser og rabatter | [Omberegn](#recalculate) |

Hvis du vil ha informasjon om hvordan de foregående operasjonene kan konfigureres i salgsstedsprogrammet, og om de støtter frakoblet modus, kan du se [Tilkoblede og frakoblede salgsstedsoperasjoner](pos-operations.md).

## <a name="price-check"></a>Priskontroll

Ved hjelp av **Priskontroll**-operasjonen kan salgsstedsbrukere slå opp forhåndskonfigurerte priser for et bestemt produkt.

## <a name="view-all-discounts"></a>Vis alle rabatter

Ved hjelp av **Vis alle rabatter**-operasjonen kan salgsstedsbrukere slå opp alle effektive kampanjer som for øyeblikket kjører i butikkanalen. Mer bestemt viser denne operasjonen alle rabatter som samsvarer med en av følgende betingelser:

- Prisgruppen for rabatten samsvarer med prisgruppen for butikken.
- Prisgruppen for rabatten tilordnes til et tilknytnings- eller fordelsprogram.
- Prisgruppen for rabatten tilordnes til en katalog som er knyttet til butikken.

Operasjonen **Vis alle rabatter** viser bare rabatter som ikke konkurrerer med en rabatt som allerede er tatt i bruk. Denne virkemåten bidrar til å sikre at hvis en salgsmedarbeider gir en kunde informasjon om rabatt, og kunden utfører den nødvendige handlingen (for eksempel kjøper kunden en vare til for å få 10 prosent rabatt), brukes rabatten på transaksjonen. Kupongbaserte rabatter vises bare hvis parameteren **Bruk uten en kupongkode** er aktivert.

I operasjonen **Vis alle rabatter** kan salgsstedsbrukere søke etter rabatter etter navn og beskrivelse, og de kan filtrere rabatter basert på om de krever en kupong.

## <a name="view-available-discounts"></a>Vis tilgjengelige rabatter

Ved hjelp av operasjonen **Vis tilgjengelige rabatter** kan salgsstedsbrukere vise alle rabatter som gjelder en valgt linje i en transaksjon eller hele transaksjonen. Rabattene som gjelder en valgt linje, omfatter rabatter som allerede er brukt, og rabatter som ennå ikke er brukt, men som kan brukes (samlerabatter som krever flere varer). Hvis en gjeldende rabatt er koblet til en kupong der **Bruk uten kupongkode**-parameter er aktivert, kan salgsstedsbrukeren også bruke **Bruk kupong**-funksjonen i denne operasjonen til å innløse kupongen direkte, uten å måtte angi eller skanne kupongkoder eller kupongstrekkoder.

## <a name="price-override"></a>Prisoverstyring

Ved hjelp av operasjonen **Prisoverstyring** kan salgsstedsbrukere overstyre salgsprisen til et produkt i en transaksjon. Denne operasjonen fungerer bare for produkter som er konfigurert til å tillate prisoverstyringer.

## <a name="line-discount-amount"></a>Linjerabattbeløp

Ved hjelp av operasjonen **Linjerabattbeløp** kan salgstedsbrukere angi et rabattbeløp for et linjeelement i en transaksjon. Denne operasjonen gjelder bare varer som det gis rabatt på, og den overholder verdien **Største linjerabattbeløp** som er angitt i salgsstedstillatelsesgruppen for brukeren.

## <a name="line-discount-percent"></a>Linjerabatt i prosent

Ved hjelp av operasjonen **Linjerabattprosent** kan salgstedsbrukere angi en rabattprosent for et linjeelement i en transaksjon. Denne operasjonen gjelder bare varer som det gis rabatt på, og den overholder verdien **Største linjerabattprosent** som er angitt i salgsstedstillatelsesgruppen for brukeren.

## <a name="total-discount-amount"></a>Totalt rabattbeløp

Ved hjelp av operasjonen **Totalt rabattbeløp** kan salgstedsbrukere angi et rabattbeløp for en transaksjon. Denne operasjonen gjelder bare varer som det gis rabatt på, og den overholder verdien **Største totale rabattbeløp** som er angitt i salgsstedstillatelsesgruppen for brukeren. Hvis rabattbeløpet som er angitt, overskrider det maksimale sluttrabattbeløpet, blokkeres operasjonen, og ingen overstyringsflyt for tillatelser utløses. For øyeblikket kan ikke et sluttrabattbeløp brukes på en handlekurv som har en blanding av salgsvarer og returvarer.

## <a name="total-discount-percent"></a>Total rabattprosent

Ved hjelp av operasjonen **Total rabattprosent** kan salgstedsbrukere angi en rabattprosent for en transaksjon. Denne operasjonen gjelder bare varer som det gis rabatt på, og den overholder verdien **Største totale rabattprosent** som er angitt i salgsstedstillatelsesgruppen for brukeren. Hvis rabattprosenten som er angitt, overskrider den maksimale sluttrabattprosenten, blokkeres operasjonen, og ingen overstyringsflyt for tillatelser utløses. For øyeblikket kan ikke en sluttrabattprosent brukes på en handlekurv som har en blanding av salgsvarer og returvarer.

## <a name="remove-system-discounts-from-transaction"></a>Fjern systemrabatter fra transaksjonen

Ved hjelp av operasjonen **Fjern systemrabatter fra transaksjon** kan salgsstedsbrukere fjerne alle brukte systemrabatter (inkludert kupongbaserte rabatter) fra en transaksjon. Når denne operasjonen er utført, begynner prissettingsmotoren å utelate systemrabatter fra rabattberegningsområdet. Operasjonen **Fjern systemrabatter fra transaksjon** fjerner ikke manuelle rabatter.

## <a name="reapply-system-discounts"></a>Bruk systemrabatter på nytt

Ved hjelp av operasjonen **Bruk systemrabatter på nytt** kan salgsstedsbrukere bruke systemberegnede rabatter på nytt for en transaksjon hvis rabattene ble fjernet ved hjelp av operasjonen **Fjern systemrabattene fra transaksjon**. Når denne operasjonen er utført, begynner prissettingsmotoren å ta med alle systemrabatter i rabattberegningsområdet.

## <a name="add-coupon-code"></a>Legg til kupongkode

Ved hjelp av operasjonen **Legg til kupongkode** kan salgstedsbrukere legge til en kupong i en transaksjon ved å angi en kupongkode. Salgsstedsbrukere kan også skanne en kupongstrekkode ved å angi den ved hjelp av det numeriske tastaturet på **Transaksjoner**-skjermen.

## <a name="remove-coupon-code"></a>Fjern kupongkode

Ved hjelp av operasjonen **Fjern kupongkode** kan salgsstedsbrukere velge og fjerne en eller flere kuponger som for øyeblikket brukes på en transaksjon.

## <a name="recalculate"></a>Omberegn

Ved hjelp av **Omberegn**-operasjonen kan salgsstedsbrukere utløse prissettingsberegninger etter behov. Denne operasjonen er nødvendig når prislås eller forsinket prisberegning er aktivert, og salgsstedsbrukeren ønsker å beregne priser og rabatter på nytt etter at handlekurv- eller ordreendringer er endret. **Omberegn**-operasjonen omberegner alltid hele ordren. Den kan ikke brukes til å omberegne valgte salgslinjer. Hvis du vil bruke manuelle rabatter på en låst salgslinje i salgssted, må salgsstedsbrukere først bruke operasjonen **Omberegn** for å låse opp alle salgslinjer.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
