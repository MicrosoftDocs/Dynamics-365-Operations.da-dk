---
title: Part og globalt adressekartotek
description: I dette emne beskrives funktionen til part og globalt adressekartotek for dobbeltskrivning.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: e7bec58f8094a1448017822e7d8840368cc482b8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750782"
---
# <a name="party-and-global-address-book"></a>Part og globalt adressekartotek

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Part og globalt adressekartotek er begreber i Finance and Operations-programmer. En part kan være en person eller organisation. Det er en god ide at gemme og administrere egenskaberne for en **part** globalt, f.eks. navn, sprog, kontakter og adresser. Når en egenskabsværdi ændres på ét sted, afspejler den alle de steder, hvor **parten** er involveret.

## <a name="party"></a>Part

En *part* er en person eller organisation, der er involveret i virksomheden. Ved at bruge partbegrebet kan en person eller organisation spille mere end én rolle (arbejder, kunde, leverandør eller kontakt) i en virksomhed. Rollen er baseret på sammenhæng og formål. Her er nogle eksempler fra to fiktive firmaer, Contoso og Fabrikam.

+ **Arbejder**: En medarbejder. Det kan f.eks. være en medarbejder hos Contoso.
+ **Leverandør**: En leverandørorganisation eller en enkeltmandsvirksomhed, der leverer varer eller ydelser til en virksomhed. Hvis Fabrikam f.eks. sælger varer til Contoso, har Fabrikam leverandørrollen.
+ **Kontakt**: En person, der kan kontaktes. Hvis Contoso f.eks. køber varer fra Fabrikam, kontakter en medarbejder hos Contoso kontakten hos Fabrikam.
+ **Kunde**: En kunde er en person eller et firma, der køber ting fra et firma. Hvis Contoso f.eks. køber varer fra Fabrikam, er Contoso kunde hos Fabrikam.

Partmodellen bruges ofte til at repræsentere mellemstore til komplekse relationer mellem organisationer og personer, særligt når en part spiller mere end én rolle. Her er nogle almindelige eksempler:

+ En part kan både være kunde og leverandør. I Nordamerika sælger Fabrikam f.eks. ledninger til Contoso og køber samlede højttalere hos Contoso. I Europa sælger Fabrikam reservedele til Contoso, men køber ikke noget hos Contoso.
+ En part kan både være medarbejder og kunde. En medarbejder hos Contoso køber f.eks. elektronik fra Contoso til personlig brug.
+ Der kan være en mange til mange-relation mellem en person og en organisation. Fabrikam leverer f.eks. serviceteknikere og ansætter en placeringskoordinator. Koordinatoren svarer til serviceteknikere for arbejdsanmodninger fra flere af Fabrikams kunder. Contoso er en af kundekontiene. Når Contoso skal bruge en specialist, kontakter Contoso koordinatoren, som derefter opfylder anmodningen. Koordinatoren håndterer anmodninger for alle kunder og opretter en mange til mange-relation.

Følgende billede viser datamodellen for part:

![Datamodel for part](media/party-gab-image1.png)

> [!Tip]
> Når du forsøger at oprette en ny kontopost, skal du bruge feltet "Part" til at søge efter posten ved hjælp af navnet. Hvis du finder posten, skal du blot vælge posten. Alle data fra parten udfyldes automatisk. Du behøver ikke at udfylde alle de obligatoriske felter manuelt. Denne funktionsmåde findes i formularerne Konto, Kontakt og Leverandør, der er leveret som standard.

Ikke alle partroller i Finance and Operations understøttes af dobbeltskrivning. Du kan få vist en komplet liste over partroller i [Oversigten over globalt adressekartotek](../../../fin-ops/organization-administration/overview-global-address-book.md).

### <a name="global-address-book"></a>Globalt adressekartotek

Det globale adressekartotek er et bibliotek med post- og elektroniske adresser på de organisationer og enkeltpersoner, der deltager i et firma.

Det globale adressekartotek gemmer og håndterer lige så mange postadresser og elektroniske adresser, der er behov for. Antag f.eks., at Fabrikam har benzintanke på 50 steder. Alle steder har forskellige postadresser, mails og telefonnumre. Alle firmakøb faktureres til den primære benzintank, men indkøb leveres direkte til den bestemte benzintank, der har anmodet om købet. Det globale adressekartotek gemmer hovedbenzintanken som faktureringsadresse og hver enkelt benzintank som leveringsadresse for Fabrikam. Adresserne kan gemmes én gang og hentes efter behov for tilbud og ordrer.

