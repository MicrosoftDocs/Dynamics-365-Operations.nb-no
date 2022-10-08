---
title: Kjøre egendefinerte X++-skript med null nedetid
description: Denne artikkelen beskriver hvordan du laster opp og kjører distribuerbare pakker som inneholder egendefinerte X++-skript, uten at du trenger å stenge ute systemet.
author: AndersGirke
ms.date: 12/16/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-12-16
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 3d00f842da69f889738fbcb293c7489bb018e810
ms.sourcegitcommit: f62c9b24c2205d03e2fd6e7c67f7b5c316233b12
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2022
ms.locfileid: "9598089"
---
# <a name="run-custom-x-scripts-with-zero-downtime"></a>Kjøre egendefinerte X++-skript med null nedetid

[!include [banner](../includes/banner.md)]

Ved hjelp av denne funksjonen kan du laste opp og kjøre distribuerbare pakker som inneholder egendefinerte X++-skript, uten å måtte gå gjennom Microsoft Dynamics Lifecycle Services (LCS) eller stenge ute systemet. Du kan derfor korrigere mindre datainkonsekvenser uten å forårsake forstyrrende nedetid.

Fordelen med å bruke et X++-skript til å korrigere mindre datainkonsekvenser er at systemet automatisk justerer alle relaterte tabeller etter behov når det kjører skriptet. Denne fremgangsmåten sikrer integriteten for korrigeringen, og bidrar til å redusere risikoen for å innføre nye inkonsekvenser.

> [!IMPORTANT]
> Denne funksjonen er bare beregnet på korrigering av mindre datainkonsekvenser. Den må ikke brukes til følgende formål eller andre formål:
>
> - Datainnsamling
> - Skjemaendringer
> - Dataoverføring eller andre langsiktige prosesser
> - Korrigering av data som kan korrigeres på andre måter, for eksempel vanlige forretningsprosesser, verktøy for datakonsistens eller andre selvbetjeningsverktøy
>
> Ved hjelp av funksjonen kan autoriserte brukere endre enheter og deres poster direkte, uten at de trenger å kjøre forretningslogikken som er knyttet til disse enhetene. Disse endringene kan forårsake problemer med dataintegriteten. Derfor kan organisasjonen kreve at du innhenter godkjenning fra interne og eksterne revisorer (eller andre tilsvarende interessenter), før og/eller etter at du har kjørt et skript. Av samsvarsårsaker kan det hende at endringer som påvirker enkelte egenskaper, også må offentliggjøres i eksterne rapporter (for eksempel regnskapsoppgjør) eller rapporteres til myndighetene. Organisasjonen din er eneansvarlig for alle endringer som blir gjort i dataene via denne funksjonen, enhver godkjenning eller offentliggjøring av disse endringene, og samsvar med gjeldende lover. Du bærer all risikoen ved å bruke denne funksjonen.

Alle distribuerbare pakker som lastes opp til systemet, går gjennom en obligatorisk arbeidsflyt. Som et sikkerhetstiltak, og for å sikre arbeidsdeling, kan ikke brukeren som laster opp en distribuerbar pakke, godkjenne den for de neste trinnene i arbeidsflyten. En annen bruker må godkjenne den. Etter at pakken er godkjent, kan imidlertid brukeren som lastet den opp, fullføre de gjenværende trinnene.

Systemet krever at alle distribuerbare pakker går gjennom en testkjøring. Før skriptet får tillatelse til å kjøre på produksjonsdata, må en bruker validere at utdataene er korrekte, ved å velge **Godta testlogg**. Hvis utdataene ikke er korrekte, må brukeren merke pakken som mislykket ved å velge **Forlat**. I så fall har ikke skriptet tillatelse til å kjøre på produksjonsdata.

Hver pakke som lastes opp, lagres i systemet og går gjennom en definert hendelsesarbeidsflyt. For hver hendelse beholder systemet en logg som inkluderer et tidsstempel og identiteten til personen som utførte hendelsen. På denne måten sikrer systemet at det finnes et revisjonsspor.

Som illustrasjonen nedenfor viser, gir systemet detaljer om hvordan hver distribusjonsbare pakke ble kjørt i X++, og hvilke enheter som ble berørt.

![Skriptdetaljer-siden](media/script-details.png "Skriptdetaljer-siden")

## <a name="assign-duties-to-users-to-control-access"></a>Tilordne plikter til brukere for å kontrollere tilgang

Denne funksjonalitet inneholder følgende plikter: Administratorer kan bruke disse pliktene som hjelp til å kontrollere tilgangen til funksjonen.

