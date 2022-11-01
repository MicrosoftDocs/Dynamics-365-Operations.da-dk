---
title: Begræns brug af betalingstoken
description: Denne artikel beskriver den funktion, der begrænser den måde, betalingstokens bruges på i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 8092ab0724f33f21759aa84d25e0bdcb5b2ad5dd
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709647"
---
# <a name="limit-payment-token-usage"></a>Begræns brug af betalingstoken

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Denne artikel beskriver den funktion, der begrænser den måde, betalingstokens bruges på i Microsoft Dynamics 365 Commerce. Brugen af token er begrænset til området for en salgsordre, eller hvis der gives kundesamtykke, gemmes den som et kort i en fil.

## <a name="key-terms"></a>Vigtige termer

| Periode | Beskrivende tekst |
|---|---|
| Token | En XML-blob, der refereres til, i Dynamics 365-systemet, som gemmer betalingsreferencer til transaktionsformål. |
| Kort på fil | Et gemt kortreferencetoken, som er aftalt for fremtidig brug i Dynamics 365-systemet eller betalings-gateway'en, og som er specifik for en kundes konto. |

Grænserne for brug af betalingstoken gælder for alle miljøer, der bruger en betalings-gateway-tjeneste, hvor der anvendes tilbagevendende tokens. I [Dynamics 365 Payment Connector til Adyen](adyen-connector.md) bruges som standard tilbagevendende betalingstokens til at udføre efterfølgende ordrehandlinger som f.eks. godkendelsesreguleringer og gengodkendelser.

Hvis du vil styre, hvordan disse tilbagevendende betalingstokens bruges i hele systemet, begrænser funktionen **Begræns brugen af betalingstoken til ordrekonteksten** brugen af et tilbagevendende token til området for en salgsordre i systemet. Når den er aktiveret, ændrer funktionen brugergrænsefladen i Commerce headquarters ved at opdatere betalingsinputsider og begrænse muligheden for at vælge tidligere debitorbetalingsreferencer til brug i nye transaktionsforekomster.

