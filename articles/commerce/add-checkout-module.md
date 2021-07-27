---
title: Kassemodul
description: Dette emnet beskriver hvordan du legger til en kassemodul på en side og angir de nødvendige egenskapene.
author: anupamar-ms
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bda264a255a688d64e314d994dc281602c9324cc
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347596"
---
# <a name="checkout-module"></a>Kassemodul

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du legger til en kassemodul på en side og angir de nødvendige egenskapene.

En kassemodul er en spesialcontainer som er vert for alle modulene som kreves for å opprette en ordre. Den viser en trinnvis flyt som en kunde bruker til å angi all relevant informasjon for å foreta et kjøp. Den henter forsendelsesadressen, leveringsmetoden og faktureringsinformasjonen. Den gir også et ordresammendrag og annen informasjon som er knyttet til en kundeordre.

En kassemodul gjengir data basert på handlekurv-IDen. Denne handlekurv-IDen lagres som en informasjonskapsel i leseren. En handlekurv-ID kreves for å gjengi informasjon i kassemodulen, for eksempel varene i ordren, totalbeløpet og rabattene. 

Bildet nedenfor viser et eksempel på en Fabrikam-kassemodul på en kasseside.

![Eksempel på en kassemodul.](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a>Egenskaper i kassemodulen

En kassemodul viser et ordresammendrag og inneholder funksjonalitet for å legge inn en ordre. Hvis du vil samle all kundeinformasjon som kreves før en ordre kan legges inn, må ytterligere moduler legges til i kassemodulen. Derfor har forhandlere fleksibilitet til å legge til egendefinerte moduler i utsjekkingsflyten eller utelate moduler, basert på deres behov.

| Egenskapsnavn | Verdier | beskrivelse |
|----------------|--------|-------------|
| Overskrift for utsjekking | Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | En overskrift for kassemodulen. |
| Overskrift for ordresammendrag | Overskriftstekst | En overskrift for ordresammendragsdelen i modulen. |
| Overskrift for linjeelementer for handlekurv | Overskriftstekst | Overskrift for varer i handlekurven som vises i kassemodulen. |
| Vis forsendelseskostnader for linjevare | **Sann** eller **Usann** | Hvis denne egenskapen er satt til **Sann**, vises forsendelseskostnadene som gjelder for linjevarer, på handlekurvlinjer. Hvis funksjonen **Overskriftsgebyr uten fordeling** er aktivert i Commerce Headquarters, vil forsendelseskostnaden bli brukt på overskriftsnivået, ikke på linjenivået. Denne funksjonen ble lagt til i Commerce versjon 10.0.13. |

## <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moduler som kan brukes i kassemodulen

- **Leveringsadresse** – Med denne modulen kan en kunde legge til eller velge leveringsadressen for en ordre. Hvis du vil ha mer informasjon om denne modulen, kan du se [Leveringsadressemodul](ship-address-module.md).

    Bildet nedenfor viser et eksempel på en leveringsadressemodul på en kasseside.

    ![Eksempel på en leveringsadressemodul.](./media/ecommerce-shippingaddress.PNG)

- **Leveringsalternativer** – I denne modulen kan en kunde velge en leveringsmodus for en ordre. Hvis du vil ha mer informasjon om denne modulen, kan du se [Modul for leveringsalternativer](delivery-options-module.md).

    Bildet nedenfor viser et eksempel på en leveringsalternativer-modul på en kasseside.
 
    ![Eksempel på en modul for leveringsalternativer.](./media/ecommerce-deliveryoptions.PNG)

- **Container for betalingsdel** – Denne modulen er en container som du kan sette flere moduler i for å opprette en del innenfor betalingsflyten. Du kan for eksempel plassere alle betalingsrelaterte moduler i denne containeren for å vise dem som én inndeling. Denne modulen har bare innvirkning på oppsettet for flyten.

- **Gavekort** – Ved hjelp av denne modulen kan en kunde betale for en ordre ved å bruke et gavekort. Hvis du vil ha mer informasjon om denne modulen, kan du se [Gavekortmodul](add-giftcard.md).

- **Fordelspoeng** – Denne modulen gjør det mulig for en kunde å betale for en ordre ved å bruke fordelspoeng. Den gir et sammendrag av tilgjengelige poeng og utløpende poeng og lar kunden velge antall poeng du vil løse inn. Hvis kunden ikke er logget på eller ikke er fordelsmedlem, eller hvis totalbeløpet i handlekurven er 0 (null), blir denne modulen automatisk skjult.

- **Betaling** – Ved hjelp av denne modulen kan en kunde betale for en ordre ved å bruke et kredittkort eller et debetkort. Kunder kan også oppgi faktureringsadresse for betalingsalternativet de velger. Hvis du vil ha mer informasjon om denne modulen, kan du se [Betalingsmodul](payment-module.md).

    Følgende bilde viser et eksempel på en gavekort-, fordelspoeng- og betalingsmodul på en kasseside.

    ![Eksempel på en gavekort-, fordelspoeng- og betalingsmodul på en kasseside.](./media/ecommerce-payments.PNG)

- **Kontaktinformasjon** – Ved hjelp av denne modulen kan en kunde legge til eller endre kontaktinformasjonen (e-postadresse) for en ordre.

- **Tekstblokk** – Denne modulen inneholder alle meldinger som drives av innholdsstyringssystemet (CMS). Den kan for eksempel inneholde en melding som sier "For problemer med bestillingen, ta kontakt med 1-800-Fabrikam". 

- **Betalingsvilkår** – Denne modulen viser rik tekst som inneholder vilkårene og en avmerkingsboks for kundeinndataene. Avmerkingsboksen er valgfri og konfigurerbar. Inndataene registreres av modulen og kan brukes som en sjekk før ordreplassering utløses, men den tas ikke med i ordresammendragsinformasjonen. Denne modulen kan legges til i betalingscontaineren, betalingsdelcontaineren eller sporet for vilkår, i henhold til forretningsbehovene. Hvis den legges til i betalingscontaineren eller betalingsdelcontaineren, vises den som et trinn i betalingsprosessen. Hvis den legges til i sporet for vilkår, vises den i nærheten av ordreplasseringsknappen.

    Bildet nedenfor viser et eksempel på vilkår på en kasseside.

    ![Eksempel på vilkår på en betalingsside.](./media/ecommerce-checkout-terms.PNG)

## <a name="commerce-scale-unit-interaction"></a>Samhandling med Commerce Scale Unit

Det meste av informasjonen i kassen, for eksempel forsendelsesadressen og forsendelsesmetoden, lagres i handlekurven og behandles som en del av ordren. Det eneste unntaket er kredittkortinformasjonen. Denne informasjonen behandles direkte ved hjelp av betalingskoblingen Adyen. Betalingen er godkjent, men den blir ikke belastet før ordren er oppfylt.

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a>Legge til en kassemodul på en side, og angi de nødvendige egenskapene

Hvis du vil legge til en kassemodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Gå til **Fragmenter**, og velg **Nytt** for å opprette et nytt sidefragment.
1. I dialogboksen **Nytt fragment** velger du **Kasse**-modulen.
1. Under **Navn på fragment** angir navnet **Kassefragment**, og deretter velger du **OK**.
1. Velg **Kassemodul**-sporet.
1. I egenskapsruten til høyre velger du blyantsymbolet, angir overskriftsteksten i feltet, og merker av for avmerkingssymbolet.
1. I **Kasseinformasjon**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I **Legg til modul**-dialogboksen velger du modulene **Leveringsadresse**, **Leveringsalternativer**, **Beholder for betalingsdel** og **Kontaktinformasjon**, og velger deretter **OK**.
1. I **Beholder for betalingsdel**-modulen velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du modulene **Gavekort**, **Fordel** og **Betaling**, og deretter velger du **OK**. På denne måten sørger du for at alle betalingsmåtene vises sammen i en del.
1. I sporet **Vilkår** legger du til en **Betalingsvilkår**-modul, hvis det er nødvendig. I modulens egenskapsrute konfigurerer du vilkårsteksten etter behov.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise fragmentet. Noen moduler som ikke har en handlekurvkontekst, gjengis kanskje ikke i forhåndsvisningen.
1. Velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere den.
1. Opprett en mal som bruker det nye kassefragmentet.
1. Opprett en utsjekkingsside som bruker den nye malen.

## <a name="additional-resources"></a>Tilleggsressurser

[Handlekurvmodul](add-cart-module.md)

[Handlekurvikonmodul](cart-icon-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Leveringsalternativmodul](delivery-options-module.md)

[Henteinformasjonsmodul](pickup-info-module.md)

[Ordredetaljermodul](order-confirmation-module.md)

[Gavekortmodul](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]