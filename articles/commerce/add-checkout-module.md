---
title: Kassemodul
description: Dette emnet beskriver hvordan du legger til en kassemodul på en side og angir de nødvendige egenskapene.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4b810441fd25d41ee0893b119b4f7d91e7435d21
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697089"
---
# <a name="checkout-module"></a>Kassemodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du legger til en kassemodul på en side og angir de nødvendige egenskapene.

## <a name="overview"></a>Oversikt

En kassemodul er en spesialcontainer som er vert for alle modulene som kreves for å opprette en ordre. En kassemodul kan inneholde moduler som håndterer leveringsadressen, leveringsmetoder, faktureringsinformasjon, ordresammendrag og annen informasjon som er knyttet til en kundeordre. Den viser en trinnvis flyt som en kunde bruker til å angi all relevant informasjon for å foreta et kjøp.

En kassemodul gjengir data basert på handlekurv-IDen. Denne handlekurv-IDen lagres som en informasjonskapsel i leseren. En handlekurv-ID kreves for å gjengi informasjon i kassemodulen, for eksempel varene i ordren, totalbeløpet og rabattene.

## <a name="checkout-module-properties"></a>Egenskaper i kassemodulen

En kassemodul inneholder et sett med moduler. Med egenskapen bredde kan du angi om varene i kassemodulen skal tilpasses til bredden eller fylle skjermen.

En kassemodul har flere spor, for eksempel **Kasseinformasjon**-sporet, et **Ordresammendrag**-spor og et **Bestill**-spor. Hvert spor støtter et sett med moduler som vil vises i et bestemt oppsett på siden. **Kasseinformasjon**-sporet inneholder for eksempel alle modulene som kreves for å utløse en utsjekking, for eksempel moduler for leveringsadresse og betalingsmåte. **Ordresammendrag**-sporet viser et ordresammendrag og støtter handlingen med å bestille. **Bestill**-sporet støtter også handlingen med å bestille. Bestill-moduler kan defineres i to spor for å optimalisere prosessen med å plassere bestillinger fra ulike plattformer.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moduler som kan brukes i kassemodulen

