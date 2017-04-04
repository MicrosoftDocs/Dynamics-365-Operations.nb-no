---
title: Elimineringsregler
description: Dette emnet inneholder informasjon om elimineringsregler og de ulike alternativene for rapportering om elimineringer.
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: db4b05bc55d735513d7580ca5908a1e84eb760c6
ms.openlocfilehash: 152b63fdfc78b3c4e79b93340d18c5cf69257024
ms.lasthandoff: 03/31/2017


---

# <a name="elimination-rules"></a>Elimineringsregler

Dette emnet inneholder informasjon om elimineringsregler og de ulike alternativene for rapportering om elimineringer.

Elimineringstransaksjoner er nødvendige når en overordnet juridisk enhet handler med én eller flere underordnede juridiske enheter og bruker konsolidert finansrapportering. Konsoliderte regnskapsoppgjør kan bare omfatte transaksjoner som forekommer mellom den konsoliderte organisasjonen og andre enheter utenfor denne organisasjonen. Derfor må transaksjoner mellom juridiske enheter som er en del av den samme organisasjonen fjernes, eller elimineres, fra økonomimodulen, slik at de ikke vises i økonomiske rapporter. Det finnes flere måter å rapportere om elimineringer på:

-   En elimineringsregel kan opprettes og behandles i et konsoliderings- eller elimineringsfirma.
-   Finansrapportering kan brukes til å vise elimineringskontoene og -dimensjonene i en bestemt rad eller kolonne.
-   En separat juridisk enhet kan brukes til å postere manuelle transaksjonsoppføringer for å spore elimineringer.

Dette emnet fokuserer på elimineringsregler som behandles i et konsoliderings- eller elimineringsfirma. Du kan definere elimineringsregler for å opprette elimineringstransaksjoner i en juridisk enhet som er angitt som juridisk målenhet for elimineringer. Denne juridiske mottakerenheten kalles den den juridiske elimineringsenheten. Elimineringsjournaler kan enten genereres under konsolideringsprosessen eller ved hjelp av et elimineringsjournalforslag. Før du definerer elimineringsregler, bør du gjøre deg kjent med følgende begreper:

-   **Kilde for juridisk enhet** – Den juridiske enheten der beløpene som elimineres, var postert.
-   **Juridisk målenhet** – Den juridiske enheten der elimineringsreglene posteres.
-   **Juridisk enhet for eliminering** – Den juridiske enheten som er angitt som juridisk målenhet for elimineringer.
-   **Konsolidert juridisk enhet** – Den juridiske enheten som opprettes for å rapportere økonomiske resultater for en gruppe med juridiske enheter. De økonomiske dataene fra de juridiske enhetene konsolideres til denne juridiske enheten, og deretter opprettes en finansrapport ved hjelp av de kombinerte dataene.

Følgende tabell viser hvilke typer transaksjoner du kan være nødt til å eliminere.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>transaksjonstype</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Salgsordreoppføringer og -fakturering (sentralisert behandling)</td>
<td>Du selger et produkt til en kunde på vegne av en annen juridisk enhet i organisasjonen.</td>
</tr>
<tr class="even">
<td>Salgsordreoppføring (mellom firmaer / internt i ett firma) og -fakturering</td>
<td>Du selger varer mellom juridiske enheter i organisasjonen.</td>
</tr>
<tr class="odd">
<td>Bestillinger (sentralisert behandling)</td>
<td>Du kjøper lagerbeholdning, utstyr, tjenester, anleggsmidler og andre produkter fra en leverandør på vegne av en annen juridisk enhet i organisasjonen.</td>
</tr>
<tr class="even">
<td>Lagerstyring (mellom firmaer / internt i ett firma)</td>
<td><ul>
<li>Du overfører beholdningen til én juridisk enhet til anleggsmidler for en annen juridisk enhet i organisasjonen.</li>
<li>Du overfører beholdningen til én juridisk enhet til beholdningen for en annen juridisk enhet i organisasjonen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lagersporing i transitt</td>
<td>Du overfører varer mellom lagre i den samme juridiske enheten, men i forskjellige geografiske områder.</td>
</tr>
<tr class="even">
<td>Sentralisert fakturabehandling for leverandører</td>
<td>Du registrerer en faktura på vegne av en annen juridisk enhet i organisasjonen.</td>
</tr>
<tr class="odd">
<td>Sentralisert betaling av leverandører</td>
<td>Du betaler en faktura på vegne av en annen juridisk enhet i organisasjonen.</td>
</tr>
<tr class="even">
<td>Kontantstyring og pengebeholdning (sentralisert behandling)</td>
<td><ul>
<li>Du behandler skatteinnbetalinger, skatterefusjoner, rentebelastninger, lån, forskudd, utbetalt aksjeutbytte og forhåndsbetalt royalty eller provisjon.</li>
<li>Du betaler en utgift på vegne av en annen juridisk enhet i organisasjonen. Fakturaen legges inn i den juridiske målenhetens bøker, og du må utligne mellom juridiske enheter. En juridisk enhet betaler for eksempel reiseregningsrapporten for en ansatt i en annen juridisk enhet. I dette tilfellet har den ansattes reiseregningsrapport utgifter som er knyttet til en annen juridisk enhet.</li>
<li>Du overfører kontanter fra én juridisk enhet til en annen i organisasjonen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kunder (sentralisert behandling)</td>
<td>Du mottar kontanter for kundefakturaen for en annen juridiske enhet, og du betaler sjekken inn på bankkontoen til denne juridiske enheten.</td>
</tr>
<tr class="even">
<td>Lønn (sentralisert behandling, mellom firmaer / innenfor ett firma)</td>
<td><ul>
<li>Du betaler lønnen til en annen juridisk enhet. En juridisk enhet betaler for eksempel sin egen lønn til sine ansatte, men viderefakturerer arbeid som en ansatt har utført for en annen juridisk enhet i den lønnsperioden. Eller en ansatt har arbeidet deltid for juridisk enhet A og deltid for juridisk enhet B, og fordelene beregnes ut fra samlet lønn. I disse tilfellene inneholder lønnen til den ansatte lønn fra begge juridiske enheter. Ikke bare posteres lønn, men også avgifter, fordeler, fradrag og avsetninger for lønn.</li>
<li>Du overfører arbeidskraft fra en avdeling eller divisjon til en annen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Anleggsmidler (mellom firmaer / innenfor ett firma)</td>
<td>Du overfører anleggsmidler til en annen juridisk enhets anleggsmidler eller lagerbeholdning.</td>
</tr>
<tr class="even">
<td>Tildelinger (mellom firmaer / innenfor ett firma)</td>
<td>Du behandler firmatilordninger. Tildelinger er aktiviteter til en hvilken som helst tildelt konto, uansett opprinnelsesmodul.</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Eksempel
Den juridiske enheten, juridisk enhet A, selge noe til en annen juridisk enhet i organisasjonen, juridisk enhet B. Følgende eksempel viser hvordan transaksjoner som forekommer mellom de to juridiske enhetene kan måtte elimineres:

