---
title: Forsinke nøyaktig pris- og rabattberegning for forbedret ytelse
description: Denne artikkelen beskriver funksjoner for forsinket prisberegning som er tilgjengelig på Microsoft Dynamics 365 Commerce-salgsstedet (POS) og telefonsenteret.
author: boycezhu
ms.date: 09/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 6926c288a91dbe66b6ffc2e6c06f866d3ebd7652
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845903"
---
# <a name="delay-exact-price-and-discount-calculation-for-improved-performance"></a>Forsinke nøyaktig pris- og rabattberegning for forbedret ytelse

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver funksjoner for forsinket prisberegning som er tilgjengelig på Microsoft Dynamics 365 Commerce-salgsstedet (POS) og telefonsenteret.

Dynamics 365 Commerce støtter oppretting av samkjøpsrabatter som brukes når flere salgslinjer i en salgsordre eller et salgstilbud kombineres. Disse rabattene inkluderer samlerabatter, terskelrabatter og antallsrabatter.

Hver gang en ny linje legges til i en ordre, evaluerer prissettingsmotoren i Commerce hele handlekurven for å fastslå om noen av disse samkjøpsrabattene kan brukes. På grunn av denne omberegningen, kan tillegget av nye linjer påvirke ytelsen etter hvert som en salgsordre vokser.

Bedrift-til-bedrift-firmaer (B2B) og enkelte bedrift-til-kunde-firmaer (B2C) har imidlertid ofte store ordrestørrelser. Derfor kan det være tidkrevende å vente på at prissettingsmotoren skal beregnes på nytt etter at hver vare er lagt til i handlekurven. Dessuten er det vanligvis ikke så viktig at den nøyaktige prisen og rabatten vises hver gang en vare legges til i handlekurven, for store bestillinger. Det er viktig at brukerne raskt kan legge til varer. Muligheten til å utsette nøyaktige pris- og rabattberegninger til en bruker ber om det eller en ordre er ferdigstilt, kan forbedre ytelsen betraktelig. Det kan også redusere tiden det tar å fullføre bestillingen.

Muligheten til å utsette nøyaktige pris- og rabattberegninger har lenge vært tilgjengelig på salgsstedet. Fra og med Commerce versjon 10.0.22 er den også tilgjengelig for telefonsenteret.

## <a name="enable-delayed-price-and-discount-calculation-for-pos"></a>Aktivere forsinket pris- og rabattberegning for salgssted

For å aktivere forsinket pris- og rabattberegning for salgssted følger du disse trinnene.

1. I Commerce-hovedkvarteret går du til funksjonalitetsprofilen som er knyttet til den fysiske butikken.
1. I hurtigkategorien **Beløp** aktiverer du konfigurasjonen **Beregn flere varerabatter manuelt**.
1. Åpne skjermoppsettutforming for kassene der den forsinkede beregningen skal aktiveres.
1. Legg til en knapp for **Beregn total**-operasjonen til den ønskede knappegruppen.
1. Kjør **1070**- og **1090**-jobbene.

Når varer nå legges til i en transaksjon, beregnes ikke samkjøpsrabatter med mindre kassereren velger **Beregn total**-knappen. Når **Beregn total** er valgt for en transaksjon, beregnes det alltid samkjøpsrabatter for den. Kassereren trenger ikke å velge knappen på nytt, selv om flere varer er lagt til i handlekurven. Systemet tillater ikke at kassereren kan registrere betaling før **Beregn total** er valgt.

## <a name="enable-delayed-price-and-discount-calculation-for-call-center"></a>Aktivere forsinket pris- og rabattberegning for telefonsenter

For å aktivere forsinket pris- og rabattberegning for telefonsenter følger du disse trinnene.

1. I Commerce Headquarters går du til **Arbeidsområder \> Funksjonsbehandling**.
1. Aktiver funksjonen **Hindre utilsiktet prisberegning for handelsordrer**. Denne funksjonen er en forutsetning for funksjonen for forsinket pris- og rabattberegning.

    > [!NOTE]
    > For nye distribusjoner er funksjonen **Hindre utilsiktet prisberegning for handelsordrer** aktivert som standard.

1. Gå til **Commerce-parametere \> Priser og rabatter**.
1. I **Diverse**-delen aktiverer du konfigurasjonen **Manuell beregning av flerlinjepriser og rabatter**.

Når en salgsordre eller et salgstilbud blir opprettet eller redigert i telefonsenteret, blir den nøyaktige pris- og rabattberegningen for den forsinket. Prissettingsmotoren vil bare vurdere salgslinjen som legges til eller redigeres, og vil ignorere alle andre salgslinjer. Nettobeløpet for en vare omfatter prisberegning og enkle rabatter (rabattprosent eller rabatt av en enkelt vare). Samlerabatter, terskelrabatter og antallsrabatter brukes imidlertid ikke. Samtalesenterbrukere som vil vise den nøyaktige prisen, inkludert alle rabatter, kan velge én av tre knapper: **Omberegn**, **Totaler** eller **Fullført**.

> [!NOTE]
> Når det gjelder samtalesenterordrer, viser systemet en advarsel slik at brukeren blir påminnet om at de må velge knappen **Beregn på nytt**, **Totaler** eller **Fullført** for at den nøyaktige pris- og rabattberegningen skal utføres. For ordrer der **Fullført**-knappen er tilgjengelig, kan ikke telefonsenterbrukeren utelate den nøyaktige pris- og rabattberegningen, fordi de må velge **Fullfør** for å fullføre ordreregistreringen. For ordrer der **Fullført**-knappen ikke er tilgjengelig, er det ingen handling som indikerer fullføring av ordreregistreringen. Derfor er samtalesenterbrukeren ansvarlig for å velge enten **Omberegn** eller **Totaler** før de fullfører ordreregistreringen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