Denne funktion hjælper med at opfylde brugsreglerne for visse betalingsudstedere, f.eks. Visa. Visa angiver i sine [Visa-kerneregler og Visa-produkt- og -serviceregler](https://usa.visa.com/content/dam/VCOM/download/about-visa/visa-rules-public.pdf), at brugen af betalingstokens skal begrænses til området for en transaktion, medmindre kortholderen accepterer andet.

Funktionen **Begræns brugen af betalingstoken til ordrekonteksten** er kun relevant, hvis du bruger en betalingsgateway-tjeneste, der anvender referencer til tilbagevendende betalingstoken.

## <a name="enable-the-feature"></a>Aktivere funktionen

Hvis du vil aktivere funktionen **Begræns brugen af betalingstoken til ordrekonteksten** skal du i Commerce headquarters for dit miljø gå til **Arbejdsområder \> Funktionsstyring**, finde og vælge **Begræns brugen af betalingstoken til ordrekonteksten** på listen og derefter vælge **Aktivér nu**.

## <a name="limit-payment-token-usage"></a>Begræns brug af betalingstoken

Når funktionen er aktiveret, vil de sider i Commerce headquarters, der bruges til indlæsning af betalingsmetoder, opdatere, hvordan de refererer til kundebetalingsmåder, som er gemt i fil for kunden. Denne opdatering påvirker primært to driftsområder:

- Hvordan et kundekort på fil angives på vegne af en kunde
- Hvordan betalingsoplysninger for en kunde gemmes til fremtidige betalingsposter i salgsordrer

Når en kunde opretter transaktioner i Commerce-kanaler, gemmes betalingsoplysninger sammen med en salgsordrekontekst. Salgsordrekonteksten begrænser betalingstokenet, så det ikke bruges som betalingsreference i forhold til kundeposten på betalingssiderne for nye eller redigerede salgsordrebetalinger i Commerce headquarters.

### <a name="payment-form-changes"></a>Ændringer i betalingsmåde

Når en callcenter- eller Commerce headquarters-bruger tager en betaling for en kunde i forhold til en salgsordre, viser betalingssiden oplysninger om valg af betalingsmåde. Når funktionen **Begræns brugen af betalingstoken til ordrekonteksten** er aktiveret, vises der kun gemte "kort i fil"-poster, hvis en bruger vælger plustegnet (**+**) på betalingssiden. Ændringer kræver, at callcenter- eller Commerce headquarters-brugeren angiver alle de betalingsoplysninger, kunden har oplyst, da de udfyldte siden **Angiv oplysninger om debitorbetaling** for den nye salgsordretransaktion.

Listen over værdier i feltet **Nummer** indeholder kun kortreferencer, der er tilknyttet den debitor, som har kortet på fil. Det filtrerer alle tidligere betalingsreferencer ud, der ikke har område for en salgsordre.

Plustegnet (**+**) under feltet **Nummer** forbliver tilgængeligt og kan bruges til at angive de betalingsoplysninger, som kunden har angivet for den transaktion, der er knyttet til den salgsordre, der behandles.

### <a name="how-cards-on-file-work"></a>Hvordan kort på fil fungerer

Når funktionen **Begræns brugen af betalingstoken til ordrekonteksten** er aktiveret, er et kort på fil et tilbagevendende betalingstoken, der gemmes i en kundepost og ikke er begrænset til området for en salgsordre. Et kort på fil giver mulighed for hurtig reference til Commerce headquarters-brugere, når de udfylder betalingssiden for en ny salgsordrebetaling. Denne tokenreference gælder kun for Dynamics 365-miljøet. Til onlinekanaler, der bruger en betalingsgateway-tjeneste, der giver brugere mulighed for at gemme en betalingsmåde til fremtidig brug i betalingsmodulet iFrame, gemmer betalingsgatewayen disse referencer som en separat reference til Dynamics 365-kortet på fil.

Hvis f.eks. Dynamics 365 Commerce Payment Connector for Adyen bruges i en onlinekanal, kan kunder, der angiver deres kreditkortoplysninger i betalingsmodulet iFrame, kun se referencer til gatewaytjenesten for de gemte kort for deres næste onlinekøb, når de godkendes. De kan ikke se det gemte Dynamics 365-miljøkort på fil som en mulighed i betalingsmodulet iFrame. På samme måde kan callcenter-brugeren ikke se deres gemte onlinekortreferencer som valgmuligheder, når de bestiller en ordre via callcenteret. Callcenter-brugeren kan kun se referencer til tidligere kort på fil fra Dynamics 365-systemet (som kunden har godkendt) for at gemme dem til fremtidige ordrer.

Brugere i Commerce headquarters kan gemme et kort på fil til en kunde ved at gå til **Retail og Commerce \> Kunder** og vælge debitorkontoposten. i sektionen **Debitor \> Opsætning** kan brugere, der har rettigheder til at behandle betalingssiderne, bruge indtastningssiden **Kreditkort** til at angive et betalingskort, der gemmes til fremtidige transaktioner. Denne handling hjælper med at spare tid, når fremtidige salgsordrebetalinger behandles for kunden. Brugere i callcenter and Commerce headquarters skal kun angive oplysninger om kort på fil, hvis kunden accepterer at bruge kortreferencen til fremtidige transaktioner.

Når afkrydsningsfeltet **Gem til fremtidig brug** nederst på betalingssiderne i Commerce headquarters giver brugerne mulighed for at gemme kortet på fil til fremtidig brug. Dette afkrydsningsfelt skal kun bruges, hvis kunden accepterer at bruge kortet på fil til fremtidige transaktioner. Du kan vise eller begrænse afkrydsningsfeltet **Gem til fremtidig brug** ved at bruge indstillingen **Tillad kundekort på fil** under fanen **Betaling** på siden **Call center-parametre** i Commerce headquarters. Når denne indstilling er angivet til **Ja**, kan brugere i Commerce headquarters, der har rettigheder til at behandle betalingssider, gemme et kort på fil ved at bruge afkrydsningsfeltet **Gem til fremtidig brug**. Når indstillingen er angivet til **Nej**, er afkrydsningsfeltet ikke tilgængeligt for Commerce headquarters-brugere, der har rettigheder til at behandle betalingssider. Indstillingen **Tillad kundekort på fil** kan bruges, hvis din virksomhed vil begrænse brugen af tilbagevendende tokens i Commerce headquarters, men ønsker endnu ikke at tillade, at et kort på fil gemmes uden en procedure for at sikre, at kundesamtykke er givet.

### <a name="commerce-headquarters-pages-where-the-recurring-token-restrictions-are-enforced"></a>Commerce headquarters-sider, hvor begrænsningerne for de tilbagevendende tokens gennemtvinges

Når du bruger tokenbegrænsning, har det indflydelse på følgende områder i Commerce headquarters, når funktionen er aktiveret:

- Debitorbetalingsoplysninger i **Salgsordre \> Betalinger \> Angiv debitorbetaling**
- Fortløbende ordrer
- Afdragsbetalinger
- Debitorbetalinger med kreditkort

### <a name="manage-payment-tokens-archiving-or-removal"></a>Administrere betalingstokens (arkivering eller fjernelse)

Betalingstokens, der blev oprettet, før funktionsflaget **Begræns brugen af betalingstoken til ordrekonteksten** blev aktiveret (eller mens funktionen var deaktiveret), vil være "uden område" i systemet og kan refereres til på valglister på Commerce headquarters-betalingssiden. Disse tokens kan fjernes jævnligt på to måder i Commerce headquarters:

- Brug siden **Arkivér kreditkorttransaktionsdata** til at oprette et job, der jævnligt fjerner eller arkiverer betalingstokens. Hvis du angiver indstillingen **Slet data uden arkivering** til **Ja**, slettes de tokens, der opfylder indstillingen af **Mindste transaktionsalder (i dage)**. Der er flere oplysninger i [Arkivere kreditkorttransaktionsdata](archive-cc-data.md).
- Brug den nye side **Fjern kreditkorttoken** (**Debitor \>Forespørgsler og rapporter \> Oprydning \> Fjern kreditkorttoken**), som giver dig mulighed for at køre eller definere et batchjob, der sletter betalingstoken. Angiv følgende parametre:

    - Værdien af **Mindste tokenalder i dage** skal være 90 dage eller mere.
    - Indstillingerne **Kør i baggrunden** kan bruges til at definere indstillingerne **Gentagelse** eller **påmindelser**.
    - Der kan tildeles en batchgruppe til kørsel af opgaven for en bestemt gruppe.
    - Hvis indstillingen **Privat** er angivet til **Ja**, er det kun den bruger, der opretter jobbet, som kan køre det.
    - Indstillingen **Ja** til **Kritisk job** sikrer, at systemet aktivt registrerer jobbets status.

Slettede tokens kan ikke hentes. Angiv feltet **Mindste tokenalder i dage** til et interval, der passer til den længste levetid for transaktioner i dit miljø (fra godkendelse til registrering eller refundering).

## <a name="additional-resources"></a>Yderligere ressourcer

[Ofte stillede spørgsmål om betalinger](payments-retail.md)

[Betalingsmodul](../add-checkout-module.md)

[Betalingsmodul](../payment-module.md)
