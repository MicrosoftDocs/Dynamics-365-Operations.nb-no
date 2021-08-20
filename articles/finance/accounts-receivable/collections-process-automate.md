---
title: Automatisering av innkrevingsprosess
description: Dette emnet beskriver prosessen med å definere strategier for innkrevingsprosesser som automatisk identifiserer kundefakturaer som krever en e-postpåminnelse, en innkrevingaktivitet eller en purring som skal sendes til kunden.
author: panolte
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 0afc56ecea72e281d689930cc91cf6048426d3127ab10c8c284b2eea0f3933d6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723901"
---
# <a name="collections-process-automation"></a>Automatisering av innkrevingsprosess

[!include [banner](../includes/banner.md)]

Dette emnet beskriver prosessen med å definere strategier for innkrevingsprosesser som automatisk identifiserer kundefakturaer som krever en e-postpåminnelse, en innkrevingaktivitet (for eksempel en telefonsamtale) eller en purring som skal sendes til kunden. 

Organisasjoner bruker betydelig tid på å undersøke saldorapporter, kundekontoer og åpne fakturaer for å finne ut hvilke kunder som bør kontaktes om en åpen faktura eller kontosaldo. Denne undersøkelsen tar tid fra en innkrevingsagents tid som brukes til å kommunisere med kunder for å samle forfalte forfalte balanser eller løse fakturatvister. Ved hjelp av automatisering av innkrevingsprosess kan du sette opp en strategibasert tilnærming til innkrevingsprosessen. Dette hjelper deg med å bruke innkrevingsaktiviteter konsekvent ved å levere tilpassede e-postpåminnelser eller programmert prosess for å sende purringer. 

## <a name="collections-process-setup"></a>Oppsett av innkrevingsprosess
Du kan bruke siden **Oppsett av innkrevingsprosess** (**Kreditt og innkreving > Setup > Oppsett av innkrevingsprosess**) til å opprette en prosess for automatiserte innkrevinger som vil planlegge aktiviteter, sende e-postmeldinger og opprette og postere kundepurringer. Prosesstrinnene er basert på den ledende eller eldste fakturaen som er åpen. Hvert trinn bruker denne fakturaen for å bestemme hvilken kommunikasjon eller aktivitet som skal skje med en bestemt kunde.  

Innkrevingsteam sender vanligvis ut tidlig varsel knyttet til hver utestående faktura, slik at en kunde blir varslet når fakturaen er i ferd med å forfalle. Valget **Før purring** kan angis slik at ett trinn i hvert prosesshierarki kan gjøres oppmerksom på for hver faktura når fakturatiden når det trinnet.

### <a name="process-hierarchy"></a>Prosesshierarki
Hvert kundeutvalg kan bare tilordnes til ett prosesshierarki. Hierarkiets rangering av dette trinnet identifiserer hvilken prosess som vil ha forrang hvis en kunde inkluderes i mer enn ett utvalg som har fått tilordnet et prosesshierarki. Utvalgs-ID-en bestemmer hvilke kunder som skal tilordnes til prosessen. 

De rolige dagene brukes til å sikre at en kunde ikke blir kontaktet for ofte av den automatiserte prosessen.  Hvis de rolige dagene for eksempel er satt til to, vil ikke en kunde bli kontaktet av den automatiserte prosessen på minst to dager, selv om den opprinnelige ledende fakturaen er utlignet i sin helhet. 

Hvis du vil utelate kunder fra prosessautomatisering hvis kontosaldoen eller fakturasaldoen er mindre enn en definert verdi, setter du feltet **Utelat fra prosess** til **Ja** og angir beløpsverdien.

## <a name="process-details"></a>Prosessdetaljer
**Beskrivelse** brukes til å identifisere formålet med eller navnet på trinnet i hierarkiet.

**Handlingstype** definerer om trinnet skal opprette en aktivitet, sende en e-post eller opprette en purring.

**Forretningsdokument** definerer malen som brukes til å opprette handlingstypen.  Dette kan være en aktivitetsmal, en e-postmal eller en purring per kunde. 

Handlingstypene kan opprettes på enten før eller etter forfallsdatoen for fakturaen, basert på innstillingen som vises i kolonnen **Dager i forhold til fakturaens forfallsdato**.

Når du velger en handlingstype for e-post, vil mottakeren bli brukt til å definere om det er en kunde-, salgsgruppe- eller inkassoagentkontakt. Verdien i feltet **Kontakt for forretningsformål** bestemmer deretter hvilken kontakt fra kundens konto som skal motta kommunikasjonen.

