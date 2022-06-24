---
title: Opprette returer i POS
description: Denne artikkelen beskriver hvordan du starter returer for hentesalgstransaksjoner eller kundeordrer i Microsoft Dynamics 365 Commerce Point of Sale (POS).
author: hhainesms
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.20
ms.openlocfilehash: a49e9abd0143d480cc1cafb05be5e995fb3cebdd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857004"
---
# <a name="create-returns-in-pos"></a>Opprette returer i POS

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du starter returer for hentesalgstransaksjoner eller kundeordrer i appen Microsoft Dynamics 365 Commerce Point of Sale (POS).

> [!NOTE]
> Det er en ny funksjon kalt **Enhetlig returbehandling i POS** tilgjengelig i Commerce versjon 10.0.20 og nyere. Denne funksjonen gir en mer konsekvent og enhetlig returprosess i POS, uavhengig av transaksjonstypen (hentesalgstransaksjon eller kundeordre) eller den opprinnelige kanalen ordren ble opprettet i. Vi anbefaler at alle organisasjoner aktiverer denne nye funksjonen for å forbedre den helhetlige påliteligheten til returbehandling via POS.
>
> Når funksjonen er aktivert, kan den ikke deaktiveres.

## <a name="process-returns-by-using-the-return-transaction-operation"></a>Behandle returer ved hjelp av returtransaksjonsoperasjonen

Vi anbefaler at du legger til returtransaksjonsoperasjonen i [skjermoppsettet](pos-screen-layouts.md) i POS. I versjoner før utgivelsen av Commerce versjon 10.0.20 støtter returtransaksjonsoperasjonen bare behandling av returer for hentesalgstransaksjoner på riktig måte. Etter at du har aktivert funksjonen **Enhetlig returbehandling i POS** i utgivelsen av Commerce versjon 10.0.20 eller nyere, støtter også returtransaksjonsoperasjonen behandling av returer som stammer fra kundeordrer, for eksempel ordrer for henting eller hjemlevering som allerede er fakturert.

Fra returtransaksjonsoperasjonen kan brukere søke etter en hentesalgstransaksjon eller kundeordre de kan returnere mot, ved å angi et av følgende fire søkekriterier. Brukere kan angi disse kriteriene ved hjelp av et enhetstastatur, skjermtastatur eller en strekkodeskanner.

- Mottaks-ID
- Ordrenummer
- Kanalreferanse-ID (også kalt ordrebekreftelses-ID)
- Faktura-ID

Hvis det blir funnet en transaksjon eller ordre som samsvarer med søkekriteriene, vises siden **Produkter som kan returneres**. Der kan brukere angi varene som returneres. De kan også angi returantall og årsakskoder.

For hver ordrelinje i listen over produkter som kan returneres, viser POS informasjon om det opprinnelige bestillingsantallet og antallet fra alle returer som er behandlet tidligere. Returantallet som en bruker angir for en ordrelinje, må være mindre enn eller lik verdien i feltet **Tilgjengelig for retur**.

![Siden Produkter som kan returneres.](media/returnslist.png)

Hvis en bruker har det fysiske produktet under returbehandling og produktet har en strekkode, kan brukeren skanne strekkoden for å registrere returen. Hver skanning av strekkoden øker returantallet med én vare. Hvis strekkodeetiketten imidlertid har et innebygd antall, angis dette antallet i **Returnerer nå**-feltet.

Brukere kan også velge varer manuelt på siden **Produkter som kan returneres** og deretter oppdatere **Returnerer nå**-feltet ved hjelp av detaljruten til høyre.

Hvis det største tilgjengelige **Returnerer nå**-antallet angis for en transaksjon, kan brukeren velge **Velg alle**-operasjonen på POS-applinjen for å angi maksimalt antall som kan returneres på alle linjer.

For hver linje som har et **Returnerer nå**-antall, må brukeren velge en returårsakskode ved hjelp av detaljpanelet. Når det gjelder returer av hentesalgstransaksjoner, konfigureres returårsakskodene som informasjonskoder i butikkens funksjonalitetsprofil. Når det gjelder returer av kundeordrer, konfigureres returårsakskodene på siden **Koder for returårsaker** i Dynamics 365 Commerce Headquarters.

Etter at returantallet og årsakskoden er angitt for hver vare som skal returneres, kan brukeren velge **Retur**-operasjonen på POS-applinjen for å fortsette med behandlingen. Siden for POS-transaksjon vises, der varene som kan returneres og ble valgt på forrige side, er lagt til i handlekurven. **Returnerer nå**-antallene for varene vises som negative antallslinjer på transaksjonen, og den totale refunderingen beregnes.

Brukere kan legge til linjer i en returtransaksjon hvis de oppretter en bytteordre. Brukere kan også legge til flere adhocreturvarer i en returtransaksjon ved å bruke **Returprodukt**-operasjonen for en valgt salgslinje med positivt antall som er lagt til.