En person eller organisation kan have mere end én rolle i forretningskonteksten. Når de gør dette, kan deres postadresser og elektroniske adresser være ens. I dette tilfælde skal adresseændringen i den ene rolle vises i den anden rolle og omvendt. Det globale adressekartotek gemmer og håndterer adresser globalt.

![Datamodel for globalt adressekartotek](media/party-gab-image2.png)

## <a name="contacts"></a>Kontakter

I kundeengagementapps er en *Kontakt* en person. Men **Kontakt**-tabellen er dog blevet overlæsset med oplysninger om en person, en portalbruger, en B2C-kunde eller en leverandør. Repræsentationen er implicit, og du kan ikke se forskellen uden at undersøge relaterede transaktioner. **Kontakt**-tabellen er begrænset til at have en 1:1-relation til **Konto**-tabellen. Som en del af modellen til part og globalt adressekartotek introducerer dobbeltskrivning eksplicitte egenskaber til klassifikation, og dobbeltskrivning tillader N:N-relationer mellem en **Kontakt** og en organisation (kontoenhed eller leverandørenhed).

Der findes to typer **Kontakt**-rækker:

+ Stribet kontakt – Kontaktrække med en obligatorisk værdi i feltet **Firma**.
+ Ikke-stribet kontakt – Kontaktrække med tomt **Firma**-felt.

I tabellen **Kontakt** kan du gemme disse typer rækker:

Rækketype | Betegnelse
---|---
En person, der er kunde, f.eks. en salgbar kontakt eller B2C-kunde. | En stribet kontaktpost, hvor feltet **Firma** ikke er tomt, og feltet **Er kunde** er angivet til **Ja**.
En person, der f.eks. er leverandør og enkeltmandsvirksomhed som leverandør. | En stribet kontaktpost, hvor feltet **Firma** ikke er tomt, og feltet **Er leverandør** er angivet til **Ja**.
En person, der både er kunde og leverandør. | En stribet kontaktpost, hvor feltet **Firma** ikke er tomt, feltet **Er kunde** er angivet til **Ja**, og feltet **Er leverandør** er angivet til **Ja**. En person kan både være producent af ét produkt og en forbruger af et andet produkt. Både Finance and Operations-apps og dobbeltskrivning understøtter denne relation.
En person, der er kontaktperson for en organisation, men ikke er kunde eller leverandør. | En ikke-stribet kontaktpost, hvor feltet **Firma** er tomt, feltet **Er kunde** er angivet til **Nej**, og feltet **Er leverandør** er angivet til **Nej**.

## <a name="contact-for-party"></a>Kontakt for part

**Kontakt for part** gemmer og håndterer N:N-relationer mellem **Konto**-rækker og **Kontakt**-rækker. De kan filtrere stribede **Kontakt**-rækker fra ikke-stribede rækker og kun knytte de ikke-stribede **Kontakt**-rækker til en **Konto**- eller **Leverandør**-række.

Natasha Jones og Miguel Reyes er f.eks. dyrlæger, som arbejder for farme i deres lokalområder. Natasha betjener Seattle-området, og Miguel betjener Kent-området. I kundeengagementsappen er farmene repræsenteret som kunder, og dyrlægerne er kontaktpersoner. En enkelt **Kontakt**-post for Natasha er tilknyttet alle de farme, som Natasha arbejder med. Og en enkelt **Kontakt**-post for Miguel er tilknyttet alle de farme, som Miguel arbejder med.

Disse relationer gemmes i tabellen **Kontakt for part**. Du kan finde oplysningerne i standardformularerne:

