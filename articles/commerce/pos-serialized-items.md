---
title: Arbeide med serialiserte varer på salgsstedet
description: Denne artikkelen forklarer hvordan du administrerer serialiserte varer i salgsstedsprogrammet.
author: boycezhu
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 8a715a9d025f36656506daeb9e611bfacdafa102
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880035"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Arbeide med serialiserte varer på salgsstedet

[!include [banner](includes/banner.md)]

Mange forhandlere selger produkter som krever en seriell kontroll. Disse produktene blir referert til som *serialiserte varer*. Noen forhandlere vil kanskje vedlikeholde serienumre i butikk- eller lagerbeholdningen til sporingsformål. Andre forhandlere kan ønske å registrere serienumre under salgsprosessen for service- og garantiformål. Denne artikkelen forklarer hvordan du administrerer serialiserte varer i salgsstedsprogrammet for Microsoft Dynamics 365 Commerce.

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

## <a name="sell-serialized-items-in-pos"></a>Selge serialiserte varer på salgssted

Salgsstedsprogrammet har alltid støttet salg av serialiserte varer, men i Commerce versjon 10.0.17 og senere kan organisasjoner aktivere funksjonalitet som forbedrer forretningslogikken som utløses ved salg av produkter som er konfigurert for serienummersporing.

Når funksjonen for **Utvidet serienummervalidering i ordrehenting og ordreoppfyllelse for salgssted er aktivert**, evalueres følgende produktkonfigurasjoner når du selger serialiserte produkter på salgsstedet:

- Oppsett av **Serietype** for produktet (**aktiv** eller **aktiv i salg**).
- **Tom avgang tillatte**-innstillinger for produktet.
- **Fysisk negativt lager**-innstillinger for produktet og/eller salgslageret.

### <a name="active-serial-configurations"></a>Aktive konfigurasjoner av serienumre

Når varer selges på salgsstedet som er konfigurert med en **Aktiv** serienummersporingsdimensjon, starter salgsstedet valideringslogikk som hindrer brukere i å fullføre salget av en serialisert vare med et serienummer som ikke finnes i salgslagerets gjeldende lager. Det finnes to unntak fra denne valideringsregelen:

- Hvis varen også er konfigurert med **Tom avgang** aktivert, kan brukere hoppe over registreringen av serienummeret og selge varen uten serienummerbetegnelse.
- Hvis varen og/eller salgslageret er konfigurert med **Fysisk negativt lager** aktivert, godtar og selger programmet et serienummer som ikke kan bekreftes å være på lageret det selges mot. Ved hjelp av denne konfigurasjonen kan lagertransaksjonen for dette bestemte vare-/serienummeret være negativt, og systemet vil derfor tillate salg av ukjente serienumre.

> [!IMPORTANT]
> For å sikre at salgsstedsprogrammet kan validere riktig om serienumrene som selges for **Aktiv**-serietypevarer, er på salgslagerets lager, er det nødvendig at organisasjoner kjører jobben **Produkttilgjengelighet med sporingsdimensjoner** i Commerce Headquarters og den tilhørende distribusjonsjobben for produkttilgjengelighet, **1130**, via Commerce Headquarters hyppig. Ettersom nytt serialisert lager mottas til salgslagre, må lagerstandarden ofte oppdatere kanaldatabasen med de mest oppdaterte lagertilgjengelighetsdataene for at salgsstedet skal kunne validere tilgjengelighet for lagernumre som selges. Jobben **Produkttilgjengelighet med sporingsdimensjoner** tar et øyeblikksbilde av hovedlageret, inkludert serienumre, for alle firmalagre. Distribusjonsjobben **1130** tar et øyeblikksbilde av lageret og deler det med alle konfigurerte kanaldatabaser.

### <a name="active-in-sales-process-serial-configurations"></a>Aktiv i salgsprosess-seriekonfigurasjoner

Varer som er konfigurert med seriedimensjonen **Aktiv i salgsprosess**, går ikke gjennom noen lagervalideringslogikk, fordi denne konfigurasjonen innebærer at lagerserienumrene ikke er forhåndsregistrert på lager, og serienumrene registreres bare på salgstidspunktet.  