> [!NOTE]
> **Returprodukt**-operasjonen i POS gir ingen validering mot noen opprinnelige transaksjoner, og lar ethvert produkt returneres. Vi anbefaler derfor at bare autoriserte brukere får tillatelse til å utføre denne operasjonen, eller at en lederoverstyring kreves hvis denne operasjonen skal brukes.

Hvis en refundering forfaller ved kassen, kan organisasjoner konfigurere [betalingspolicyer for refundering](refund_policy_returns.md) som begrenser betalingsmåtene som kan brukes til å refundere kunder. Hvis den opprinnelige transaksjonen ble betalt med et kredittkort, avhengig av betalingsprosessoren og systemkonfigurasjonen, kan brukerne få muligheten til å [utstede en refundering til det opprinnelige kortet](dev-itpro/linked-refunds.md). I dette tilfellet kan refunderingen behandles uten at kunden må bruke kredittkortet på nytt. Det opprinnelige betalingstokenet brukes til å utstede refusjonen.

## <a name="other-return-options-in-pos"></a>Andre returalternativer i POS

Når funksjonen **Enhetlig returbehandling i POS** er aktivert, kan brukere også bruke **Vis journal**-operasjonen i POS til å starte en retur for en hentesalgstransaksjon eller kundeordre. De kan deretter velge en transaksjon i journalen og velge **Retur**-operasjonen på POS-applinjen. Denne operasjonen er bare tilgjengelig hvis det finnes linjer som kan returneres, i ordren. Den starter den samme brukeropplevelsen som **Returtransaksjon**-operasjonen.

Brukere kan også bruke operasjonen **Tilbakekall ordre** i POS til å søke etter og tilbakekalle kundeordrer. (Denne operasjonen kan ikke brukes for hentesalgstransaksjoner). Etter at en kundeordre er valgt i dette tilfellet, kan **Retur**-operasjonen på POS-applinjen brukes til å starte en retur for kundeordren. Denne operasjonen er bare tilgjengelig hvis det finnes linjer som kan returneres, i ordren. Den starter den samme brukeropplevelsen som operasjonen **Returtransaksjon** eller **Vis journal**.

## <a name="return-orders-are-posted-to-commerce-headquarters-as-sales-orders"></a>Returordrer posteres til Commerce Headquarters som salgsordrer 

Når funksjonen **Enhetlig returbehandling i POS** er aktivert, skrives alle returer som opprettes i POS, til Commerce Headquarters som salgsordrer med negative linjer. I utgivelser før Commerce versjon 10.0.20 kan brukere velge om returordrer skal posteres som salgsordrer med negative linjer, eller om de skal være returordrer som opprettes via autorisasjonsprosessen for retur av materiell (ARM). 

I funksjonen **Enhetlig returbehandling i POS** er alternativet for å bruke ARM-prosessen til å opprette returer i POS, avskrevet. Etter at denne funksjonen er aktivert, blir alle returer opprettet som salgsordrer med negative linjer.

## <a name="offline-return-processing-improvements"></a>Forbedringer i frakoblet behandling av returer

Når en retur behandles i POS, prøver systemet i de fleste tilfeller å foreta et serviceoppkall til Commerce Headquarters i sanntid for å validere gjeldende antall som er tilgjengelig for retur. Denne valideringen bidrar til å forhindre svindelscenarioer der en kunde prøver å returnere den samme varen flere steder.

For å håndtere situasjoner der serviceoppkall i sanntid ikke kan foretas på grunn av nettverks- eller tilkoblingsproblemer, er det utviklet en prosess som periodisk synkroniserer returantallsdata fra Commerce Headquarters med kanaldatabasen i en butikk. Denne retursporingen på kanalsiden bidrar til å sikre at antallene som er **Tilgjengelig for retur** og vises i POS, er rimelig nøyaktige, også når POS er frakoblet. Den sikrer også at POS kan fortsette å validere informasjonen på kanalsiden for å bidra til å forhindre falske returer.

For å kunne bruke den frakoblede returprosessen på riktig måte må organisasjoner planlegge den satsvise jobben **Oppdater returantall** i Commerce Headquarters slik at den kjøres ofte. Vi anbefaler at denne jobben kjøres med samme frekvens som P-jobben, som henter nye transaksjoner fra Commerce-kanaler til Commerce Headquarters.

Jobben **Oppdater returantall** beregner antallet som er tilgjengelig for retur for alle salgsordrer som finnes i Commerce Headquarters. Dataene som jobben beregner, må deretter sendes til kanaldatabaser, slik at butikkanalene kan oppdateres. Distribusjonsjobben **Returantall** (1200) brukes til dette formålet. Siden data om antallet som kan returneres, synkroniseres fra Commerce Headquarters hvis en retur behandles i POS, men serviceoppkallet i sanntid ikke kan utføres, kan POS bruke returinformasjonen på kanalsiden til å validere antallene som er **Tilgjengelig for retur** for en gitt salgslinje.

