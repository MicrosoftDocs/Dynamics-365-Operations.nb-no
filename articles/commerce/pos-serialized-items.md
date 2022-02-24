---
title: Arbeide med serialiserte varer på salgsstedet
description: Dette emnet forklarer hvordan du administrerer serialiserte varer i salgsstedsprogrammet.
author: boycezhu
manager: annbe
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 6ba01abc3d1a4496ec586a621aa03b4981f84d76
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414757"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Arbeide med serialiserte varer på salgsstedet

[!include [banner](includes/banner.md)]

Mange forhandlere selger produkter som krever en seriell kontroll. Disse produktene blir referert til som *serialiserte varer*. Noen forhandlere vil kanskje vedlikeholde serienumre i butikk- eller lagerbeholdningen til sporingsformål. Andre forhandlere kan ønske å registrere serienumre under salgsprosessen for service- og garantiformål. Dette emnet forklarer hvordan du administrerer serialiserte varer i Microsoft Dynamics 365 Commerce-salgsstedsprogrammet.

## <a name="serial-number-configurations"></a>Konfigurasjoner av serienumre

En vare anses som en serialisert vare hvis det er tilordnet en sporingsdimensjonsgruppe som er definert til å tillate serienumre. I Commerce-hovedkvarteret velger du alternativet **Aktiv** på siden **Sporingsdimensjonsgrupper** for å aktivere serienumre for lagerprosessen, eller velger alternativet **Aktiv i salgsprosess** for å aktivere serienumre for salgsprosessen.

I hurtigkategorien **Sporingsdimensjoner** aktiverer du parameteren **Tom tilgang tillatt** for å tillate at serienumre kan være valgfrie inndata i løpet av lagermottaksprosessen for en serialisert vare. Hvis du deaktiverer denne parameteren, tvinges serienummeret til å være påkrevd inndata. På samme måte kan parameteren **Tom avgang tillatt** kontrollere om det kreves et serienummer under lagerforsendelsesprosessen.

> [!NOTE]
> Hvis du vil bruke salgsstedsoperasjonen **Inngående lager** og **Utgående lager** til å registrere eller validere serienumre mot en serialisert vare, må du konfigurere den varen til å bli tilordnet en sporingsdimensjonsgruppe som blir konfigurert til å tillate serienumre for alternativet **Aktiv**, ikke alternativet **Aktiv i salgsprosess**.

## <a name="serial-number-management-page"></a>Administrasjonsside for serienummer

I salgsstedsoperasjonene **Inngående lager** og **Utgående lager** inneholder ruten **Detaljer** alternativet **Behandle serienummer** hvis varen som blir valgt, mottatt eller sendt, er en serialisert vare. Alternativet har en kobling til siden **Administrasjon av serienumre** der du kan registrere eller validere serienumre for varen. Du kan også åpne siden for **Administrasjon av serienumre** ved å velge handlingen **Serienummer** på applinjen i ordredetaljervisningen, eller ved å velge alternativet **Behandle serienummer** i dialogboksen som spør deg under mottaks- eller sendeprosessen. 

Siden for **administrajon av serienummer** viser alle åpne serienummerlinjer som venter på registrering eller validering. Det kan være to kategorier på denne siden: én for den gjeldende varen og én for alle de serialiserte varene i ordren.

**Status**-feltet på siden for **administrasjon av serienummer** inneholder informasjon om gjeldende stadium som hvert serienummer er i:

- **Ikke registrert** – Serienummeret er ikke oppgitt, eller det forhåndsregistrerte serienummeret er ennå ikke validert (i mottaksprosessen).
- **Registrering** – Serienummeret er registrert og lagret lokalt i butikkens kanaldatabase, eller det forhåndsregistrerte serienummeret har blitt validert. Bare serienumre som har statusen **Registrering**, sendes til Commerce-hovedkvarteret når du er ferdig med å motta eller oppfylle.

## <a name="receive-serialized-items"></a>Motta serialiserte varer

Med salgsstedsoperasjonen **Inngående lager** kan brukere utføre følgende oppgaver for serialiserte varer:

- Registrere serienumre mot serialiserte varer når varene mottas i butikken via en bestilling.
- Validere forhåndsregistrerte serienumre mot serialiserte varer når varene mottas i butikken via en bestilling eller overføringsordre.

### <a name="register-serial-numbers-against-serialized-items"></a>Registrere serienumre mot serialiserte varer

For en bestilling blir det vist en dialogboks med alternativet **Behandle serienummer** i løpet av mottaksprosessen for en serialisert vare. Du kan velge dette alternativet for å åpne siden for **administrasjon av serienumre** og begynne å registrere serienumre. Du kan også hoppe over dette trinnet under mottaksprosessen og angi inndataene senere, før mottaket posteres.