## <a name="business-document-details"></a>Detaljer for forretningsdokument
Detaljene i forretningsdokumentet varierer, basert på handlingstypen som er valgt i prosessdetaljene.  Når handlingstypen er en aktivitet, vil aktivitetsmaldetaljene vises.  Disse detaljene omfatter navnet på aktivitetsmalen, typen aktivitet som blir opprettet, formålet med aktiviteten, antall dager som er planlagt for fullføring av aktiviteten, og detaljene for aktiviteten.  Denne aktiviteten vil deretter koble til den ledende fakturaen som forteller mottakeren om handlingen som er nødvendig for å fullføre aktiviteten.

Hvis handlingstypen er en e-post i prosessdetaljene, vil denne delen inneholde to hurtigkategorier.  Den første brukes til å definere mal-ID-en, e-postbeskrivelsen, standardspråket, brukernavnet som blir tilordnet e-postmeldinger som sendes automatisk, og de tilknyttede avsenderes e-postadresser. Det andre gjør det mulig å opprette brødteksten i e-postmeldingen etter at verdiene i feltene **Språk** og **Emne** er lagret ved å velge **Rediger**.  Dette åpner et vindu som tillater at HTML-innhold lastes opp. Du kan også skrive inn meldingen som er opprettet manuelt, i boksen nederst til venstre i vinduet.  

> [!Note]
> En Outlook-e-postadresse kan lagres sammen med ønsket brødtekst i en kommunikasjon i HTML-format. Dette kan deretter lastes opp til å implementere malen. <br> <br> Hvis handlingstypen for purring er valgt, vil det ikke være en detaljinndeling for forretningsdokument i oppsettsskjemaet.


## <a name="fasttab-reference"></a>Referanse for hurtigkategori
Tabellene nedenfor viser en liste over sidene og feltene som de angitte hurtigkategoriene er tilgjengelige fra, sammen med en beskrivelse av informasjonen i den kategorien. 

### <a name="process-hierarchy"></a>Prosesshierarki

|     Side                                                  |     Felt                         |     Beskrivelse                           |
| --------------------------------------------------------  |-------------------------------    |---------------------------------------    |
|     Oppsett av innkrevingsprosess <br> Prosessautomatisering       |                                   |     Opprett og behandle innkrevingsprosesser basert på tilordning av kundeutvalg.                                                                                                                             |
|     Oppsett av innkrevingsprosess <br> Prosessautomatisering       |     Hierarki                     |     Definerer prosessautomatisering som brukes til å tilordne en kunde hvis de tilhører flere utvalg.                                                                                                   |
|     Oppsett av innkrevingsprosess <br> Prosessautomatisering       |     Pulje-ID                       |     Spørringer som definerer en gruppe kundeposter.                                                                                                                                                        |
|     Oppsett av innkrevingsprosess <br> Prosessautomatisering       |     Rolige dager                    |     Begrens hvor ofte et prosesstrinn kan fullføres. Hvis det for eksempel er satt inn to rolige dager, vil neste prosesstrinn ikke forekomme i minst to dager hvis den ledende fakturaen endres.     |
|     Oppsett av innkrevingsprosess <br> Prosessautomatisering       |     Utelat fra prosess        |     Hvis du velger **Kundealdersfordelingssaldo mindre enn** eller **Fakturabeløp mindre enn**, utelates en kunde fra prosessautomatisering hvis verdikriteriene ikke er oppfylt.                                   |

### <a name="process-details"></a>Prosessdetaljer
|     Side                                                  |     Felt                                         |      Beskrivelse                  |
|--------------------------------------------------------   |-----------------------------------------------    |----------------------------   |
|     Oppsett av innkrevingsprosess <br> Prosessautomatisering       |                                                   |     Definer trinnene som er tatt på grunnlag av den ledende fakturaen.                                                                                                |
|                                                           |     Beskrivelse                                   |     Fritekstfelt som brukes til å gi et navn og/eller en beskrivelse av trinnet.                                                                           |
|                                                           |     Handlingstype                                   |     Aktivitet, e-post eller purring som vil bli opprettet ved hjelp av prosesstrinnet.                                                                     |
|                                                           |     Forretningsdokument                           |     Definerer aktiviteten eller e-postmalen som brukes under prosesstrinnet.                                                                        |
|                                                           |     Når                                          |     Definerer om prosesstrinnet skal skje før eller etter den ledende forfallsdatoen for fakturaen sammen med feltet **Dager i forhold til fakturaens forfallsdato**.        |
|                                                           |     Dager i forhold til fakturaens forfallsdato        |     Sammen med feltet **Når** identifiseres tidsberegningen for prosesstrinnet.                                                                          |
|                                                           |     Varsel om purring                                   |     Med dette valget kan du angi ett trinn per prosesshierarki og kjøre mot hver faktura når tidsmålingskriteriene nås.                                                |
|                                                           |     Mottaker                                     |     Angir om det skal sendes en e-post til kontakten for kunde, salgsgruppe eller innkrevingsagent.                                                   |
|                                                           |     Kontakt for forretningsformål                    |     Bestemmer hvilken mottakerens e-postadresse som brukes i e-postkommunikasjon.                                                                                 |

