---
title: Arbejde med publiceringsgrupper
description: I dette emne beskrives funktionen publicering af grupper i Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d757f34d3e16850e4f5de122f63b2b3342f612e49f07c7cf6585362999f03c02
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717666"
---
# <a name="work-with-publish-groups"></a>Arbejde med publiceringsgrupper

[!include [banner](includes/banner.md)]

I dette emne beskrives funktionen publicering af grupper i Microsoft Dynamics 365 Commerce.

E-Commerce-websteder opdateres konstant med nyt indhold i løbet af året. Opdateringer udgives ofte i batches omkring tidspunktet for travle e-Commerce-hændelser som helligdage, sæsonbetonede marketingkampagner eller salgsfremmende lanceringer. Disse opdateringer kræver ofte, at grupper af webstedsindhold (f.eks. sider, billeder, fragmenter og skabeloner) iscenesættes, valideres og udgives samtidigt i en enkelt handling.

Muligheden for at gruppere elementer i logiske sæt, der udgiver elementer sammen og hvor hvert sæt har sin egen livscyklus, giver webstedsforfatterne mange fordele. I Commerce kaldes disse logiske sæt for publiceringsgrupper. De lader webstedsforfattere spore opdateringssæt som deres egne enheder, som kan konfigureres, testes og publiceres.

Forfatterne kan få vist opdateringer i en trinvis publiceringsgruppe uden at det påvirker det aktive websted eller andre selvstændige publiceringsgrupper. Forfatterne kan derefter planlægge publiceringshandlingen, således at de samtidigt udgiver alle elementerne i publiceringsgruppen på det aktive websted. Muligheden for at gruppere, få vist og planlægge opdateringer til udgivelse er vigtig for mange virksomheder på virksomhedsniveau, der genererer en betydelig årlig omsætning omkring milepæle for hændelsesbaseret webstedsopdatering.

Virksomheder kan blive pålagt omkostninger fra langsom eller ugyldig indholdsudrulninger, der ikke går glat. Publiceringsgrupper hjælper med at sikre, at lanceringer organiseres, valideres og udgives til tiden. Uanset om de er store eller små, er publiceringsgrupper et værdifuldt værktøjsæt, der hjælper forfattere med at organisere og forenkle igangværende webstedsopdateringsopgaver.

## <a name="when-to-use-publish-groups"></a>Hvornår skal du bruge publiceringsgrupper?

Du kan bruge publiceringsgrupper, når du skal planlægge og udgive flere dokumenter sammen. Hvis dit websted eksempelvis opdaterer indholdet hver sæson, kan du oprette publiceringsgrupper for disse sæsonprægede marketingbevægelser. Publiceringsgruppen "Efterårssæsonopdatering" kan indeholde nye sæsonbestemte billeder, fragmenter, der har sæsonrelaterede marketingmeddelelser, sider, der omfatter sæsonrelaterede produktsamlinger eller andre sæsonrelaterede opdateringer af webstedet.

En fordel ved publiceringsgrupper er, at du kan planlægge flere opdateringer parallelt. Eksempelvis kan der kort efter opdateringen til udgivelsesgruppen "Efterårssæsonopdatering" være en indholdsopdatering til en bestemt ferieweekend. I dette tilfælde kan du lægge indhold ind til publiceringsgruppen "Efterårssæsonopdatering" samtidig med, at du lægger indhold ind til en efterfølgende "Efterårsferieopdatering"-publiceringsgruppe. Hver publiceringsgruppe indeholder sit eget unikke sæt af sider, billeder, fragmenter, skabeloner osv. Du kan lægge ind, få vist og validere disse to publiceringsgrupper uafhængigt, men på en sideløbende tidslinje. Det kan derefter planlægges således, at hver publiceringsgruppe kan aktiveres på dit websted på bestemte datoer og tidspunkter.

## <a name="turn-on-the-publish-groups-feature"></a>Slå funktionen publiceringsgrupper til

Funktionen publiceringsgrupper er valgfri og skal være aktiveret for dit websted.

Hvis du vil aktivere funktionen publiceringsgrupper for dit websted i Commerce-oprettelsesværktøjerne, skal du følge disse trin.