Kategorien for gjeldende vare vises som standard. Alle serienummerlinjer har en tom serienummerverdi og statusen **Ikke registrert**. Du kan skanne strekkoder for serienumre, eller du kan velge **Serienummer** på applinjen for å kontinuerlig angi serienumre. Serienumrene du angir, vises i listen, og statusen deres endres til **Registrering**. Det maksimale antallet serienumre du kan registrere i listen, er lik det mottakende antallet. Hvis du gjør ein feil, kan du velge **Rediger** eller **Slett** i ruten **Detaljer** for å gjøre endringer i serienumrene du skrev inn.

Du kan også registrere serienumre i kategorien **Alle serialiserte varer** på siden for **administrasjon av serienumre**. Velg varen du ønsker å registrere serienumre mot, i listen.

### <a name="validate-serial-numbers-on-serialized-items"></a>Validere serienumre på serialiserte varer

For en overføringsordre må den utgående siden forhåndsregistrere serienumre på de serialiserte varene i løpet av forsendelsesprosessen. For en bestilling kan leverandøren levere serienummerinformasjon gjennom en forhåndsvarsel for forsendelse, og du kan forhåndsregistrere numrene på varene som skal leveres. I begge tilfeller er serienumrene kjent før mottaket. På den innkommende siden trenger du derfor bare bekrefte at du har mottatt det du skulle motta.

Hvis du vil validere serienumre, kan du åpne siden **administrajon av serienummer** under mottaksprosessen, eller når som helst før mottaket posteres. For hver serialiserte vare som har forhåndsregistrerte serienumre, settes alle serienumrene automatisk til den innledende statusen **Ikke registrert** på denne siden. For å validere serienumre kan du skanne eller angi dem. Etter hvert som serienummeret angis, validerer programmet om de samsvarer med forhåndsregistrerede serienumre. Hvis de samsvarer, endres statusen til **Registrering**. Hvis ikke får du en feilmelding. Alternativt kan du velge et serienummer direkte, og deretter velge alternativet **Valider serienummer** i ruten **Detaljer** for raskt å merke dette serienummeret som validert. Det maksimale antallet serienumre du kan validere i listen, er lik det mottakende antallet.

Du kan også validere serienumre i kategorien **Alle serialiserte varer** på siden for **administrasjon av serienumre**. Velg varen du ønsker å validere serienumre mot, i listen.

## <a name="ship-serialized-items"></a>Send serialiserte varer

Du kan bruke salgsstedsoperasjonen **Utgående lager** til å registrere serienumre mot serialiserte varer når du sender dem ut av gjeldende butikk via en overføringsordre.

### <a name="register-serial-numbers-against-serialized-items"></a>Registrere serienumre mot serialiserte varer

For en overføringsordre blir det vist en dialogboks med alternativet **Behandle serienummer** i løpet av forsendelsesprosessen for en serialisert vare. Du kan velge alternativet for å åpne siden for **administrasjon av serienumre** og begynne å registrere serienumre. Du kan også hoppe over dette trinnet under forsendelsesprosessen og angi inndataene senere, før forsendelsen posteres.

Kategorien for gjeldende vare vises som standard. Alle serienummerlinjer har en tom serienummerverdi og statusen **Ikke registrert**. Du kan skanne strekkoder for serienumre, eller du kan velge **Serienummer** på applinjen for å kontinuerlig angi serienumre. Serienumrene du angir, vises i listen, og statusen deres endres til **Registrering**. Det maksimale antallet serienumre du kan registrere i listen, er lik forsendelsesantallet. Hvis du gjør ein feil, kan du velge **Rediger** eller **Slett** i ruten **Detaljer** for å gjøre endringer i serienumrene du skrev inn.

Du kan også registrere serienumre i kategorien **Alle serialiserte varer** på siden for **Administrasjon av serienumre**. Velg varen du ønsker å registrere serienumre mot, i listen.

Du kan også aktivere validering av tilgjengelighet for serienummer under serienummerregistreringen mot en utgående overføringsordre. Hvis du prøver å sende et serienummer som ikke er tilgjengelig i beholdningen i forsendelsesbutikken, vil du få en feilmelding der du må oppgi et annet nummer.

Hvis du vil aktivere for eksempel validering som en forutsetning, må du planlegge at følgende jobber skal kjøre på regelmessig basis:

- **Detaljhandel og handel** > **IT for Detaljhandel og handel** > **Produkter og beholdning** > **Produkttilgjengelighet med sporingsdimensjoner**
- **Detaljhandel og handel** > **Distribusjonsplaner** > **1130** (**Produkttilgjengelighet**)

## <a name="additional-resources"></a>Tilleggsressurser

[Inngående lageroperasjon i salgsstedet](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)

[Utgående lageroperasjon i salgsstedet](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)
