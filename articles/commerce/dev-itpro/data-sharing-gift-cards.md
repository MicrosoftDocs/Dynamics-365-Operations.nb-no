---
title: Datadeling for gavekort mellom firmaer
description: Denne artikkelen beskriver hvordan du konfigurerer Microsoft Dynamics 365 Commerce slik at det bruker datadelingsfunksjonaliteten i Dynamics 365 Finance på tvers av dataområder til å synkronisere gavekortdata.
author: BrianShook
ms.date: 08/26/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: b56890b546c3cd74b75cf447e62495733ea8d288
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387071"
---
# <a name="cross-company-data-sharing-for-gift-cards"></a>Datadeling for gavekort mellom firmaer

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer Microsoft Dynamics 365 Commerce slik at det bruker datadelingsfunksjonaliteten i Dynamics 365 Finance til å synkronisere gavekortdata. Funksjonen for deling av dataposter kan deretter brukes til å dele data på tvers av firmaer mellom to dataområder. På denne måten kan den interne Commerce-gavekorttabellen dele data mellom to firmaenheter. Hvis du vil ha mer informasjon om deling av data på tvers av firmaer i Dynamics 365 Finance, [Datadeling mellom firmaer](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

## <a name="key-terms"></a>Viktige termer

| Semester | Beskrivelse |
|---|---|
| Selskap | Den juridiske enheten i Dynamics 365 Finance-miljøet. |
| Gavekort | Det interne gavekortproduktet i Dynamics 365 Commerce. |

## <a name="prerequisites"></a>Forutsetninger

Brukere må konfigurere miljøet for deling av data på tvers av firmaer som beskrevet i [Datadeling mellom firmaer](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

**RetailGiftCardTable** må ha feltet **DataSharingType** satt til **Duplikat** for å aktivere deling av duplisert post for gavekorttabellen. Hvis du vil ha mer informasjon, kan du se [Datadeling mellom firmaer for utviklere](/dynamics365/fin-ops-core/dev-itpro/sysadmin/drs-srs-dev).

## <a name="configure-cross-company-data-sharing-for-gift-cards"></a>Konfigurer datadeling for gavekort mellom firmaer

Følg trinnene nedenfor for å konfigurere datadeling for gavekort mellom firmaer.

1. I Commerce headquarters går du til **Systemadministrasjon \> Oppsett \> Konfigurer datadeling mellom firmaer**.
1. Velg **Ny** i handlingsruten for å legge til en datadelingspost.
1. Skriv inn et navn for datadelingsposten i **Navn**-feltet (for eksempel **Gavekort**).
1. Velg **Legg til** i delen **Tabeller og felter for deling**.
1. Skriv inn **RETAILGIFTCARDTABLE** (tabellen for gavekort for detaljhandel) i **Tabellnavn**-feltet i dialogboksen **Del ny tabell**. **Gavekorttabell** skal angis automatisk i feltet **Tabelletikett**.
1. Kontroller at det er merket av for **Lagre data per firma**, **Har unik indeks** og **Ikke delt ennå**. Når det er merket av for disse alternativene, utløses valideringer som er knyttet til datadelingsfunksjonaliteten.
1. Velg **Legg til tabell**. Posten **Gavekorttabell (RetailGiftCardTable)** skal nå vises under **Tabeller og felter for deling**. Velg cirkumflekstegnet (^) for å vise alle tabellfeltene som knyttes til tabellen for deling automatisk.
1. Velg **Legg til** i delen **Firmaer som deler poster i disse tabellene** for å legge til et firma du vil dele data med.
1. Velg et firma fra rullegardinlisten i raden under **Firma**.
1. Angi firmanavnet i **Navn**-feltet.
1. Gjenta trinn 8 til og med 10 hvis du vil legge til flere firmarader.
1. Når du er ferdig å legge til firmarader, velger du **Aktiver** i handlingsruten.
1. Du får en advarsel med følgende melding: «Det anbefales at du bare utfører denne handlingen utenom åpningstid. Alle samtidige transaksjonsoperasjoner mislykkes for tabeller i policyen. Vil du fortsette?» Velg **Ja** for å godta.
1. Du får en advarsel med følgende melding: «Vil du kopiere alle eksisterende data mellom alle delte firmaer nå?» Velg **Ja** for å godta.

Etter at du har godtatt begge meldingene, begynner tabellene å kopiere data mellom de konfigurerte firmaene. Saldoer mot et firmagavekort, vises deretter for det andre firmaet.

## <a name="additional-resources"></a>Tilleggsressurser

[Vanlige spørsmål om betalinger](payments-retail.md)

[Kassemodul](../add-checkout-module.md)

[Betalingsmodul](../payment-module.md)