- **Vedlikehold egendefinerte skript** – Denne plikten gir mulighet til å laste opp, teste, kontrollere og kjøre egendefinerte X++-skript i miljøer (brukergodkjenningstesting \[UAT\] og produksjon).
- **Godkjenn egendefinerte skript** – Denne plikten gir muligheten til å godkjenne et egendefinert X++-skript som er lastet opp. Godkjenning er et obligatorisk trinn før et hvilket som helst skript kan testes, kontrolleres og kjøres.

For å redusere faren for ondsinnede handlinger må hvert skript godkjennes av en annen bruker enn brukeren som lastet det opp. Før du kan bruke denne funksjonen i organisasjonen, må en administrator tilordne de foregående pliktene til minst to relevante og meget pålitelige brukere. Selv om én enkelt bruker kan ha begge pliktene, kan ikke denne brukeren godkjenne sine egne skript.

## <a name="create-a-deployable-package"></a>Opprette en distribuerbar pakke

Funksjonen krever en vanlig, distribuerbar pakke som kan opprettes i Visual Studio. Hvis du vil ha mer instruksjoner, kan du se [Opprette distribuerbare pakker av modeller](../deployment/create-apply-deployable-package.md).

Den distribuerbare pakken må inneholde nøyaktig én kjørbar X++-klasse. Det må med andre ord ha én klasse som inneholder en metode som har følgende signatur.

```xpp
public static void main(Args _args)
```

> [!NOTE]
> Navnet på hovedmetoden må være i små bokstaver.

## <a name="code-example"></a>Kodeeksempel

Følgende kodeeksempel viser hvordan en distribuerbar pakke kan struktureres.

```xpp
class MyScriptClassForIssueXYZ
{
    public static void main(Args _args)
    {
        if (curExt() != 'DAT')
        {
            throw error("This script must run in the DAT company!");
        }

        ttsbegin;

        MyTable myTable;

        update_recordset myTable
            setting myField = 17
            where myTable.myReference == 'xyz';

        if (myTable.RowCount() != 1)
        {
            throw error("Not updating the expected row!");
        }

        info("Success");
  
        ttscommit;
    }

}
```

## <a name="best-practices"></a>Anbefalte fremgangsmåter

Listen nedenfor beskriver anbefalte fremgangsmåter for riktig skriving, implementering og kjøring av et skript. Listeoversikten er ikke fullstendig, og den bør bare vurderes som veiledning.

- **Skriv** en suksessmelding på slutten av skriptet. På denne måten kan du se at skriptet ble kjørt uten unntak.
- **Legg til** eksplisitt behandling av transaksjonsområdet.
- **Bruk** eksisterende forretningslogikk, for eksempel `update()`-metoder, men **ikke** omgå forretningslogikk ved å burke metodene `doUpdate()`, `doInsert()` og `doDelete()`. Denne fremgangsmåten vil hjelpe deg med å sikre at avhengige data håndteres på riktig måte. Det vil også redusere risikoen for ytterligere datainkonsekvenser betydelig.
- **Forfekt** firmakonteksten. Denne fremgangsmåten viser vanlige feil når et skript kjøres. Den vil for eksempel vises om skriptet kjøres i feil firma.
- **Forfekt** at antallet påvirkede poster stemmer overens med forventningene. Denne fremgangsmåten vil finne ut om data uventet ble forskjøvet i systemet mens skriptet ble klargjort.
- **Bruk** unike klassenavn for hvert skript (for eksempel ved å ta med en referanse til et arbeidselement i navnet). Denne fremgangsmåten forhindrer problemer med likr navn når du laster opp skriptet. Hvis det kreves en ny repetisjon for et skript, må du gi det et nytt navn.
- **Test** hvert skript i et ikke-produksjonsmiljø først. Test for den tiltenkte innvirkningen og for utilsiktede sideeffekter på relaterte data. Sørg for at alle forretningsprosesser som kan påvirkes, kan fullføres fullstendig og på riktig måte etterpå.

## <a name="upload-and-run-a-deployable-package"></a>Laste opp og kjøre en distribuerbar pakke

Bruk fremgangsmåten nedenfor til å laste opp og kjøre et skript.

