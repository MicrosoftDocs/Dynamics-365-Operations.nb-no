---
title: Rabattbehandlingsgrupper
description: Dette emnet beskriver hvordan du setter opp rabattbehandlingsgrupper. Rabattbehandlingsgrupper kan brukes under rabattberegninger, og kan knyttes til en hovedoppføring.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: cef7abbbf2a94e26b6b9e66492cd7347d3b4d1f2
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920067"
---
# <a name="rebate-management-groups"></a>Rabattbehandlingsgrupper

[!include [banner](../includes/banner.md)]

Beregninger av rabatt og fradrag kan drives av grupper. Rabattbehandlingsgrupper kan opprettes for kunder, leverandører og varer. De kan knyttes til en hovedoppføring.

## <a name="rebate-management-customer-groups"></a>Rabattbehandlingskundegrupper

Beregningen for en gruppe kunder opprettes ofte for en kjede av firmaer, for eksempel en butikkjede eller et franchisefirma. Denne typen beregning er vanligvis knyttet til en rabatt.

Et fradrag beregnes ofte uten å vurdere hvem den kvalifiserende ordren ble solgt til. Det finnes imidlertid noen unntak. En lisenstaker kan for eksempel opprette en fradragsplan der kundegruppe A mottar 4 prosent, men kundegruppe B mottar bare 3 prosent.

### <a name="set-up-customer-groups"></a>Definer kundegrupper

Hvis du vil arbeide med kundegrupper for rabattstyring, kan du gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Kundegrupper**. Du kan bruke knappene i handlingsruten til å legge til og fjerne grupper etter behov. For hver gruppe angir du feltene nedenfor:

- **Rabattbehandlingsgruppe** – Angi et unikt navn for gruppen.
- **Beskrivelse** – Angi en beskrivelse av gruppen for å få mer informasjon om hvordan den skal brukes.

### <a name="manage-customer-group-assignments"></a>Administrer tilordninger av kundegrupper

Hver kunde kan tilhøre et hvilket som helst antall rabattbehandlingsgrupper. Hvis du vil vise og tilordne gruppemedlemmer, kan du starte fra enten gruppelisten eller kundelisten.

Følg denne fremgangsmåten for å vise, legge til eller fjerne kunder for en valgt gruppe.

1. Gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Kundegrupper**.
1. Velg gruppen som skal administreres.
1. Velg **Kunder** i handlingsruten. Siden **Rabattbehandlingsgrupper** vises med en liste over kunder som allerede er medlemmer av den valgte gruppen.
1. Hvis du vil legge til en ny kunde i gruppen, velger du **Ny** i handlingsruten for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Kundekonto** – Velg kundekonto-ID-en.
    - **Navn** – Angi et navn og/eller en beskrivelse for kunden.

1. Hvis du vil fjerne en kunde fra gruppen, velger du kunden og velger deretter **Slett** i handlingsruten.

Følg denne fremgangsmåten for å vise, legge til eller fjerne gruppetilordninger for en valgt kunde.

1. Gå til **Kunder \> Kunder \> Alle kunder**.
1. Velg kunden du vil arbeide med.
1. I handlingsruten, på fanen **Kunde**, i **Rabattbehandling**-gruppen, velger du **Rabattbehandlingsgrupper**. Siden **Rabattbehandlingsgrupper** vises med en liste over grupper som den valgte kunden allerede hører til i.
1. Hvis du vil legge til kunden i en ny gruppe, velger du **Ny** i handlingsruten for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Rabattbehandlingsgruppe** – Velg gruppen du vil legge til kunden i.
    - **Beskrivelse** – Angi en beskrivelse av gruppen (for eksempel for å forklare hvorfor kunden er medlem av den).

1. Hvis du vil fjerne en kunde fra en gruppe, velger du gruppen og velger deretter **Slett** i handlingsruten.

## <a name="rebate-management-vendor-groups"></a>Rabattbehandlingsleverandørgrupper

Beregningen for en gruppe med leverandører opprettes ofte for en gruppe med leveringspunkter. Denne typen beregning er vanligvis knyttet til en rabatt.

### <a name="set-up-vendor-groups"></a>Definer leverandørgrupper

Hvis du vil arbeide med leverandørgrupper for rabattstyring, kan du gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Leverandørgrupper**. Du kan bruke knappene i handlingsruten til å legge til og fjerne grupper etter behov. For hver gruppe angir du feltene nedenfor:

- **Rabattbehandlingsgruppe** – Angi et unikt navn for gruppen.
- **Beskrivelse** – Angi en beskrivelse av gruppen for å få mer informasjon om hvordan den skal brukes.

### <a name="manage-vendor-group-assignments"></a>Administrer tilordninger av leverandørgrupper

Hver leverandør kan tilhøre et hvilket som helst antall rabattbehandlingsgrupper. Hvis du vil vise og tilordne gruppemedlemmer, kan du starte fra enten gruppelisten eller leverandørlisten.

Følg denne fremgangsmåten for å vise, legge til eller fjerne leverandører for en valgt gruppe.

1. Gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Leverandørgrupper**.
1. Velg gruppen som skal administreres.
1. Velg **Leverandører** i handlingsruten. Siden **Rabattbehandlingsgrupper** vises med en liste over leverandører som allerede er medlemmer av den valgte gruppen.
1. Hvis du vil legge til en ny leverandør i en gruppe, velger du **Ny** i handlingsruten for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Leverandørkonto** – Velg leverandørkonto-ID-en.
    - **Navn** – Angi et navn og/eller en beskrivelse for leverandøren.

1. Hvis du vil fjerne en leverandør fra gruppen, velger du leverandøren og velger deretter **Slett** i handlingsruten.

Følg denne fremgangsmåten for å vise, legge til eller fjerne gruppetilordninger for en valgt leverandør.

1. Gå til **Leverandører \> Leverandører \> Alle leverandører**.
1. Velg leverandøren du vil arbeide med.
1. I handlingsruten, på fanen **Leverandør**, i **Rabattbehandling**-gruppen, velger du **Rabattbehandlingsgrupper**. Siden **Rabattbehandlingsgrupper** vises med en liste over grupper som den valgte leverandøren allerede hører til i.
1. Hvis du vil legge til leverandøren i en ny gruppe, velger du **Ny** i handlingsruten for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Rabattbehandlingsgruppe** – Velg gruppen du vil legge til leverandøren i.
    - **Beskrivelse** – Angi en beskrivelse av gruppen (for eksempel for å forklare hvorfor leverandøren er medlem av den).

1. Hvis du vil fjerne en leverandør fra en gruppe, velger du gruppen og velger deretter **Slett** i handlingsruten.

## <a name="item-rebate-groups"></a>Varerabattgrupper

Ved å gruppere varer har du mer fleksibilitet når rabatter og fradrag beregnes. Denne fremgangsmåten er ofte en mer effektiv måte å definere rabatter og fradrag for kunder og leverandører.

### <a name="set-up-item-groups"></a>Definer varegrupper

Hvis du vil arbeide med varegrupper for rabattstyring, kan du gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Varegrupper**. Du kan bruke knappene i handlingsruten til å legge til og fjerne grupper etter behov. For hver gruppe angir du feltene nedenfor:

- **Rabattbehandlingsgruppe** – Angi et unikt navn for gruppen.
- **Beskrivelse** – Angi en beskrivelse av gruppen for å få mer informasjon om hvordan den skal brukes.

### <a name="manage-item-group-assignments"></a>Administrer tilordninger av varegrupper

Hver vare kan tilhøre et hvilket som helst antall rabattbehandlingsgrupper. Hvis du vil vise og tilordne gruppemedlemmer, kan du starte fra enten gruppelisten eller varelisten. Du kan også legge til varer basert på kategorihierarkiet.

Følg denne fremgangsmåten for å vise, legge til eller fjerne varer for en valgt gruppe.

1. Gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Varegrupper**.
1. Velg gruppen som skal administreres.
1. Velg **Varer** i handlingsruten. Siden **Rabattbehandlingsgrupper** vises med en liste over varer som allerede er medlemmer av den valgte gruppen.
1. Hvis du vil legge til en ny vare i gruppen, velger du **Ny** i handlingsruten for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Varekonto** – Velg varekonto-ID-en.
    - **Produktnavn** – Angi et navn og/eller en beskrivelse for varen.

1. Hvis du vil fjerne en vare fra gruppen, velger du varen og velger deretter **Slett** i handlingsruten.

Følg denne fremgangsmåten for å vise, legge til eller fjerne gruppetilordninger for en valgt vare.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Velg varen du vil arbeide med.
1. I handlingsruten, på fanen **Produkt**, i **Rabattbehandling**-gruppen, velger du **Rabattbehandlingsgrupper**. Siden **Rabattbehandlingsgrupper** vises med en liste over grupper som den valgte varen allerede hører til i.
1. Hvis du vil legge til varen i en ny gruppe, velger du **Ny** i handlingsruten for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Rabattbehandlingsgruppe** – Velg gruppen du vil legge til varen i.
    - **Beskrivelse** – Angi en beskrivelse av gruppen (for eksempel for å forklare hvorfor varen er medlem av den).

1. Hvis du vil fjerne en vare fra en gruppe, velger du gruppen og velger deretter **Slett** i handlingsruten.

Følg denne fremgangsmåten for å legge til varer i en gruppe basert på kategorihierarkiet.

1. Gå til **Rabattbehandling \> Oppsett av rabattbehandlingsgrupper \> Varegrupper**.
1. Velg gruppen som skal administreres.
1. Velg **Legg til varer** i handlingsruten.
1. I dialogboksen **Legg til varer**, i feltet **Kategorihierarki**, velger du en kategori på øverste nivå.
1. Varehierarkiet åpnes i den venstre ruten. Velg hierarkinivået du vil se etter. 
1. Varer fra det valgte hierarkiet og hierarkinivået vises nå i høyre rute. Følg denne fremgangsmåten for å arbeide med ruten:

    - Merk av i avmerkingsboksen for hver vare du vil legge til.
    - Merk av i avmerkingsboksen på rutenetthodet for å velge alle varene som vises på listen.
    - Velg **Vis valgt**-knappen for å filtrere rutenettet slik at den bare viser varene du har valgt så langt. Velg knappen på nytt for å gå tilbake til den fullstendige listen.

1. Velg **OK** for å bruke varevalget på den valgte gruppen.