1. Vælg **Indstillinger for websted** i venstre navigationsrude for at udvide den.
1. Under **Indstillinger for webstedet** skal du vælge **Funktioner**.
1. Angiv indstillingen **Publiceringsgrupper** til **Til**.

## <a name="create-a-publish-group"></a>Opret en publiceringsgrupper

Hvis du vil oprette en publiceringsgruppe for dit websted i Commerce-oprettelsesværktøjerne, skal du følge disse trin.

1. Vælg **Publiceringsgrupper** i navigationsruden til venstre.
1. Vælg **Ny** øverst på kommandolinjen.
1. Angiv et beskrivende navn i dialogboksen **Opret publiceringsgruppe** under **Publiceringsgruppenavn**. Vælg derefter **OK**.

## <a name="set-the-publish-group-authoring-context"></a>Angiv oprettelseskonteksten for publiceringsgruppen

I Commerce er standardoprettelseskonteksten det aktive websteds kontekst. Konteksten for oprettelse af aktive websteder er standardvisningen, hvor du kan få vist og foretage ændringer direkte på dit websted uden at bruge en publiceringsgruppe. Det repræsenterer de seneste direkte opdateringer til den publicerede version af dit websted. Hvis kontekstkontrolelementet under **Publiceringsgrupper** i den venstre navigationsrude viser navnet **Aktivt websted**, arbejder du i oprettelseskonteksten for det aktive websted. **Aktivt websted** er standardnavnet på kontekstkontrollen. Ellers viser kontekstkontrollen navnet på en publiceringsgruppe.

Hvis du vil arbejde i en publiceringsgruppe, skal du skifte til oprettelseskonteksten for publiceringsgruppen. Følg en af disse trin for at indstille publiceringsgruppens kontekst.

- I den venstre navigationsrude skal du vælge kontekstkontrolelementet direkte under **Publiceringsgrupper** og derefter vælge navnet på publiceringsgruppen på listen over de indstillinger, der vises. Kontekstkontrollen omdøbes og viser navnet på publiceringsgruppen.
- Vælg **Publiceringsgrupper** i venstre navigationsrude, og vælg derefter navnet på publiceringsgruppen under **Publiceringsgrupper**. Kontekstkontrollen omdøbes og viser navnet på publiceringsgruppen.

Når du har angivet oprettelseskonteksten for publiceringsgruppen, arbejder du i denne publiceringsgruppes kontekst, når du får vist og redigerer webstedsindhold.

Hvis du vil vende tilbage til standardkonteksten for oprettelse af aktive websteder, skal du vælge kontekstkontrol og derefter vælge **Aktivt websted**.

## <a name="add-pages-or-other-items-to-a-publish-group"></a>Tilføj sider eller andre elementer til en publiceringsgruppe

Når du har valgt en publiceringsgruppes oprettelseskontekst, og kontekstkontrollen i den venstre navigationsrude viser dens navn, kan du oprette indhold på samme måde som i standardkonteksten for aktive websteder. Du kan også tilføje eksisterende sider eller andre elementer fra andre publiceringsgrupper eller fra det aktive websteds kontekst.

Hvis du vil kopiere eksisterende sider til en publiceringsgruppe, skal du følge disse trin.

1. Vælg den oprettelseskontekst, du vil kopiere fra, og vælg derefter **Sider** i venstre navigationsrude.
1. Vælg den side, der skal føjes til en publiceringsgruppe.
1. Vælg **Kopiér til publiceringsgruppe** på kommandolinjen.
1. I dialogboksen **Vælg en publiceringsgruppe** skal du vælge publiceringsgruppen, som siden skal tilføjes til, og derefter vælge **OK**.

Du kan bruge de samme grundlæggende trin til at oprette tilpassede produktsider, URL-adresser, skabeloner, layout, fragmenter og mediebiblioteksaktiver eller til at føje eksisterende elementer af disse typer til en publiceringsgruppe.

## <a name="validate-a-publish-group"></a>Valider en publiceringsgruppe

For at sikre at alle afhængigheder i publiceringsgruppens indhold er opfyldt, og at alle valideringer overføres, kan du køre validering for at identificere eventuelle problemer, der skal løses, før du planlægger en publiceringshandling.

