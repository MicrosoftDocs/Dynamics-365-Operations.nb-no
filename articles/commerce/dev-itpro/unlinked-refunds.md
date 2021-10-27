---
title: Behandle ikke-sammenkoblede refunderinger med Dynamics 365 Commerce Payment Connector for Adyen
description: Dette emnet beskriver hvordan refunderinger som ikke er sammenkoblet, fungerer når Microsoft Dynamics 365 Payment Connector for Adyen brukes.
author: BrianShook
ms.date: 10/07/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c137dcf7d35031a293c88d8c4f5dc1e5f3d9e2f9
ms.sourcegitcommit: a21a664cd35b95c8600c5af0aac588a64e892902
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/11/2021
ms.locfileid: "7623927"
---
# <a name="process-unlinked-refunds-with-the-dynamics-365-commerce-payment-connector-for-adyen"></a>Behandle ikke-sammenkoblede refunderinger med Dynamics 365 Commerce Payment Connector for Adyen

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan refunderinger som ikke er sammenkoblet, fungerer når [Microsoft Dynamics 365 Payment Connector for Adyen](adyen-connector.md) brukes. Det gjennomgår også muligheten til å behandle en refusjon mot en ny betalingsmetode i salgsstedet eller telefonsenteret.

Dynamics 365 Payment Connector for Adyen støtter muligheten til å behandle refunderinger ved hjelp av en annen betalingsmetode enn den som ble brukt for den opprinnelige transaksjonen. Selv om vi anbefaler at du bruker [sammenkoblede refusjoner](linked-refunds.md) til å behandle en refusjon mot den opprinnelige betalingsmetoden som ble angitt, kreves refusjoner til en annen metode i enkelte scenarioer. Kortet som ble brukt for den opprinnelige betalingen, kan for eksempel være utløpt eller mistet, eller det kan ha blitt sperret av brukeren.

## <a name="prerequisites"></a>Forutsetninger

Følgende forutsetninger må være fullført før Dynamics 365 Payment Connector for Adyen kan behandle ikke-sammenkoblede refusjoner:

- Konfigurer [betalingsmetoder](../payment-methods.md).
- Konfigurer [betalinger for omnikanal](../omni-channel-payments.md).

## <a name="additional-configuration"></a>Tilleggskonfigurasjon

Dynamics 365 Payment Connector for Adyen gir en enkel implementering av alle støttede refunderingsscenarioer som er beskrevet i neste avsnitt. Kunder som ikke bruker standardimplementeringen av Dynamics 365 Payment Connector for Adyen, må konfigurere koblingen som støtter tokenisering av kredittkort.

## <a name="supported-refund-scenarios"></a>Refunderingsscenarioer som støttes

Dynamics 365 Commerce støtter refunderinger av transaksjoner som tidligere er godkjent og bekreftet. Refunderinger kan bestå av enten en fullstendig refundering eller en delvis refundering av transaksjonen. Refunderinger kan ikke overskride hele beløpet i den opprinnelige betalingsautorisasjonen. Refunderinger som ikke er sammenkoblet, støttes bare i salgssenter og telefonsenter.

## <a name="enable-unlinked-refunds-functionality"></a>Aktiver funksjonalitet for refunderinger som ikke er sammenkoblet

Hvis du vil aktivere funksjonalitet for refunderinger som ikke er sammenkoblet, i Commerce Headquarters, gjør du følgende.

1. Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> Delte handelsparametere**.
1. På fanen **Omnikanal-betalinger** setter du alternativet **Bruk betalinger for omnikanal** til **Ja**.

### <a name="supported-payment-method-variants"></a>Støttede betalingsmåtevarianter

Følgende varianter for betalingsmetode støtter som standard refunderinger som ikke er sammenkoblet:

- Kort
- Lommebok

Ikke alle variantene av betalingsmetode støtter refunderinger som ikke er sammenkoblet. Tabellen nedenfor viser en liste over vanlige betalingsmetoder, og viser støttefunksjonene for hver metode for sammenkoblede og ikke-sammenkoblede refunderinger.

| Betalingsmåte        | Sammenkoblet refundering | Ikke-sammenkoblet refundering |
|-----------------------|:-------------:|:---------------:|
| amexcommercial        | Ja           | Ja             |
| amexconsumer          | Ja           | Ja             |
| amexcorporate         | Ja           | Ja             |
| amexdebit             | Ja           | Ja             |
| amexprepaid           | Ja           | Ja             |
| amexprepaidreloadable | Ja           | Ja             |
| amexsmallbusiness     | Ja           | Ja             |
| discover              | Ja           | Ja             |
| maestro               | Ja           | Ja             |
| maestrouk             | Ja           | Ja             |
| mc                    | Ja           | Ja             |
| mcalphabankbonus      | Ja           | Ja             |
| mcprepaidanonymous    | Ja           | Ja             |
| visa                  | Ja           | Ja             |
| visaalphabankbonus    | Ja           | Ja             |
| visacheckout          | Ja           | Ja             |
| visadankort           | Ja           | Ja             |
| visahipotecario       | Ja           | Ja             |
| visasaraivacard       | Ja           | Ja             |
| vpay                  | Ja           | Ja             |
| givex                 | **Nei**        | Ja             |
| svs                   | **Nei**        | Ja             |
| cup                   | Ja           | Ja             |
| diners                | Ja           | Ja             |
| interac               | **Nei**        | Ja             |
| jcb                   | Ja           | Ja             |
| jcb_applepay          | Ja           | Ja             |
| unionpay              | Ja           | Ja             |

### <a name="process-an-unlinked-refund-in-pos"></a>Behandle en ikke-sammenkoblet refundering i salgsstedet

En kunde returnerer en vare til en salgsstedskasserer i den tillatte perioden for returer, og har en gyldig kvittering. Under behandling for returen inneholder dialogboksen **Returbetaling** et alternativ for **Velg en betalingsmetode**. Kassereren kan deretter velge en betalingsmetode blant betalingsmetodene som støttes for refundering (kort og lommebok).

### <a name="process-an-unlinked-refund-in-call-center"></a>Behandle en ikke-sammenkoblet refundering i telefonsenteret

Når en refundering som ikke er sammenkoblet, behandles mot en ordre i telefonsenteret, velger en telefonsenteransatt en betalingsmetode som er forskjellig fra den opprinnelige metoden. Deretter blir den ansatte bedt om å få en administrator til å overstyre PIN-nummeret. PIN-koden er nødvendig før den andre betalingsmetode kan behandles for refunderinger.

#### <a name="set-up-an-administrator-override-pin-for-call-center"></a>Konfigurer en administratoroverstyrings-PIN-kode for telefonsenter

Følg denne fremgangsmåten for å konfigurere en administratoroverstyrings-PIN-kode for telefonsenter i Commerce Headquarters.

1. Gå til **Retail og Commerce \> Kanaloppsett \> Telefonsenteroppsett**, eller søk etter Overstyringstillatelser.
1. Velg rollen som du vil tillate behandlingstillatelser for refundering som ikke er sammenkoblet.
1. I hurtigfanen **Returer** setter du alternativet **Tillat alternativ betaling** til **Ja**.

## <a name="additional-resources"></a>Tilleggsressurser

[Dynamics 365 Payment Connector for Adyen](adyen-connector.md)

[Koblede refunderinger av tidligere godkjente og bekreftede transaksjoner](linked-refunds.md)
