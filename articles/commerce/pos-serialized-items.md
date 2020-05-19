---
title: Arbeide med serialiserte varer på salgsstedet
description: Dette emnet forklarer hvordan du administrerer serialiserte varer i salgsstedsprogrammet.
author: boycezhu
manager: annbe
ms.date: 04/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 1e0d6aa7cd5576578378e70c6ee808833314aff3
ms.sourcegitcommit: 919620b4aca425e6a1248ee12f50a622d2531e58
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2020
ms.locfileid: "3290776"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Arbeide med serialiserte varer på salgsstedet

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Mange forhandlere selger produkter som krever en seriell kontroll. Disse varene blir referert til som *serialiserte varer*. Noen forhandlere vil kanskje vedlikeholde serienumre til sporingsformål. Andre forhandlere kan ønske å registrere serienumre under salgsprosessen for service- og garantiformål. Dette emnet forklarer hvordan du administrerer serialiserte varer i Microsoft Dynamics 365 Commerce-salgsstedsprogrammet.

## <a name="serial-number-configurations"></a>Konfigurasjoner av serienumre

En vare anses som en serialisert vare hvis det er tilordnet en sporingsdimensjonsgruppe som er definert til å tillate serienumre. I Commerce-hovedkvarter, på siden **Sporingsdimensjonsgrupper**, velger du alternativet **Aktiv** for å aktivere serienubre for lagerprosess. Hvis du vil aktivere serienumre for salgsprosessen, velger du alternativet **Aktiv i salgsprosess**.

Hvis alternativet **Tom tilgang tillatt** er aktivert i hurtigfanen **Sporingsdimensjoner**, er serienummeret en valgfri inndata under lagermottaksprosessen. Hvis alternativet er deaktivert, er serienummeret nødvendig.

I hurtigkategorien **Serienumre**, hvis alternativet **Serienummerkontroll** er aktivert, må serienummeret være unikt per enhet. Det er med andre ord ikke tillatt med dupliserte serienumre.

## <a name="serialized-items-in-the-receiving-process"></a>Serialiserte varer i mottaksprosessen

Med operasjonen **Inngående lager** i POS-programmet kan brukere utføre følgende oppgaver for serialiserte varer:

- Registrere serienumre mot serialiserte varer når varene mottas i butikken via en bestilling.
- Validere forhåndsregistrerte serienumre mot serialiserte varer når varene mottas i butikken via en bestilling eller overføringsordre.

> [!NOTE]
> Hvis du vil bruke operasjonen **Inngående lager** til å registrere eller validere en serialisert vare, må varen tilordnes en sporingsdimensjonsgruppe som er satt til å tillate serienumre for alternativet **Aktiv**, ikke alternativet **Aktiv i salgsprosess**.

Når du skal starte mottaksprosessen i operasjonen **Inngående lager**, kan du starte visningen **Motta nå** ved å skanne varens strekkode eller angi vare-IDen. Du kan også starte i visningen **Fullstendig ordreliste** ved å velge varen manuelt.

Hvis varen som blir valgt eller mottatt, er en serialisert vare, inneholder **Detaljer**-ruten for varen en **Behandle serienummer**-koblingen som åpner siden for **administrasjon av serienumre**. Du kan også åpne siden for **administrasjon av serienumre** ved å velge **Serienummer** på applinjen i ordredetaljervisningen eller ved å velge **Behandle serienummer** i dialogboksen som spør deg under mottaksprosessen. Siden for **administrajon av serienummer** viser alle åpne serienummerlinjer som venter på registrering eller validering. Det kan være to kategorier på denne siden: én for den gjeldende varen og én for alle de serialiserte varene i ordren.

**Status**-feltet på siden for **administrasjon av serienummer** inneholder informasjon om gjeldende stadium som hvert serienummer er i:

- **Ikke registrert** – Serienummeret er ikke oppgitt, eller det forhåndsregistrerte serienummeret er ennå ikke validert.
- **Registrering** – Serienummeret er registrert og lagret lokalt i butikkens kanaldatabase, eller det forhåndsregistrerte serienummeret har blitt validert. Bare serienumre som har statusen **Registrering**, sendes til Commerce-hovedkvarteret når du er ferdig med å motta.

### <a name="register-serial-numbers-against-serialized-items"></a>Registrere serienumre mot serialiserte varer

For en bestilling er det en dialogboks under mottaksprosessen der du blir bedt om å oppgi et serialisert varetilbud, som tilbyr alternativet **Behandle serienummer**. Du kan velge dette alternativet for å åpne siden for **administrasjon av serienumre** og begynne å registrere serienumre. Du kan også hoppe over dette trinnet under mottaksprosessen og angi inndataene senere, før mottaket posteres.

Kategorien for gjeldende vare vises som standard. Alle serienummerlinjer har en tom serienummerverdi og statusen **Ikke registrert**. Du kan skanne strekkoder for serienumre, eller du kan velge **Serienummer** på applinjen for å kontinuerlig angi serienumre i dialogboksen. Serienumrene du angir, vises i listen, og statusen for serienummerlinjene endres til **Registrering**. Det maksimale antallet serienumre du kan registrere i listen, er lik det mottakende antallet. Hvis du gjør ein feil, kan du velge **Rediger** eller **Slett** i ruten **Detaljer** for å gjøre endringer i serienumrene du skrev inn.

Du kan også registrere serienumre i kategorien **Alle serialiserte varer** på siden for **administrasjon av serienumre**. Velg varen du ønsker å registrere serienumre mot, i listen.

Under serienummerregistrering på denne siden oppstår duplisering av validering. Hvis du prøver å angi et duplisert serienummer mot en vare som serienummerkontrollen er slått på for, får du en feilmelding, og må oppgi et annet nummer.

### <a name="validate-serial-numbers-on-serialized-items"></a>Validere serienumre på serialiserte varer

For en overføringsordre må den utgående siden forhåndsregistrere serienumre på de serialiserte varene i løpet av forsendelsesprosessen. For en bestilling kan leverandøren levere serienummerinformasjon gjennom en forhåndsvarsel for forsendelse, og du kan forhåndsregistrere numrene på varene som skal leveres. I begge tilfeller er serienumrene kjent før mottaket. På den innkommende siden trenger du derfor bare bekrefte at du har mottatt det du skulle motta.

Hvis du vil validere serienumre, kan du åpne siden **administrajon av serienummer** under mottaksprosessen, eller når som helst før mottaket posteres. For hver serialiserte vare som har forhåndsregistrerte serienumre, settes alle serienumrene automatisk til den innledende statusen **Ikke registrert** på denne siden. For å validere serienumre kan du skanne eller angi dem. Etter hvert som serienummeret angis, validerer programmet om de samsvarer med forhåndsregistrerede serienumre. Hvis de samsvarer, endres statusen til **Registrering**. Hvis ikke får du en feilmelding. Det maksimale antallet serienumre du kan validere i listen, er lik det mottakende antallet.

Du kan også validere serienumre i kategorien **Alle serialiserte varer** på siden for **administrasjon av serienumre**. Velg varen du ønsker å validere serienumre mot, i listen.

## <a name="additional-resources"></a>Tilleggsressurser

[Inngående lageroperasjon i salgsstedet](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)