Når serviceoppkall i sanntid ikke kan utføres og POS bruker data på kanalsiden til returvalidering, får brukerne en advarsel om at de oppretter en «frakoblet» retur. De blir dermed klar over at antallet som er **Tilgjengelig for retur** og vises i POS, kan være foreldet og ikke lenger nøyaktig, avhengig av når jobben **Oppdater returantall** sist ble behandlet og synkronisert med kanalen.

La oss si at en kunde nylig behandlet en retur for en ordrelinje i en annen kanal, men at data ennå ikke er synkronisert med kanaldatabasene via jobben **Oppdater returantall**. Kunden går deretter til en annen butikk og prøver å returnere den samme varen på nytt. Hvis butikken i dette tilfellet ikke kan foreta et serviceoppkall i sanntid til Commerce Headquarters for å hente returdata i sanntid, tillater POS at varen returneres igjen. Brukeren blir imidlertid advart om at informasjonen som brukes til å validere returen, kan være foreldet. Meldingen som brukeren mottar, er bare en advarsel. Den forhindrer ikke brukeren fra å fortsette med behandling av returen.

Hvis informasjonen på kanalsiden av en eller annen årsak ikke er oppdatert og en frakoblet retur behandles for et antall som overskrider det faktiske antallet som er **Tilgjengelig for retur**, genereres kanskje en feil når utdragspostering kjøres for å opprette transaksjonen i Commerce Headquarters.

> [!NOTE]
> Når funksjonen **Enhetlig returbehandling i POS** er aktivert, blir nye valgfrie funksjoner som støtter validering av serialiserte produktreturer, tilgjengelige. Hvis du vil ha mer informasjon, kan du se [Returnere serienummerkontrollerte produkter i Point of Sale (POS)](POS-serial-returns.md).

## <a name="version-details"></a>Versjonsdetaljer

Listen nedenfor inneholder minimumskravene for versjon for de ulike komponentene.
- Commerce Headquarters: versjon 10.0.20
- Commerce Scale Unit (CSU): versjon 9.30
- Point of Sale (POS): versjon 9.30

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Aktiver riktig avgiftsberegning for returer med delvis antall

Denne funksjonen sikrer at når en ordre returneres ved hjelp av flere fakturaer, vil avgiften være lik avgiftsbeløpet som opprinnelig ble belastet.

1. I arbeidsområdet **Funksjonsbehandling** søker du etter **Aktiver riktig avgiftsberegning for returer med delvis antall**.
1. Velg funksjonen **Aktiver riktig avgiftsberegning for returer med delvis antall** og velg deretter **Aktiver**.

## <a name="set-up-return-locations-for-retail-stores"></a>Definere returlokasjoner for detaljhandelbutikker

I Commerce kan du konfigurere returlokasjoner som er basert på infokoder for detaljhandel og årsakskoder for salg og markedsføring. Når kunder returnerer kjøp, indikerer selgere ofte årsaken til returen. Du kan angi at returnerte varer skal tildeles til forskjellige returlokasjoner i lageret, basert på infokoder og årsakskoder som selgere velger ved salgsstedskassen.

En kunde returnerer for eksempel et defekt produkt, og selgeren behandler returtransaksjonen. Når Retail POS viser informasjonskoden for returer, velger selgeren delkoden for mangelfulle returer. Det returnerte produktet tildeles deretter automatisk til en bestemt returlokasjon.

En returlokasjon kan være en butikk, et lager, en lokasjon i et lager eller en bestemt pall, avhengig av hvilke lagerlokasjoner organisasjonen har definert. Du kan tildele hver returlokasjon til en eller flere handelsinformasjonskoder og salgs- og markedsføringsårsakskoder.

### <a name="prerequisites"></a>Forutsetninger

Før du kan definere returlokasjoner, må du definere følgende elementer:

- **Informasjonskoder for detaljhandel** – Spørsmål ved kassen på salgsstedet som er definert i **Retail**-modulen. Hvis du vil ha mer informasjon, kan du se [Konfigurer informasjonskoder](/dynamicsax-2012/appuser-itpro/setting-up-info-codes).
- **Årsakskoder for salg og markedsføring** – spørsmål ved salgsstedskassen som er definert i **Salg og markedsføring**-modulen. Hvis du vil ha mer informasjon, kan du se [Konfigurer årsakskoder](/dynamicsax-2012/appuser-itpro/set-up-return-reason-codes).
- **Lagerlokasjoner** – stedene der beholdningen lagres. Hvis du vil ha mer informasjon, kan du se [Konfigurer lagerlokasjoner](/dynamicsax-2012/appuser-itpro/about-locations).
    