Hvis du vil validere din publiceringsgruppe, før du lægger en tidsplan for den, skal du følge disse trin.

1. Vælg **Publiceringsgrupper** i navigationsruden til venstre.
1. Vælg den publiceringsgruppe, der skal valideres.
1. Vælg **Valider** øverst på kommandolinjen.

Validering køres på alt indhold i publiceringsgruppen. Eventuelle problemer, der vil forhindre en vellykket publiceringshandling, vises i en meddelelsesboks øverst til højre.

> [!NOTE]
> Validering køres altid automatisk, når en publiceringsgruppe er planlagt. Men knappen **Valider** på kommandolinjen er nyttig, fordi den hjælper med at identificere problemer, du skal løse, før du forsøger at planlægge aktiveringen af en publiceringsgruppe.

## <a name="schedule-a-publish-group-to-go-live"></a>Planlæg at aktivere en publiceringsgruppe

Følg disse trin for at planlægge aktiveringen af en publiceringsgruppe på dit websted.

1. Vælg **Publiceringsgrupper** i navigationsruden til venstre.
1. Under **Publiceringsgruppe** skal du vælge den publiceringsgruppe, du ønsker at planlægge.
1. Vælg **Rediger tidsplan** øverst på kommandolinjen. Dialogboksen **Rediger tidsplan** vises.
1. Vælg den dato og det klokkeslæt, hvor publiceringsgruppen skal aktiveres, og vælg derefter **OK**.

Hvis du vil annullere planlægningen af en publiceringsgruppe, skal du følge de samme trin, men vælge **Annuller tidsplanen for publiceringsgruppe** i dialogboksen **Rediger tidsplan**.

> [!NOTE]
> Det kan tage op til et minut eller to at publicere meget store publiceringsgrupper, når deres planlagte tid ankommer. Vær opmærksom på, at en publiceringshandling ikke er øjeblikkelig, og at mindre publiceringsgrupper vil blive publiceret hurtigere.

## <a name="publish-groups-faq"></a>Ofte stillede spørgsmål vedrørende publiceringsgrupper

**Hvor mange elementer kan der være i en publiceringsgruppe?**

I øjeblikket er der en grænse på 2.000 elementer pr. publiceringsgruppe. Vær opmærksom på, at det kan tage adskillige minutter at publicere meget store publiceringsgrupper, når deres planlagte tid ankommer.

**Er publiceringsgrupper ligesom kode-"grene" i terminologi for softwareudvikling?**

Ja og nej. Publiceringsgrupper kan opfattes som forgrenede versioner af dit websted. På den måde opfører de sig som grene. Der sker dog ikke nogen sammenfletning på niveauet for de enkelte elementer. Det element, der udgives sidst, overskriver blot, hvad der fandtes tidligere, og den seneste publiceringshandling erstatter altid tidligere publiceringshandlinger.

**Kan jeg planlægge at aktivere to publiceringsgrupper på samme tid?**

Nr. Af hensyn til ydeevnen og konflikter tvinger systemet dig til at have forskudte planlagte publiceringsgrupper med mindst fem minutters mellemrum.

**Kan jeg bruge publiceringsgrupper til at planlægge flerkanalsadministrationselementer, såsom rabatter og produktopdateringer?**

I øjeblikket understøtter funktionen publiceringsgrupper kun webstedsindhold. Microsoft er dog klar over, at integration med administrationsmerchandisingscenarier kan være værdifuld for koordinering og automatisering af lanceringen af flerkanalskampagner.

## <a name="additional-resources"></a>Yderligere ressourcer

[Metoder til at tilføje indhold](add-manage-content.md)

[Ordliste til sidemodel](page-elements-overview.md)

[Dokumenttilstande og -livscyklus](document-states-overview.md)

[Aktivere og bruge deling på tværs af kanaler](cross-channel-sharing.md)

[Arbejde med moduler](work-with-modules.md)

[Arbejde med fragmenter](work-with-fragments.md)

[Oversigt over skabeloner og layout](templates-layouts-overview.md)

[Tilpasse navigation på webstedet](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
