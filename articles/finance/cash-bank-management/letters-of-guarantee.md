---
title: Garantibrev
description: Denne artikkelen inneholder informasjon om garantibrev. I et garantibrev godtar en bank å betale et bestemt beløp til en person hvis en av bankens kundene misligholder en betaling eller forpliktelse til denne personen.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankLGGuarantee
audience: Application User
ms.reviewer: kfend
ms.custom: 18291
ms.assetid: 5c0b5e37-d51d-4a01-bb37-1882173abb9f
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24db7e23ec6d360bbae7113e62bb28d4aecd851f
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715367"
---
# <a name="letters-of-guarantee"></a>Garantibrev

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon om garantibrev. I et garantibrev godtar en bank å betale et bestemt beløp til en person hvis en av bankens kundene misligholder en betaling eller forpliktelse til denne personen. 

Et garantibrev er en avtale der en bank (garantisten) skal betale et angitt pengebeløp til en person (mottakeren) hvis en bankkunde (oppdragsgiveren) unnlater å betale gjeld eller en forpliktelse til mottakeren. Garantibrev kan ikke overføres. De gjelder bare mottakeren som er nevnt ved navn i avtalen. Oppdragsgiveren kan be om en økning eller reduksjon i verdien til et garantibrev, underlagt vilkårene i avtalen. 

Hvis du vil ha avvikle et garantibrev, må mottakeren sende originalen av garantibrevet og informere banken om oppdragsgiverens feil før utløpsdatoen. Banken betaler deretter det skyldige beløpet til mottakerens konto, i samsvar med vilkårene i garantibrevet. Banken reserverer en prosent av betalingen som en margin. Prosenten er avtalt og angitt i betingelsene i avtalen. 

Du kan opprette en kode for å spore formålet med et garantibrev. Du kan også angi årsakene som kan knyttes til et garantibrev når brevet annulleres. Du kan vise formålskodene og bankårsakene på sidene **Koder for betalingsformål** og **Bankårsaker**. 

Du kan bruke **Garantibrev**-siden til å fullføre disse oppgavene:

-   Opprett riktige finansposter, og reduser behovet for manuell dataregistrering.
-   Registrer alle monetære og ikke-monetære transaksjoner, og spor saldoer for garantibrev.
-   Registrer og spor statusen og utløpsdatoen for garantibrev.
-   Generer en rapport som viser bankene som har garantibrev.

Tabellen nedenfor beskriver handlingene du kan utføre for et garantibrev.

| Handling              | Formål                                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------------------------------|
| Send til bank      | Send forespørselen om garantibrev til banken.                                                                       |
| Motta fra bank   | Når banken har samtykket i den innsendte forespørselen, får du garantibrevet fra banken.                            |
| Gi til mottaker | Når du har fått garantibrevet fra banken, må du gi garantibrevet til mottakeren.              |
| Øk verdi      | Hvis mottakeren og oppdragsgiveren samtykker, øker du pengeverdien.                                                  |
| Senk verdi      | Hvis mottakeren og oppdragsgiveren samtykker, reduserer du pengeverdien.                                                  |
| Utvid              | Når du har gitt mottakeren garantibrevet, utvider du gyldighetsperioden hvis en forlengelse er nødvendig. |
| Annuller              | Når garantibrevets formål ikke gjelder lenger, annullerer du avtalen.                  |
| Avvikle           | Når mottakeren fremviser garantibrevet for banken, innløser du garantibrevet.                      |


Hvis du vil ha mer informasjon, se følgende emner:

[Garantibrevtransaksjon](tasks/letter-guarantee-transaction.md)

[Definere bankfasiliteter og posteringsprofiler for garantibrev](tasks/set-up-bank-facilities-posting-profiles.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