+ Når du er i formularen **Konto**, findes der en fane med navnet **Tilknyttede kontakter**. Du kan bruge denne fane til at knytte en eller flere kontakter til rækken **Konto**. I denne formular knytter du en kontaktperson til en organisation. Når du har tildelt kontaktpersoner, kan du vælge en som primær kontakt for den pågældende konto. Du kan kun vælge en kontaktperson ved hjælp af formularen **Hurtig oprettelse**. Denne funktionsmåde er den samme, når du bruger formularen **Leverandør**, og posttypen er **Organisation**.
+ Når du er i formularen **Kontakt**, og rækken er en kunde eller leverandør eller begge dele (en stribet kontakt), findes der en fane med navnet **Tilknyttede kontakter**. Du kan bruge denne fane til at knytte en eller flere kontakter. I denne formular knytter du en kontaktperson til B2C-kunden eller leverandøren. Når du har tildelt kontakter, kan du vælge en som primær kontakt. Du kan kun vælge en kontaktperson ved hjælp af formularen **Hurtig oprettelse**.
+ Når du er i formularen **Kontakt**, og rækken er kontaktperson (en ikke-stribet kontakt), findes der en fane med navnet **Tilknyttede organisationer**. Du kan bruge denne fane til at tilknytte en eller flere kunder eller leverandører. I denne formular knytter du en kunde eller leverandør til den underliggende kontaktperson. Kunden eller leverandøren kan være en organisation, en person eller begge dele. Du kan kun vælge én værdi blandt de fire felter ad gangen.

    ![Fanen Tilknyttede organisationer](media/party-gab-image3.png)

    + Hvis du vælger **Part-id**, tildeles den underliggende kontakt alle rollerne for den valgte part.
    + Hvis du vælger **Tilknyttet kontakt**, vælger du den stribede kontakt, der er af typen person.
    + Hvis du vælger **Tilknyttet konto** eller **Leverandør**, vælger du en organisation.

    Uanset dit valg oprettes tilknytningen på partniveau og gælder for alle partens roller og gemmes i enheden "Kontakt for part".

> [!Note]
> Det viste navn på tabellen **Kontakt for part** i kundeengagementsappen er **Kontakt for kunde/leverandør**.

Når du åbner en række med **Kontakt**, hvor **Er kunde** er **Nej** og **Er leverandør** er **Nej**, får du vist fanen **Tilknyttede organisationer**. Du kan bruge denne fane til at knytte en eller flere kunde- eller leverandørorganisationer til kontakten.

Når du åbner en række med **Kontakt**, hvor **Er kunde** er **Ja**, eller **Er leverandør** er **Ja**, får du vist fanen **Tilknyttede kontakter**. Du kan bruge denne fane til at tilknytte en eller flere kontakter.

## <a name="postal-address"></a>Postadresse

Der er indført en ny fane med navnet **Adresser** i formularerne **Konto**, **Kontakt** og **Leverandør**. **Adresserne** understøtter N-adresser ved hjælp af et gitter som vist på dette billede:

![Gitter for postadresse](media/party-gab-image4.png)

+ I kolonnen **Postadresseroller** vises formålet med adressen.
+ I kolonnen **Er primær** vises den primære adresse.
+ I kolonnen **Adressenummer** vises adresserækkefølgen.
+ Du kan bruge knappen **+ Ny adresse** til at oprette en ny adresse. Du kan oprette lige så mange adresser, som du vil.

Felterne **Adresse 1** og **Adresse 2** under fanen **Oversigt** i formularen **Konto** svarer til henholdsvis **leverings-** og **fakturaadresserne**.

![Fanen Oversigt for postadresse](media/party-gab-image5.png)

Felterne **Adresse 1**, **Adresse 2** og **Adresse 3** under fanen **Oversigt** i formularen **Kontakt** svarer til henholdsvis adresserne **Virksomhed**, **Levering** og **Faktura**.

## <a name="electronic-address"></a>Elektronisk adresse

Der er indført en ny fane med navnet **Elektroniske adresser** i formularerne **Konto**, **Kontakt** og **Leverandør**. **Adresserne** understøtter N-adresser ved hjælp af et gitter som vist på dette billede:

![Gitter for elektronisk adresse](media/party-gab-image6.png)

+ Kolonnen **Type** viser adressens type.
+ I kolonnen **Er primær** vises den primære adresse.
+ I kolonnen **Formål** vises formålet med den elektroniske adresse.
+ Du kan bruge **+ Ny elektronisk adresse** til at oprette en ny adresse. Du kan oprette lige så mange adresser, som du vil.

Elektroniske adresser er kun tilgængelige i dette gitter. I fremtidige versioner fjernes alle felter med elektroniske adresser og postadresser fra andre faner, f.eks. fanen **Oversigt** og **Detaljer**.

## <a name="setup-instructions"></a>Installationsvejledning

Hvis du er en eksisterende kunde med dobbeltskrivning, skal du bruge følgende konfigurationsinstruktioner. Ellers kan du springe dette afsnit over.

1. Stop følgende tilknytninger, da de ikke kræves længere. Kør i stedet tilknytningen Kontakter V2 (msdyn_contactforparties).

    + CDS Kontakter V2 og kontakter (refererer til kundekontakter)
    + CDS Kontakter V2 og kontakter (refererer til leverandørkontakter)