### <a name="set-up-return-locations"></a>Definer returlokasjoner

Hvis du vil konfigurere returlokasjoner, gjør du følgende.

1. Gå til **Retail og Commerce \> Kanaloppsett \> Lagre** og velg et lager.
1. På hurtigfanen **Detaljhandel** i feltet **Standard returlokasjon** velger du lagerlokasjonen som skal brukes for returer der informasjonskoder eller årsakskoder ikke er tildelt til returlokasjoner.
1. I feltet **Standard returpall** velger du pallen som skal brukes for returer der informasjonskoder eller årsakskoder ikke er tildelt til returlokasjoner.
1. Gå til **Retail og Commerce \> Lagerstyring \> Returlokasjoner**.
1. Velg **Ny** for å opprette en returlokasjonspolicy.
1. Angi et unikt navn og en beskrivelse for returlokasjonen.

    > [!NOTE]
    > Hvis en nummerserie er definert for returlokasjoner, angis navnet automatisk.

1. I hurtigfanen **Generelt** angir du **Utskriftsetiketter** til **Ja** for å skrive ut etiketter for alle produktene som er tildelt returlokasjoner.
1. Angi alternativet **Blokker lager** til **Ja** for å ta de returnerte produktene på standard returlokasjon, ut fra lageret og hindre at de blir solgt.
1. Følg denne fremgangsmåten for å tildele bestemte delkoder til returlokasjoner;

    1. Velg **Legg til** på hurtigfanen **Informasjonskoder for detaljhandel**.
    1. Velg en informasjonskode for returer i **Informasjonskode**-feltet.
    1. I **Delkode**-feltet velger du en delkode for årsaken til returen. Feltet **Beskrivelse** viser beskrivelsen av den valgte delkoden.
    1. I **Butikk**-feltet velger du butikken der informasjonskoden brukes.
    1. Bruk feltene **Lager**, **Lokasjon** og **Pall-ID** til å angi en returlokasjon. Hvis du vil angi en bestemt lokasjon i en butikk, kan du for eksempel velge en butikk i **Butikk**-feltet og en lokasjon i **Lokasjon**-feltet.
    1. Merk av for **Blokker lager**-avmerkingsboksen for å ta returnerte varer ut av lageret og hindre at de blir solgt.

1. Følg denne fremgangsmåten for å tildele bestemte salgs- og markedsføringsårsakskoder til returlokasjoner;

    1. Velg **Legg til** i hurtigfanen **Årsakskoder for salg og markedsføring**.
    1. Velg en ny årsakskode for returer i feltet **Årsakskode**. Feltet **Beskrivelse** viser beskrivelsen av den valgte årsakskoden.
    1. I **Butikk**-feltet velger du butikken der årsakskoden brukes.
    1. Bruk feltene **Lager**, **Lokasjon** og **Pall-ID** til å angi en returlokasjon. Hvis du vil angi en bestemt pall på en lokasjon på et lager, kan du for eksempel velge et lager i **Lager**-feltet, en lokasjon i **Lokasjon**-feltet og en pall i **Pall**-feltet.
    1. Merk av for **Blokker lager**-avmerkingsboksen for å ta returnerte varer ut av lageret og hindre at de blir solgt.

    > [!NOTE]
    > Hvis det brukes en returlokasjonspolicy for en vare, men returårsaken som en kasserer velger, ikke samsvarer med kodene som er angitt i hurtigfanene **Informasjonskoder for detaljhandel** eller **Årsakskoder for salg og markedsføring**, sendes varen til standard returlokasjon som er definert på **Lager**-siden. I tillegg bestemmer innstillingen for **Blokker lager**-avmerkingsboksen på hurtigfanen **Generelt** på siden **Returlokasjoner** om den returnerte varen skal lagersperres.

1. Gå til **Retail og Commerce \> Handelsprodukthierarki**.
1. Velg en returlokasjon i feltet **Returlokasjon** i hurtigfanen **Behandle kategoriegenskaper for lager**. Fordi det kan defineres flere returlokasjonspolicyer for den samme butikken, bestemmer verdien du velger her, returlokasjonspolicyen som brukes.

## <a name="additional-resources"></a>Tilleggsressurser

[Returnere serienummerkontrollerte produkter i Point of Sale (POS)](POS-serial-returns.md)

[Koblede refunderinger av tidligere godkjente og bekreftede transaksjoner](dev-itpro/linked-refunds.md)

[Opprette og oppdatere en retur- og refunderingspolicy for en kanal](refund_policy_returns.md)

[Visuelle konfigurasjoner av brukergrensesnittet for salgssted](pos-screen-layouts.md)