-   Juridisk enhet A selger en gjenstand som koster 10,00 til juridisk enhet B for 10,00.
-   Juridisk enhet A selger en gjenstand som koster 10,00 til juridisk enhet B for 10,00 pluss 2,00 i faktiske leveringskostnader.
-   Juridisk enhet A selger en gjenstand som koster 10,00 til juridisk enhet B for 15,00 og anerkjenner en margin på dette salget.
-   Juridisk enhet A selger en gjenstand som koster 10,00 til juridisk enhet B for 15,00 og anerkjenner halvparten av marginen på dette salget. Juridisk enhet B anerkjenner den andre halvparten av marginen på salget. Derfor deles omsetningen. Delt omsetning gir et insentiv til å bestille fra en annen juridisk enhet i organisasjonen i stedet for en ekstern organisasjon.

Alle disse transaksjonene genererer transaksjoner mellom firmaene som posteres til forfall-til- og forfall-fra-kontoer. I tillegg kan disse transaksjonene omfatte påslags- og avslagsbeløp når beløpet for konserninternt salg ikke er likt kostnadene for varene som ble solgt.

## <a name="set-up-elimination-rules"></a>Definere elimineringsregler
Når du definerer elimineringsregler i Dynamics 365 for operasjoner, anbefaler vi at du oppretter en finansdimensjon spesielt for eliminering formål. De fleste kundene gi den navnet handel Partner eller noe lignende. Hvis du bestemmer deg for ikke å bruke en finansdimensjon, må du passe på å har primære kontoer som er spesifikke for bare konserninterne transaksjoner. 

Oppsettet for elimineringer som finnes i Oppsett-området i modulen konsolideringer. Når du skriver inn en beskrivelse av regelen, må du velge selskapet som vil postere elimineringsjournalen til. Dette bør være et selskap som har **Bruk til finanseliminering** valgt i oppsettet for juridisk enhet. 

Du kan angi en dato da elimineringsregelen trer i kraft, og når den er utløpt, om nødvendig. Du må angi **aktive** til **Ja** Hvis du vil at den skal være tilgjengelig i forslagsprosessen eliminering. Velg et journalnavn som har en **eliminering**.

Når du har definert grunnleggende, kan du definere de faktiske behandlingen av reglene ved å klikke **linjer**. Det finnes to alternativer for elimineringer, eliminere hvor bevegelse eller definere et fast beløp. 

Velg kildekontoen. Du kan bruke en stjerne (\*) som et jokertegn. For eksempel 1\* merker alle kontoer som starter med 1 som en datakilde for tildelingen. 

Når du har valgt kilden kontoene, den **konto spesifikasjonen** bestemmer kontoen fra målfirmaet som brukes. Velg **kilde** Hvis du vil bruke samme hovedkontoen som er definert i den **kilde** konto. Hvis du velger **brukerdefinerte**, og deretter må du angi en målkonto. 

I dimensjon-spesifikasjonen fungerer på samme måte. Hvis du velger **kilde**, vil den bruke de samme dimensjonene i målfirmaet som kilde-selskapet. Hvis du velger **brukerdefinerte**, må du angi dimensjoner i målfirmaet ved å klikke på **målet dimensjoner** menyelementet. 

Velg Kildedimensjoner og finansdimensjoner og verdiene som brukes som en kilde for eliminering.

## <a name="process-elimination-transactions"></a>Behandle elimineringstransaksjoner
Det er to måter å behandle elimineringstransaksjoner, under Konsolider online prosessen eller ved å opprette en elimineringsjournalen og kjøre eliminering forslagsprosessen. Denne delen fokuserer på å opprette kladden og kjøre elimineringsprosessen. 

I et selskap som er definert som et elimineringsfirma, velger du **elimineringsjournalen** i modulen konsolideringer. Når du har valgt journalnavnet, klikker du **linjer**. Du kan kjøre forslaget ved å velge den **forslag** -menyen og deretter velge **Elimineringsforslag**.

Velg firmaet som er kilden til de konsoliderte dataene, og deretter velger du regelen du vil behandle. Angi en startdato for å starte søket for eliminering beløp, og en sluttdato for å avslutte søket datoen for eliminering beløp. Den **GL Bokføringsdato** -feltet er datoen som brukes for postering av journal til finans. Når du klikker **OK**, kan du se gjennom beløpene og postere journalen.