2. Følgende enhedstilknytninger opdateres for partfunktioner, så den seneste version skal anvendes på disse tilknytninger.

Tilknyt | Opdater til denne version | Ændringer
---|---|---
Debitorer V3 (konti) | 1.0.0.5 |Fjernede PartyNumber og andre felter, der vedrører parter, f.eks. navn, personlige oplysninger, postadressefelter, adressefelter for elektroniske kontakter osv.
Debitor V3 (kontakter) | 1.0.0.5 | Fjernede PartyNumber og andre felter, der vedrører parter, f.eks. navn, personlige oplysninger, postadressefelter, adressefelter for elektroniske kontakter osv.
Kreditorer V2 (msdyn_vendors) | 1.0.0.6 | Fjernede PartyNumber og andre felter, der vedrører parter, f.eks. navn, personlige oplysninger, postadressefelter, adressefelter for elektroniske kontakter osv.
CDS-salgstilbudshoveder (tilbud) | 1.0.0.6 | Erstattede kontaktpersonen med reference til ContactforParty.
Salgsfakturahoveder V2 (fakturaer) | 1.0.0.4 | Erstattede kontaktpersonen med reference til ContactforParty.
CDS-salgsordrehoveder (salesorders) | 1.0.0.5 | Erstattede kontaktpersonen med reference til ContactforParty.
Kontakter V2 (msdyn_contactforparties) | 1.0.0.2 | Dette er en ny tilknytning. Hvis du har en tidligere version af partløsningen, skal du sørge for at opdatere denne tilknytning til den seneste version som nævnt.
Placeringer af CDS-partpostadresser (msdyn_partypostaladdresses) | 1.0.0.1  | Dette er en ny tilknytning., der er tilføjet som del af forrige partforhåndsversion.
CDS-postadressehistorik V2 (msdyn_postaladdresses) | | Dette er en ny tilknytning., der er tilføjet som del af forrige partforhåndsversion.
Placeringer af CDS-postadresser (msdyn_postaladdresscollections) | | Dette er en ny tilknytning., der er tilføjet som del af forrige partforhåndsversion.
Partkontakter V3 (msdyn_partyelectronicaddresses) | | Dette er en ny tilknytning., der er tilføjet som del af denne version.

## <a name="templates"></a>Skabeloner

En samling af tabeltilknytninger arbejder sammen under interaktion med part og globalt adressekartotek, som vist i følgende tabel.

Finance and Operations-app | Customer Engagement-app     | Betegnelse
----------------------------|-----------------------------|------------
[Titler på kontaktpersoner](mapping-reference.md#223) | msdyn_salescontactpersontitles |
[Debitorer V3](mapping-reference.md#101) | konti |
[Debitorer V3](mapping-reference.md#116) | kontakter |
[CDS-parter](mapping-reference.md#220) | msdyn_parties |
[Lokaliteter for CDS-parts postadresse](mapping-reference.md#233) | msdyn_partypostaladdresses |
[Oversigt over CDS-postadresse V2](mapping-reference.md#235) | msdyn_postaladdresses |
[Lokaliteter for CDS-postadresse](mapping-reference.md#234) | msdyn_postaladdresscollections |
[CDS-salgstilbudshoved](mapping-reference.md#215) | pristilbud |
[CDS-salgsordrehoveder](mapping-reference.md#217) | salesorders |
[Afsluttende hilsner](mapping-reference.md#222) | msdyn_complimentaryclosings |
[Kontakter V2](mapping-reference.md#221) | msdyn_contactforparties |
[Beslutningstagerrolle](mapping-reference.md#224) | msdyn_decisionmakingroles |
[Ansættelsesjobfunktioner](mapping-reference.md#225) | msdyn_employmentjobfunctions |
[Loyalitetsniveauer](mapping-reference.md#226) | msdyn_loyaltylevels |
[Partkontakter V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses |
[Personlige tegntyper](mapping-reference.md#227) | msdyn_personalcharactertypes |
[Salgsfakturahoveder V2](mapping-reference.md#118) | fakturaer |
[Tiltaleformer](mapping-reference.md#228) | msdyn_salutations |
[Kreditorer V2](mapping-reference.md#202) | msdyn_vendors |

Du kan finde flere oplysninger i [referencen til tilknytning af dobbeltskrivning](mapping-reference.md).
