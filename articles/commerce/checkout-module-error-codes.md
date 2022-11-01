---
title: Feilreferansekoder for kassemodul
description: Denne artikkelen beskriver feilreferansekoder for kassemodulen som vises i brukerfeilmeldinger i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: cd8269a71e56f23dbe3782ec3ffc69ec3ea6b151
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709664"
---
# <a name="checkout-module-error-reference-codes"></a>Feilreferansekoder for kassemodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Denne artikkelen beskriver feilkoder for kassemodulen som vises i brukerfeilmeldinger i Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce har innført standardiserte feilreferanser som kan inkluderes i elektroniske kanalkontrollfeil som presenteres for online-kunder. I Commerce versjon 10.0.31 og senere inneholder feilmeldinger i sjekkmodulen feilkoder og viser ikke unødvendig informasjon til online-kunden. Feilkodene refererer til feil som er beskrevet i denne artikkelen.

Avhengig av feilen som oppstår, inneholder tabellen i denne artikkelen følgende detaljer:

- En beskrivelse av betingelsen som forårsaket feilen, eller flere detaljer
- Informasjon som må tas i betraktning i konfigurasjoner for miljø- eller betalingskontakt
- Informasjon som det er mulig å referere til i et støtteapparat hvis det kreves mer hjelp

## <a name="checkout-module-error-reference-codes"></a>Feilreferansekoder for kassemodul

Bruk tabellen nedenfor til å få mer informasjon om feilkodereferanser som tilbys av kunder eller erfarne brukere i online-butikken.

| Feilkode | Dynamics-korrelert feilkode | Feilbeskrivelse |
| ---------- | ------------------------------ | ----------------- |
| CCR001     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardTypeMissingOrNotSupported | Betalingen kan ikke autoriseres. Korttype-ID i **TokenizedPaymentCard** mangler, eller korttype-ID støttes ikke. |
| CCR002     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePayment | Avvist. Betalingen kan ikke autoriseres. |
| CCR003     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardAdditionalContextRequired | Betalingen kan ikke autoriseres. Ytterligere informasjon kreves fra kunden. |
| CCR004     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToRetrieveCardPaymentAcceptResult | Beklager, noe gikk galt. Vi kan ikke hente resultatet av godkjenning av kortbetaling. Prøv på nytt eller kontakt systemadministratoren. |
| CCR005     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentRequiresMerchantProperties | Ikke mulig å betale på grunn av manglende forhandlerbetalingsegenskaper. Kontakt systemansvarlig. |
| CCR006     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidPaymentRequest | Kan ikke hente betalingsmiddeltjenesten for operasjonen. Kontroller konfigurasjonen av betalingsmåten for betalingsmiddelet som er valgt. |
| CCR007     | Microsoft\_Dynamics\_Commerce\_Runtime\_MultipleCustomerAccountPaymentsNotAllowed | En kundekontobetaling er allerede brukt, og bare én betaling er tillatt per transaksjon. |
| CCR008     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountLimitSignDifferentFromAmountDue | Kundekontogrensen avviker fra det forfalte beløpet. Prøve en annen betalingsmåte, eller ta kontakt med kundestøtte for hjelp. |
| CCR009     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsTotalAmountForCarryOutAndReturnItems | Kundekontobetalingen overskrider det totale forfalte beløpet for varene i listen. Prøv på nytt senere, eller kontakt kundestøtten for hjelp. |
| CCR010     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentUsingUnauthorizedAccount | Kundekontobetalingen krever egen konto eller en samsvarende fakturakonto på en betalingsmiddellinje. |
| CCR011     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsCustomerAccountFloorLimit | Kan ikke behandle en kundekontobetaling nå. Gulvgrenseverdien er overskredet. |
| CCR012     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentForCustomerWithoutAllowOnAccount | Denne kunden har ikke tillatelse til å betale a konto. |
| CCR013     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToCancelPayment | Beklager, noe gikk galt. Betalingen kan ikke kanselleres. Prøv på nytt. |
| CCR014     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToReadCardTokenInfo | Det oppstod en feil under behandling av betalingen. Prøv på nytt senere. |
| CCR015     | Microsoft\_Dynamics\_Commerce\_Runtime\_NotEnoughRewardPoints | Fordelsbetalingsbeløpet overskrider det som er tillatt for fordelskortet som brukes i denne transaksjonen. |
| CCR016     | Microsoft\_Dynamics\_Commerce\_Runtime\_RefundAmountMoreThanAllowed | Fordelsrefunderingsbeløpet overskrider det som er tillatt for fordelskortet som brukes i denne transaksjonen. |
| CCR017     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidLoyaltyCardNumber | Finner ikke fordelskortnummeret. Aktiver fordelskortnummeret eller angi et annet kortnummer, og prøv deretter på nytt. |
| CCR018     | Microsoft\_Dynamics\_Commerce\_Runtime\_BlockedLoyaltyCard | Fordelskortnummeret er ikke tilgjengelig. Angi et annet kortnummer, og prøv deretter på nytt. |
| CCR019     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoTenderLoyaltyCard | Dette fordelskortet kan ikke brukes til å løse inn fordelspoeng for denne transaksjonen. |
| CCR020     | Microsoft\_Dynamics\_Commerce\_Runtime\_GiftCardCurrencyMismatch | Det oppstod en feil i gavekortnummeret. Prøv et annen gavekort, eller ta kontakt med kundestøtte for hjelp. |
| CCR021     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAmountExceedsGiftBalance | Beløpet overskrider saldoen på gavekortet. Angi et annet beløp, og prøv deretter på nytt. |
| CCR022     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoMoreThanOneLoyaltyTender | Transaksjonen kan ikke inneholde mer enn én fordelsbetalingslinje. |
| CCR023     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAlreadyVoided | Betalingsinformasjonen er enten manglende eller feil. Bekreft betalingsinformasjonen, og prøv på nytt. |
| CCR024     | Microsoft\_Dynamics\_Commerce\_Runtime\_FraudRisk | Ordren kan ikke behandles for øyeblikket. Prøv på nytt senere. |
| CCR025     | Avbrudd på kundesiden for kasse-API | Operasjonen på kundesiden er tidsavbrutt. Bekreft om ordren er behandlet i Dynamics 365 Commerce headquarters. |
| CCR026     | Opprinnelig autorisert beløp endret | Ordrebeløpet er endret fra det opprinnelige autorisasjonsbeløpet som behandles med betalingsportalen. Dette kan skyldes et tidutløp av en kupong, kampanje eller salg. |
| CCR027     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidCartVersion | Det oppstod en feil under behandling en betaling. Referansen som oppgis til handlekurv-API, har en annen referanse enn forventet (og noterer potensiell inkonsekvens under utsjekkingsprosessen). |
| CCR028     | Microsoft\_Dynamics\_Commerce\_Runtime\_MissingRequiredCartTenderLines | Det har oppstått en feil i betalingsmåten som ble forsøkt. Kontakt kundestøtte for å se gjennom kontoinnstillingene, eller prøv på nytt med en annen betalingsmåte. |

## <a name="additional-resources"></a>Tilleggsressurser

[Vanlige spørsmål om betalinger](dev-itpro/payments-retail.md)

[Kassemodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)