1. I økonomi- og driftsappen går du til **Systemadministrasjon \> Periodiske oppgaver \> Database \> Egendefinerte skript**.
1. Velg **Last opp**.
1. Velg den distribuerbare pakken du opprettet, som beskrevet tidligere i denne artikkelen. Du blir bedt om å angi formålet med skriptet.
1. Skriptet må nå godkjennes av en annen bruker enn brukeren som lastet det opp. Godkjenneren må følge disse trinnene:

    1. Gå til **Systemadministrasjon \> Periodisk \> Database \> Egendefinerte skript**.
    1. Velg skriptet som skal godkjennes, og velg deretter **Detaljer**.
    1. I handlingsruten, på fanen **Prosessarbeidsflyt**, i **Start**-gruppen, velger du **Godkjenn** eller **Avvis**. Hvis du velger **Godkjenn**, merkes skriptet som godkjent og låses opp for testing. Hvis du velger **Avvis**, er skriptet låst. I begge tilfeller blir hendelsen logget, og en kopi av skriptet beholdes i systemet.

1. Skriptet må testes for å sikre at det gjør det som det er ment å gjøre. Testeren kan være den samme som personen som lastet opp eller godkjente skriptet, eller en tredje bruker som har de nødvendige tillatelsene. Testeren må følge disse trinnene:

    1. Gå til **Systemadministrasjon \> Periodisk \> Database \> Egendefinerte skript**.
    1. Velg skriptet som skal testes, og velg deretter **Detaljer**.
    1. I handlingsruten, på fanen **Produksjonsarbeidsflyt**, i **Test**-gruppen, velger du **Kjør test**. Skriptet kjøres i en midlertidig transaksjon som systemet automatisk vil avbryte mens det samler inn forskjellige logger og SQL-setninger.
    1. Når skriptet er ferdig med å kjøre, kan du se gjennom loggene og kontrollere at resultatene oppfyller forventningene. Følg ett av disse trinnene:

        - Hvis du er fornøyd med testresultatet, velger du **Godta testlogg** i **Test**-gruppen på fanen **Prosessarbeidsflyt** i handlingsruten for å tillate at skriptet kan kjøres. Hendelsesloggen gjenspeiler at skriptet ble testet, og den vil vise hvem som testet det og når.
        - Hvis du ikke er fornøyd med testresultatet, velger du **Forlat** i **Avslutt**-gruppen på fanen **Prosessarbeidsflyt** i handlingsruten for å hindre at skriptet kan kjøres. Systemet beholder en kopi av skriptet sammen med en logg over historikken.

1. Når du er sikker på at skriptet oppfyller forventningene, velger du **Kjør** i **Kjør**-gruppen på fanen **Prosessarbeidsflyt** i handlingsruten for å kjøre det. Denne kommandoen gjør det samme som den forrige testkjøringen, men transaksjonen vil bli igangsatt på slutten.
1. Når skriptet er ferdig med kjøringen, kontrollerer du resultatet og bekrefter at skriptet fungerte som tiltenkt. Følg ett av disse trinnene:

    - Hvis du er fornøyd med resultatet, velger du **Formål løst** i **Avslutt**-gruppen på fanen **Prosessarbeidsflyt** i handlingsruten. Hendelsesloggen gjenspeiler at skriptet ble vellykket kjørt, og den vil vise hvem som verifiserte skriptet og når. Skriptet lagres, men det er nå låst og kan ikke kjøres på nytt.
    - Hvis du ikke er fornøyd med resultatet, velger du **Formål uløst** i **Avslutt**-gruppen på fanen **Prosessarbeidsflyt** i handlingsruten. Hendelsesloggen gjenspeiler at skriptet ikke kunne oppfylle sitt tiltenkte formål, og den vil vise hvem som kjørte skriptet og når. Skriptet lagres, men det er nå låst og kan ikke kjøres på nytt. Systemet angrer imidlertid ikke skripthandlingen automatisk. Det kan hende at du må skrive, importere og kjøre et nytt skript for å angre effekten det mislykkede skriptet hadde på systemet.

Valget ditt i det siste trinnet definerer den endelige statusen for skriptet. Du kan gjenta prosessen etter behov.

## <a name="upload-and-run-a-deployable-package-through-lcs"></a>Laste opp og kjøre en distribuerbar pakke via LCS

I stedet for å distribuere den distribuerbare pakken gjennom brukergrensesnittet for økonomi- og driftsappen, som beskrevet i forrige del, kan du laste den opp til LCS og bruke den vanlige fremgangsmåten for å distribuere den. Hvis du vil ha mer informasjon, kan du se [Installere distribuerbare pakker fra kommandolinjen](../deployment/install-deployable-package.md).

Selv om denne fremgangsmåten har færre begrensninger, gir den mindre feilbeskyttelse. Dessuten vil den føre til litt nedetid fordi den krever en omstart av alle serverne.