### <a name="business-process-activity-template-details"></a>Maldetaljer for forretningsprosessaktivitet 
|     Side                                                  |     Felt                     |      Beskrivelse                  |
|--------------------------------------------------------   |----------------------------   |-------------------------  |
|     Oppsett av innkrevingsprosess <br> Prosessautomatisering       |                               |     Delen av oppsettprosessen som identifiserer detaljene i aktivitetsmalen.                                                                      |
|     Oppsett av innkrevingsprosess <br> Prosessautomatisering       |     Aktivitetsmal       |     Identifiserer type, formål, antall dager som skal fullføres, og gir informasjon om aktiviteten som vil bli opprettet under et aktivitetstrinn for prosessen.       |

### <a name="business-document-email-template-details"></a>Detaljer for e-postmal for forretningsdokument 
|     Side                                                  |     Felt     |      Beskrivelse                  |
|--------------------------------------------------------   |-------------- |-----------------------------  |
|     Oppsett av innkrevingsprosess <br> Prosessautomatisering       |               |     Identifiserer e-postbeskrivelsen, standardspråket, avsendere og e-postadressen som blir opprettet under et prosesstrinn for en e-post.        |


### <a name="collections-history"></a>Innkrevingshistorikk 
|     Side                              |     Felt     |      Beskrivelse                                                          |
|------------------------------------   |-------------- |---------------------------------------------------------------------  |
|     Oppsett av innkrevingsprosess       |               |     Vis den nylige historikken for det valgte prosesshierarkiet.       |

### <a name="collection-process-assignment"></a>Tilordning for innkrevingsprosess
|     Side                              |     Felt     |      Beskrivelse                                                  |
|------------------------------------   |-------------- |-----------------------------------------------------------    |
|     Oppsett av innkrevingsprosess       |               |     Vis kunder som er tilordnet en innkrevingsprosess.  
|     Manuell tilordning               |               |     Vis kunder som er manuelt tilordnet til en prosess, eller velg kunder som skal tilordnes til en prosess. |
|     Forhåndsvis prosesstilordning      |               |     Forhåndsvis kundene som vil bli tilordnet til en strategi når den kjøres.   |
|     Forhåndsvis kundetilordning     |               |     Vis strategien som en bestemt kunde er tilordnet.    |
 
 ### <a name="process-simulation"></a>Behandle simulering
|     Side                              |     Felt     |      beskrivelse                                                  |
|------------------------------------   |-------------- |-----------------------------------------------------------    |
|    Behandle simulering                 |               |     Forhåndsvis handlingene som vil bli opprettet hvis den valgte prosessen automatisk kjøres på dette tidspunktet. |

### <a name="parameters"></a>Parametere
|     Side                                                                  |     Felt                                             |      beskrivelse                              |
|-------------------------------------------------------------------------- |------------------------------------------------------ |-------------------------------------  |
|     Parametere for kunde > Automatisering av innkrevingsprosess     |     Prosent av kunder per satsvis oppgave          |     Innstilling for å fastslå antall satsvise oppgaver per automatiseringsprosess.                                          |
|     Parametere for kunde > Automatisering av innkrevingsprosess     |     Poster purringer automatisk           |     Handlingstyper for purringer vil postere purringen i løpet av automatiseringen.                                      |
|     Parametere for kunde > Automatisering av innkrevingsprosess     |     Opprette aktiviteter for automatisering                |     Opprett og lukk aktiviteter for handlingstyper uten aktivitet hvis du vil vise alle automatiske trinn som er utført på en konto.        |
|     Parametere for kunde > Automatisering av innkrevingsprosess     |     Dager for å beholde automatisering av innkrevingsprosesser     |     Definerer hvor mange dager det er lagret en innkrevingshistorikk.                                                       |
|     Parametere for kunde > Automatisering av innkrevingsprosess     |     Utelat faktura etter aktivering av siste prosesstrinn    |     En faktura som kommer til det siste trinnet i innkrevingsprosessen, brukes ikke til å opprette fremtidige handlingstyper for automatisk prosess. Den neste eldste fakturaen vil bestemme neste trinn for automatisk prosess for å sikre at handlingene for innkreving av automatisk behandling fortsetter.                                                        |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
