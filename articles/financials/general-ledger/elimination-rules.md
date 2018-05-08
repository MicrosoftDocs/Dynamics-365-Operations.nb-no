---
title: Elimineringsregler
description: Dette emnet inneholder informasjon om elimineringsregler og de ulike alternativene for rapportering om elimineringer.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 882b8f21be94b8cbb0c162c965ffc129b47d7edf
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="elimination-rules"></a>Elimineringsregler

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon om elimineringsregler og de ulike alternativene for rapportering om elimineringer.

Elimineringstransaksjoner er nødvendige når en overordnet juridisk enhet handler med én eller flere underordnede juridiske enheter og bruker konsolidert finansrapportering. Konsoliderte regnskapsoppgjør kan bare omfatte transaksjoner som forekommer mellom den konsoliderte organisasjonen og andre enheter utenfor denne organisasjonen. Derfor må transaksjoner mellom juridiske enheter som er en del av samme organisasjon, fjernes, eller elimineres, fra økonomimodulen, slik at de ikke vises i finansrapporter. Det finnes flere måter å rapportere om elimineringer på:

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
Når du definerer elimineringsregler i Microsoft Dynamics 365 for Finance and Operations, anbefaler vi at du oppretter en finansdimensjon spesielt for elimineringsformål. De fleste kunder gir den navnet Handelspartner eller noe lignende. Hvis du bestemmer deg for ikke å bruke en finansdimensjon, må du sørge for å ha hovedkontoer som er spesifikke for bare konserninterne transaksjoner. 

Oppsettet for elimineringer finnes i Oppsett-området i modulen Konsolideringer. Når du har skrevet inn en beskrivelse av regelen, må du velge firmaet som elimineringsjournalen skal postere til. Dette bør være et firma som har valgt **Brukes til finanseliminering** under oppsettet av den juridiske enheten. 

Du kan angi en dato da elimineringsregelen trer i kraft, og når den utløpes, om nødvendig. Du må angi **Aktiv** til **Ja** hvis du vil at den skal være tilgjengelig i elimineringsforslagsprosessen. Velg et journalnavn som har en type **Eliminering**.

Når du har definert det grunnleggende, kan du definere de faktiske behandlingsreglene ved å klikke **Linjer**. Det finnes to alternativer for elimineringer: eliminere netto endringsbeløp eller definere et fast beløp. 

Velg kildekontoen. Du kan bruke stjerne (\*) som et jokertegn. 1\* velger for eksempel alle kontoer som starter med 1, som en kilde for datatildelingen. 

Når du har valgt kildekontoene, bestemmer **kontospesifikasjonen** kontoen fra målfirmaet som brukes. Velg **Kilde** hvis du vil bruke den samme hovedkontoen som er definert i **Kilde**-kontoen. Hvis du velger **Brukerdefinert**, må du angi en målkonto. 

Dimensjonsspesifikasjonen fungerer på samme måte. Hvis du velger **Kilde**, vil den bruke de samme dimensjonene i målfirmaet som kildefirmaet. Hvis du velger **Brukerdefinert**, må du angi dimensjoner i målfirmaet ved å klikke **Måldimensjoner**-menyelementet. 

Velg kildedimensjoner og finansdimensjoner og verdiene som brukes som en kilde for eliminering.

## <a name="process-elimination-transactions"></a>Behandle elimineringstransaksjoner
Det er to måter å behandle elimineringstransaksjoner på, under den elektroniske konsolideringsprosessen eller ved å opprette en elimineringsjournal og kjøre elimineringsforslagsprosessen. Denne delen fokuserer på å opprette journalen og kjøre elimineringsprosessen. 

I et firma som er definert som et elimineringsfirma, velger du **Elimineringsjournal** i modulen Konsolideringer. Når du har valgt journalnavnet, klikker du **Linjer**. Du kan kjøre forslaget ved å velge **Forslag**-menyen og deretter velge **Elimineringsforslag**.

Velg firmaet som er kilden til de konsoliderte dataene, og velg deretter regelen du vil behandle. Angi en startdato for å starte søket for elimineringsbeløp, og en sluttdato for å avslutte søkedatoen for elimineringsbeløp. Feltet **FIN-posteringsdato** brukes til å postere journalen til økonomimodulen. Når du klikker **OK**, kan du se gjennom beløpene og postere journalen.