Hvis **Tom avgang tillatt** også er konfigurert for **Aktiv i salgsprosess**-konfigurerte varer, kan serienummeroppføringen hoppes over. Hvis **Tom avgang tillatt** ikke er konfigurert, krever programmet at brukeren angir et serienummer, selv om det ikke vil bli validert mot tilgjengelig lager.

### <a name="apply-serial-numbers-during-creation-of-pos-transactions"></a>Bruke serienumre under oppretting av POS-transaksjoner

Salgsstedsprogrammet ber brukere om henting av serienummer umiddelbart ved salg av en serialisert vare, men programmet gir brukerne muligheten til å hoppe over registreringen av serienumre opptil et bestemt tidspunkt i salgsprosessen. Når brukeren begynner å registrere betaling, iverksetter programmet og krever serienummer for varer som ikke er konfigurert til å oppfylles gjennom fremtidige forsendelser eller plukkinger. Serialiserte varer som er konfigurert for hentesalg eller utlevering, krever at brukeren registrerer serienummeret (eller godtar å la det stå tomt hvis varekonfigurasjonen tillater det) før salget fullføres.

Når det gjelder serialiserte varer som er solgt for fremtidig plukking eller forsendelse, kan salgsstedsbrukere hoppe over å angi serienummeret i utgangspunktet, og likevel fullføre opprettelsen av kundeordren.   

> [!NOTE]
> Når du selger eller oppfyller serialiserte produkter via salgsstedsprogrammet, fremtvinges antallet "1" for de serialiserte varene på salgstransaksjonen. Dette er et resultat av hvordan serienummerinformasjonen spores på salgslinjen. Ved salg eller fullføring av en transaksjon for flere serialiserte varer via salgsstedet, må hver salgslinje bare konfigureres med antallet "1". 

### <a name="apply-serial-numbers-during-customer-order-fulfillment-or-pickup"></a>Bruke serienumre under innfrielse eller plukking av kundeordre

Når du oppfyller kundeordrelinjer for serialiserte produkter ved hjelp av operasjonen **Ordreoppfyllelse** på salgsstedet, iverksetter POS registrering av serienummeret før endelig innfrielse. Hvis et serienummer ikke er angitt under den innledende ordrefangsten, må det registreres under plukk-, pakke- eller forsendelsesprosessen på salgsstedet. En validering utføres på hvert trinn, og brukeren vil bare bli bedt om serienummerdata hvis den mangler eller ikke lenger er gyldig. Hvis for eksempel en bruker hopper over plukk- eller pakketrinnene og øyeblikkelig starter en forsendelse, og det ikke er registrert et serienummer for linjen, vil salgsstedet kreve at serienummeret angis før det endelige fakturatrinnet er fullført. Når du utfører registrering av serienummeret under innfrielsesoperasjoner for ordre på salgsstedet, gjelder alle reglene som er nevnt tidligere i denne artikkelen, fremdeles. Bare serialiserte varer konfigurert som **Aktiv**, går gjennom en beholdningsvalidering for serienummer. Varer som er konfigurert som **Aktiv i salgsprosess**, blir ikke validert. Hvis **Fysisk negativt lager** er tillatt for **Aktive** produkter, blir et hvilket som helst serienummer godtatt, uavhengig av lagertilgjengelighet. Hvis **Tom avgang tillatt** er konfigurert, kan en bruker la serienumrene stå tomme hvis det er ønskelig under plukk-, pakke- og forsendelsestrinnene for både **Aktiv**- og **Aktiv i salgsprosess**-varer.

Valideringer for serienumre skjer også når en bruker utfører plukkoperasjonene på kundeordrer på salgsstedet. Salgsstedsprogrammet tillater ikke at plukkinger fullføres på et serialisert produkt med mindre det overfører valideringene som nevnt tidligere. Valideringene er alltid basert på produktets sporingsdimensjon og salgslagerkonfigurasjoner. 

## <a name="additional-resources"></a>Tilleggsressurser

[Inngående lageroperasjon i salgsstedet](./pos-inbound-inventory-operation.md)

[Utgående lageroperasjon i salgsstedet](./pos-outbound-inventory-operation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]