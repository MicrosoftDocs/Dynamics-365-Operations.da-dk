---
title: Startside for organisationsadministration
description: Dette emne peger på ressourcer, der kan hjælpe dig med din organisation.
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53a2abad03ab9349834aaafbec572d17d96df9c1
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693996"
---
# <a name="organization-administration-home-page"></a>Startside for organisationsadministration

[!include [banner](../includes/banner.md)]

Dette emne peger på indhold, som kan hjælpe superbrugere og administratorer med at konfigurere systemet til at arbejde glat og effektivt i din organisation og virksomhed.

Meget af indholdet, der vises her, gælder for funktioner i modulet **Virksomhedsadministration**. Der findes dog nogle opgaver, f.eks. oprettelse og brug af en postskabelon, der kan udføres i alle moduler for at hjælpe organisationen med at køre mere effektivt.

## <a name="number-sequences"></a>Nummerserier

Talserier bruges til generering af læselige, entydige identifikatorer for masterdataposter og transaktionsposter, der kræver identifikatorer. En masterdatapost eller transaktionspost, der kræver et id, kaldes en *reference*. Før du kan oprette nye poster til en reference, skal du konfigurere en nummerserie og knytte den til referencen.

- [Oversigt over nummerserier](number-sequence-overview.md)
- [Opret nummerserier ved hjælp af en guide](tasks/set-up-number-sequences-wizard.md) (opgaveguide)
- [Opret nummerserier på individuel basis](tasks/set-up-number-sequences-individual-basis.md) (opgaveguide)

## <a name="organizations"></a>Organisationer

En organisation er en grupper personer, der arbejder sammen for at udføre en forretningsproces eller nå et mål. Organisationshierarkier repræsenterer relationerne mellem de organisationer, som dit firma består af.

Før du opretter organisationer og organisationshierarkier, skal du sørge for at planlægge, hvordan din virksomhed skal udformes. Organisationsmodellen har en væsentlig indvirkning på implementeringen og forretningsprocesserne.

- [Oversigt over organisationer og organisationshierarkier](organizations-organizational-hierarchies.md)
- [Planlægge dit organisationshierarki](plan-organizational-hierarchy.md)
- [Opret et organisationshierarki](tasks/create-organization-hierarchy.md) (opgaveguide)
- [Opret en juridisk enhed](tasks/create-legal-entity.md) (opgaveguide)
- [Opret en driftsenhed](tasks/create-operating-unit.md) (opgaveguide)

## <a name="address-books"></a>Adressekartoteker

Det globale adressekartotek er et centraliseret lager til masterdata, der skal gemmes for alle interne og eksterne personer og organisationer, som virksomheden arbejder sammen med. De data, der er knyttet til partposter, omfatter navn, adresse og kontaktoplysninger for parten.

Når du opretter det globale adressekartotek, kan du oprette yderligere adressekartoteker, du ønsker, som et separat adressekartotek for hvert firma i organisationen eller for hvert forretningsområde.

- [Oversigt over globalt adressekartotek](overview-global-address-book.md)
- [Planen for det globale adressekartotek og andre adressekartoteker](plan-configuration-global-address-book-additional-address-books.md)
- [Konfigurere det globale adressekartotek](tasks/configure-global-address-book.md)
- [Ofte stillede spørgsmål om adressekartoteker](qa-address-books.md)

## <a name="workflow"></a>Arbejdsgang

Arbejdsgang er et system, som du kan bruge til oprette individuelle arbejdsgange eller forretningsprocesser. Når du oprette en arbejdsgang, angiver du, hvordan et dokument "flyder" eller bevæger sig gennem systemet, ved at vise, hvem der skal udføre en opgave, træffe en beslutning eller godkende et dokument.

- [Oversigt over arbejdsgangssystem](overview-workflow-system.md)
- [Arbejdsgangselementer](workflow-elements.md)
- [Handlinger i godkendelsesprocesser i arbejdsgang](workflow-actions.md)
- [Oversigt over oprettelse af arbejdsgange](create-workflow.md)

## <a name="electronic-signatures"></a>Elektroniske signaturer

En elektronisk signatur bekræfter identiteten på en person, som skal starte eller godkende en computerproces. I nogle brancher er en elektronisk signatur lige så juridisk bindende som en håndskrevet signatur. Elektroniske signaturer er et lovmæssigt krav i adskillige regulerede brancher som f.eks. lægemiddelsektoren, fødevareindustrien samt luftfart og forsvar.

Du kan bruge elektroniske signaturer til kritiske forretningsprocesser. Nogle processer har indbyggede funktioner til elektronisk signatur. Du kan også oprette tilpassede signaturkrav for enhver databasetabel og ethvert felt.

- [Oversigt over elektroniske signaturer](electronic-signature-overview.md)
- [Konfigurer elektroniske signaturer](tasks/set-up-electronic-signatures.md) (opgaveguide)

## <a name="case-management"></a>Sagsstyring

Ved at planlægge, spore og analysere sager kan du lettere finde frem til effektive løsninger, der også kan bruges til andre tilsvarende sager. Hvis medarbejdere i kundeservice eller personaleafdelingen f.eks. opretter sager, kan de finde videnartikler med oplysninger om, hvordan de kan arbejde med en sag eller løse den mere effektivt.

- [Oversigt over sagsstyring](cases.md)
- [Planlæg sagssikkerhed, sagsprocesser og sagskategorier](plan-case-management.md)

## <a name="record-templates"></a>Postskabeloner

Med postskabeloner kan du hurtigere oprette poster. Du kan oprette en postskabelon, så feltværdier, som bruges ofte, ikke behøver at angives eksplicit for hver ny post.

- [Oversigt over postskabeloner](record-templates.md)
- [Oprette en postskabelon for at lette dataindtastning](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (opgaveguide)
- [Brug postskabelon til at oprette en ny post](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (opgaveguide)

## <a name="general-organization-administration"></a>Generel virksomhedsadministration

- [Rediger banneret eller logoet](../get-started/tasks/change-banner-or-logo.md) (opgaveguide)
- [Konfigurere dokumentstyring](configure-document-management.md)
- [Konfigurere og sende mail](configure-email.md)
- [Data om dato/klokkeslæt og tidszoner](date-time-zones.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]