- **Leveringsadresse** – Med denne modulen kan en kunde legge til eller velge leveringsadressen for en ordre. Hvis kunden er logget på, vises alle adresser som tidligere ble lagret for den kunden. Kunden kan deretter velge blant disse adressene. Kunden kan også legge til en ny adresse. Leveringsadressen brukes for alle varene i ordren som krever levering. Den kan ikke tilpasses for individuelle linjeelementer. Leveringsadresseformater defineres for hvert land eller område, og land/område-spesifikke regler håndheves av denne modulen. Selv om denne modulen ikke gir adressevalidering, kan adressevalidering implementeres ved hjelp av tilpassing. Hvis ordren bare omfatter varer som skal plukkes i butikken, blir denne modulen automatisk skjult.
- **Leveringsalternativer** – I denne modulen kan en kunde velge et leveringsalternativ for en ordre. Leveringsalternativene er basert på leveringsadressen. Hvis leveringsadressen endres, må leveringsalternativene hentes på nytt. Hvis ordren bare omfatter varer som skal plukkes i butikken, blir denne modulen automatisk skjult.
- **Container for betalingsdel** – Denne modulen er en container som du kan sette flere moduler i for å opprette en del innenfor betalingsflyten. Du kan for eksempel plassere alle betalingsrelaterte moduler i denne containeren for å vise dem som én inndeling. Denne modulen har bare innvirkning på oppsettet for flyten.
- **Gavekort** – Ved hjelp av denne modulen kan en kunde betale for en ordre ved å bruke et gavekort. Den støtter bare Microsoft Dynamics 365 Commerce-gavekort. Ett eller flere gavekort kan brukes i en ordre. Hvis saldoen på gavekortet ikke dekker beløpet i handlekurven, kan gavekortet kombineres med en annen betalingsmåte. Gavekort kan bare løses inn hvis kunden er logget på.
- **Fordelspoeng** – Denne modulen gjør det mulig for en kunde å betale for en ordre ved å bruke fordelspoeng. Den gir et sammendrag av tilgjengelige poeng og utløpende poeng og lar kunden velge antall poeng du vil løse inn. Hvis kunden ikke er logget på eller ikke er fordelsmedlem, eller hvis totalbeløpet i handlekurven er 0 (null), blir denne modulen automatisk skjult.
- **Kredittkort** – Ved hjelp av denne modulen kan en kunde betale for en ordre ved å bruke et kredittkort. Hvis totalbeløpet i handlekurven dekkes av fordelspoeng eller et gavekort, eller hvis det er 0 (null), blir denne modulen automatisk skjult. Kredittkortintegrasjon leveres av betalingskoblingen Adyen. Hvis du vil ha mer informasjon om hvordan du bruker denne koblingen, se [Adyen-betalingskobling](https://).
- **Fakturaadresse** – Ved hjelp av denne modulen kan en kunde angi betalingsinformasjon. Denne informasjonen behandles sammen med kredittkortinformasjonen, etter Adyen. Denne modulen inneholder et alternativ som brukes til å la kundene bruke faktureringsadressen som leveringsadresse.
- **Kontaktinformasjon** – Ved hjelp av denne modulen kan en kunde legge til eller endre kontaktinformasjonen (e-postadresse) for en ordre.
- **Bestill** – Ved hjelp av denne modulen kan en kunde legge inn en ordre.
- **Innholdsrik blokk** – Denne modulen inneholder alle meldinger som drives av innholdsstyringssystemet (CMS). Den kan for eksempel inneholde en melding som sier "For problemer med bestillingen, ta kontakt med 1-800-FABRIKAM". 
- **Ordresammendrag** – Denne modulen viser kostnadsoppdelingen for en ordre.
- **Ordrelinjevarer** – Denne modulen viser et sammendrag av varene som vil bli inkludert i en ordre.

## <a name="retail-server-interaction"></a>Interaksjon med detaljhandelsserver

Det meste av informasjonen i kassen, for eksempel forsendelsesadressen og forsendelsesmetoden, lagres i handlekurven og behandles som en del av ordren. Det eneste unntaket er kredittkortinformasjonen. Denne informasjonen behandles direkte ved hjelp av betalingskoblingen Adyen. Betalingen godkjennes, men belastes ikke.

## <a name="add-a-checkout-module-to-a-new-page-and-set-the-required-properties"></a>Legge til en kassemodul på en ny side og angi de nødvendige egenskapene

Hvis du vil legge til en kassemodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Gå til **Fragment \> Nytt fragment**, og gi det nye fragmentet navnet **Kassefragment**.
1. Legg til en kassemodul i fragmentet.
1. Legg til en overskrift i kassemodulen.
1. I **Kasseinformasjon**-sporet legger du til moduler for leveringsadresse, leveringsalternativer, kassedelcontainer og kontaktinformasjon. Nå skal det være fire deler i **Kasseinformasjon**-sporet.
1. I kassedelcontainermodulen legger du til moduler for gavekort, fordelspoeng og kredittkort. På denne måten sørger du for at alle betalingsmåtene vises sammen i en del.
1. I sporet **Ordresammendrag** legger du til moduler for ordresammendrag, bestilling og innholdsrik blokk.
1. I modulen innholdsrikt blokk legger du til følgende tekst: **Hvis du vil ha spørsmål om bestillingen, kan du kontakte 1-800-FABRIKAM**.
1. Legg til en bestillingsmodul i sporet **Bestill**.
1. Velg **Lagre**. Noen moduler gjengis kanskje ikke i forhåndsvisningen, fordi de ikke har en handlekurvkontekst.
1. Sjekk inn fragmentet, og publiser det.
1. Opprett en mal som bruker det nye kassefragmentet.
1. Opprett en utsjekkingsside som bruker den nye malen.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kjøpsboksmodul](add-buy-box.md)

[Handlekurvmodul](add-cart-module.md)

[Ordrebekreftelsesmodul](order-confirmation-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)
