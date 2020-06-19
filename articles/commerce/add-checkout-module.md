---
title: Kassemodul
description: Dette emnet beskriver hvordan du legger til en kassemodul på en side og angir de nødvendige egenskapene.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: bd1d66fc39872019fc38dbbfb56dc3015d57d0dd
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411218"
---
# <a name="checkout-module"></a>Kassemodul


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du legger til en kassemodul på en side og angir de nødvendige egenskapene.

## <a name="overview"></a>Oversikt

En kassemodul er en spesialcontainer som er vert for alle modulene som kreves for å opprette en ordre. Den viser en trinnvis flyt som en kunde bruker til å angi all relevant informasjon for å foreta et kjøp. Den henter forsendelsesadressen, leveringsmetoden og faktureringsinformasjonen. Den gir også et ordresammendrag og annen informasjon som er knyttet til en kundeordre.

En kassemodul gjengir data basert på handlekurv-IDen. Denne handlekurv-IDen lagres som en informasjonskapsel i leseren. En handlekurv-ID kreves for å gjengi informasjon i kassemodulen, for eksempel varene i ordren, totalbeløpet og rabattene. 

Bildet nedenfor viser et eksempel på en Fabrikam-kassemodul på en kasseside.

![Eksempel på en kassemodul](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a>Egenskaper i kassemodulen

En kassemodul viser et ordresammendrag og inneholder funksjonalitet for å legge inn en ordre. Hvis du vil samle all kundeinformasjon som kreves før en ordre kan legges inn, må ytterligere moduler legges til i kassemodulen. Derfor har forhandlere fleksibilitet til å legge til egendefinerte moduler i utsjekkingsflyten eller utelate moduler, basert på deres behov.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moduler som kan brukes i kassemodulen

- **Leveringsadresse** – Med denne modulen kan en kunde legge til eller velge leveringsadressen for en ordre. Hvis kunden er logget på, vises alle adresser som tidligere ble lagret for den kunden. Kunden kan deretter velge blant disse adressene. Kunden kan også legge til en ny adresse. Leveringsadressen brukes for alle varene i ordren som krever levering. Den kan ikke tilpasses for individuelle linjeelementer. Leveringsadresseformater defineres for hvert land eller område, og land/område-spesifikke regler håndheves av denne modulen. Selv om denne modulen ikke gir adressevalidering, kan adressevalidering implementeres ved hjelp av tilpassing. Hvis ordren bare omfatter varer som skal plukkes i butikken, blir denne modulen automatisk skjult.

    Bildet nedenfor viser et eksempel på en leveringsadressemodul på en kasseside.

    ![Eksempel på en leveringsadressemodul](./media/ecommerce-shippingaddress.PNG)

- **Leveringsalternativer** – I denne modulen kan en kunde velge et leveringsalternativ for en ordre. Leveringsalternativene er basert på leveringsadressen. Hvis leveringsadressen endres, må leveringsalternativene hentes på nytt. Hvis ordren bare omfatter varer som skal plukkes i butikken, blir denne modulen automatisk skjult.

    Bildet nedenfor viser et eksempel på en leveringsalternativer-modul på en kasseside.

    ![Eksempel på en modul for leveringsalternativer](./media/ecommerce-deliveryoptions.PNG)

- **Container for betalingsdel** – Denne modulen er en container som du kan sette flere moduler i for å opprette en del innenfor betalingsflyten. Du kan for eksempel plassere alle betalingsrelaterte moduler i denne containeren for å vise dem som én inndeling. Denne modulen har bare innvirkning på oppsettet for flyten.
- **Gavekort** – Ved hjelp av denne modulen kan en kunde betale for en ordre ved å bruke et gavekort. Den støtter bare Microsoft Dynamics 365 Commerce-gavekort. Ett eller flere gavekort kan brukes i en ordre. Hvis saldoen på gavekortet ikke dekker beløpet i handlekurven, kan gavekortet kombineres med en annen betalingsmåte. Gavekort kan bare løses inn hvis kunden er logget på.
- **Fordelspoeng** – Denne modulen gjør det mulig for en kunde å betale for en ordre ved å bruke fordelspoeng. Den gir et sammendrag av tilgjengelige poeng og utløpende poeng og lar kunden velge antall poeng du vil løse inn. Hvis kunden ikke er logget på eller ikke er fordelsmedlem, eller hvis totalbeløpet i handlekurven er 0 (null), blir denne modulen automatisk skjult.
- **Betaling** – Ved hjelp av denne modulen kan en kunde betale for en ordre ved å bruke et kredittkort. Hvis totalbeløpet i handlekurven dekkes av fordelspoeng eller et gavekort, eller hvis det er 0 (null), blir denne modulen automatisk skjult. Kredittkortintegrasjon leveres av betalingskoblingen Adyen for denne modulen. Hvis du vil ha mer informasjon om hvordan du bruker denne koblingen, se [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).
- **Fakturaadresse** – Ved hjelp av denne modulen kan en kunde angi betalingsinformasjon. Denne informasjonen behandles sammen med kredittkortinformasjonen, etter Adyen. Denne modulen inneholder et alternativ som brukes til å la kundene bruke faktureringsadressen som leveringsadresse.

    Følgende bilde viser et eksempel på en gavekort-, fordelspoeng-, betalings- og faktureringsadresse-modul på en kasseside.

    ![Eksempel på moduler for gavekort, fordelspoeng, betaling og faktureringsadresse](./media/ecommerce-payments.PNG)

- **Kontaktinformasjon** – Ved hjelp av denne modulen kan en kunde legge til eller endre kontaktinformasjonen (e-postadresse) for en ordre.

- **Tekstblokk** – Denne modulen inneholder alle meldinger som drives av innholdsstyringssystemet (CMS). Den kan for eksempel inneholde en melding som sier "For problemer med bestillingen, ta kontakt med 1-800-Fabrikam". 

## <a name="commerce-scale-unit-interaction"></a>Samhandling med Commerce Scale Unit

Det meste av informasjonen i kassen, for eksempel forsendelsesadressen og forsendelsesmetoden, lagres i handlekurven og behandles som en del av ordren. Det eneste unntaket er kredittkortinformasjonen. Denne informasjonen behandles direkte ved hjelp av betalingskoblingen Adyen. Betalingen godkjennes, men belastes ikke.

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a>Legge til en kassemodul på en side, og angi de nødvendige egenskapene

Hvis du vil legge til en kassemodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Gå til **Sidefragmenter**, og velg **Ny** for å opprette et nytt sidefragment.
1. I dialogboksen **Nytt sidefragment** velger du **Kasse**-modulen.
1. Under **Navn på sidefragment** angir navnet **Kassefragment**, og deretter velger du **OK**.
1. Velg **Kassemodul**-sporet.
1. I egenskapsruten til høyre velger du blyantsymbolet, angir overskriftsteksten i feltet, og merker av for avmerkingssymbolet.
1. I **Kasseinformasjon**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I **Legg til modul**-dialogboksen velger du modulene **Leveringsadresse**, **Leveringsalternativer**, **Beholder for betalingsdel** og **Kontaktinformasjon**, og velger deretter **OK**.
1. I **Beholder for betalingsdel**-modulen velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du modulene **Gavekort**, **Fordel** og **Betaling**, og deretter velger du **OK**. På denne måten sørger du for at alle betalingsmåtene vises sammen i en del.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise fragmentet. Noen moduler som ikke har en handlekurvkontekst, gjengis kanskje ikke i forhåndsvisningen.
1. Velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere den.
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
