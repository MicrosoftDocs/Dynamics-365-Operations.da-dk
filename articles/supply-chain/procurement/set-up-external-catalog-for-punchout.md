---
title: "Konfigurere et eksternt katalog til PunchOut e-indkøb"
description: "Dette emne beskriver brugen af et eksternt katalog eller punchout-katalog til at indsamle oplysninger tilbud fra en leverandør og føje dem til en rekvisition."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 2892feff0ab8845515543af1a71d8f9642113726
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---

# <a name="set-up-an-external-catalog-for-punchout-eprocurement"></a>Konfigurere et eksternt katalog til PunchOut e-indkøb

[!include [banner](../includes/banner.md)]

Ved hjælp af det eksterne katalog kan du sikre, at oplysningerne om produkt og pris, som du derefter behandler i Dynamics 365 for Finance and Operations, juli 2017, er nøjagtige og ajourførte. Rekvisitionen kan derefter godkendes og konverteres til en indkøbsordre, og en ordre kan afgives hos leverandøren.

Når det eksterne katalog er konfigureret, og medarbejderen forbereder en rekvisition, er der mulighed for at omdirigere til et eksternt websted, det eksterne katalog, og returnere indkøbskurven, der er oprettet på det eksterne websted. Denne meddelelse er baseret på cXML-protokollen og skal være konfigureret mellem systemerne for den købende og den sælgende organisation.

For at konfigurere kommunikationen skal din leverandør give dig oplysninger til brug i det konfigurationen af det eksterne katalog, f.eks. identitet, køberfirmaets domæne, f.eks. "DUNS" og "DUNS-nummer", legitimationsoplysninger og URL-adressen til leverandørens katalog.

## <a name="setting-up-an-external-catalog"></a>Konfiguration af et eksternt katalog

Det eksterne katalog skal gøre det muligt for en medarbejder, der angiver en indkøbsrekvisition, at blive omdirigeret til et eksternt websted for at vælge produkter. De produkter, som medarbejderen vælger fra det eksterne katalog, returneres til Dynamics 365 for Finance and Operations med opdaterede prisoplysninger, og herfra kan de kan føjes til indkøbsrekvisitionen. Hensigten er ikke at give medarbejdere mulighed for at afgive en ordre på det eksterne websted. Når du opretter det eksterne katalog, skal du kontrollere, at formålet med det websted, der kan tilgås af det eksterne katalog, er at indsamle tilbudsoplysninger og ikke at afgive en faktisk ordre.

### <a name="to-set-up-an-external-vendor-catalog-complete-the-following-tasks"></a>Hvis du vil konfigurere et eksternt kreditorkatalog, skal du fuldføre følgende opgaver:

1. Konfigurer et indkøbskategorihierarki. Du kan finde flere oplysninger under [Konfigurere politikker for indkøbskategorihierarkier](tasks/set-up-policies-procurement-category-hierarchies.md).
2. Registrer leverandøren i Finance and Operations. Før du kan oprette konfigurationer for at få adgang til en ekstern leverandørs katalog, skal du konfigurere leverandøren og leverandørens kontakt i Microsoft Dynamics 365. Det eksterne katalogs leverandør skal også føjes til den valgte indkøbskategori. Du kan finde flere oplysninger om registrering af leverandører i Microsoft Dynamics 365 under [Administrere brugere af kreditorsamarbejde](manage-vendor-collaboration-users.md). Du kan finde flere oplysninger om at tildele leverandører en indkøbskategori under [Godkend leverandører til bestemte indkøbskategorier](tasks/approve-vendors-specific-procurement-categories.md).
3. Sørg for, at de måleenheder og den valuta, som leverandøren bruger, er konfigureret. Du kan finde oplysninger om, hvordan du opretter en måleenhed, i [Administrere måleenheder](../pim/tasks/manage-unit-measure.md).
4. Konfigurer det eksterne kreditorkatalog ved hjælp af kravene til leverandørens eksterne katalogwebsted. Du kan finde yderligere oplysninger om denne opgave i [Konfigurere det eksterne leverandørkatalog](#configure-the-external-vendor-catalog).
5. Test konfigurationerne af leverandørens eksterne katalog for at kontrollere, at indstillingerne er gyldige, og at du kan få adgang til leverandørens eksterne katalog. Brug handlingen **Valider indstillinger** til at validere den meddelelse om konfigurationsanmodning, du har defineret. Denne meddelelse bør medføre, at leverandørens eksterne katalogwebsted åbnes i et browservindue. Under valideringen kan du ikke bestille varer og tjenester fra leverandøren. Hvis du vil bestille varer og tjenester, skal du have adgang til leverandørkataloget fra en indkøbsrekvisition.
6. Aktivér det eksterne katalog ved hjælp af knappen **Aktivér katalog** på siden **Eksterne kataloger**. Det eksterne katalog skal aktiveres, før medarbejdere kan bruge det. Du kan deaktivere det eksterne katalog når som helst.


## <a name="configure-the-external-vendor-catalog"></a>Konfigurere det eksterne leverandørkatalog

Dette afsnit indeholder flere detaljer om opgave 4 i forrige afsnit.

1. Angiv et navn og en beskrivelse for leverandørens eksterne katalog. Det navn, du angiver, vises i indkøbsvognen, der repræsenterer det eksterne katalog, der vises for medarbejdere, som opretter en rekvisition. Medarbejderne kan klikke på indkøbsvognen for at åbne kataloget på leverandørens eksterne katalogwebsted.
2. Tilføj et billede ved hjælp af handlingen **Eksternt katalogbillede**. Billedet vises på indkøbsvognen, der repræsenterer det eksterne katalog, der vises for medarbejdere, som opretter en rekvisition. Bemærk, at billedets bredde og højde skal være ens. Ellers vises billedet ikke korrekt.
3. Vælg, om leverandørens eksterne katalogwebsted skal vises i det samme browservindue, hvor medarbejderen har oprettet rekvisitionen, eller om det åbnes i et nyt vindue.
4. Vælg leverandøren for kataloget. På listen **Juridiske enheder** er der en række for hver juridiske enhed, hvor leverandøren er oprettet. Hvis brugere skal kunne anmode om produkter direkte fra leverandørkataloget i visse juridiske enheder, men ikke andre, kan du bruge knappen **Udeluk adgang** eller **Tillad adgang** for hver juridiske enhed, hvor kataloget skal være eller ikke være tilgængeligt.
5. I feltet **Standardudløb (dage)** skal du angive antallet af dage, hvor tilbuddet fra det eksterne katalog er gyldigt og kan bruges til køb hos den eksterne leverandør. Når et tilbud er oprettet og hentet fra leverandørens eksterne katalogwebsted, er tilbuddet gyldigt med virkning fra den aktuelle systemdato og forbliver gyldigt i det antal dage, du angiver i dette felt.
6. Klik på knappen **Tilføj** for at starte tilknytning af indkøbskategorier til det eksterne katalog. Vælg derefter en kategori på listen Kategorinavn. Listen over kategorier er et undersæt af indkøbskategorier, som leverandøren er knyttet til i de juridiske enheder, der er konfigureret for leverandøren.
[!NOTE]
Indkøbspolitikker bruges til at tillade eller begrænse adgang til kategorier for den juridiske indkøbsenhed eller modtagende driftsenhed. Punchout til et eksternt katalog kræver, at der er tilladt adgang til mindst en af de indkøbskategorier, som er knyttet til kataloget.
7. Konfigurer cXML-meddelelsen om opsætningsanmodning, der skal sendes til leverandøren. Det automatisk genererede meddelelsesformat er den minimale skabelonen, der kræves for at starte en session. Udfyld værdier for koderne.

Du kan til enhver tid genindlæse den systemgenererede meddelelsesskabelon ved at klikke på **Gendan meddelelsesformat**. Bemærk, at hvis du gendanner meddelelsesformatet, bliver den aktuelle meddelelse erstattet af det automatisk genererede meddelelsesformat, som har tomme koder.

### <a name="cxml-setup-message"></a>cXML-konfigurationsmeddelelse
Nedenfor kan du se en beskrivelse af de koder, der er inkluderet i skabelonen:

| Felt | Betegnelse | 
|---------|---------|
|< Header >< From >< Credential domain=”” >|Domænet for indkøbsfirmaet.|
|< Header >< From >< Credential>< Identity >< /Identity > | Indkøbsfirmaets identitet.|
|< Header >< To >< Credential domain=”” > | Domænet for leverandørfirmaet.|
|< Header >< To >< Credential>< Identity >< /Identity> | Leverandørfirmaets identitet.|
|< Header >< Sender >< Credential domain=”” > | Domænet for indkøbsfirmaet.|
|< Header >< Sender >< Credential >< Identity >< /Identity> | Indkøbsfirmaets identitet.|
|< Header >< Sender >< Credential >< SharedSecret >< /SharedSecret >|Den delte hemmelighed for køberens firma.|
|< Request deploymentMode=”” >|Test- eller produktionsinstallationen.|
|< Request >< PunchOutSetupRequest >< SupplierSetup >< URL >< /URL>|URL-adressen på leverandørens punchout-slutpunkt.|

### <a name="extrinsic-elements"></a>Ydre elementer

Et ydre element er yderligere oplysninger, f.eks. et brugernavn, der er baseret på en bruger, der stempler ud. Det ydre element angives, når udstempling forekommer, og det kan sendes i meddelelsen om konfigurationsanmodning.
Leverandøren kan have et behov for at modtage et ydre element i opsætning af anmodningen. I så fald skal du føje det ydre element til listen over ydre elementer i sektionen **Meddelelsesformat** på siden **Eksternt katalog**. Angiv et navn for det ydre element, så leverandøren kan genkende det og tilknytte en værdi. De mulige værdier er: brugernavn, brugermail eller en tilfældig værdi.
Yderligere oplysninger om cXML-protokollen finder du i http://cxml.org/.

## <a name="post-back-message"></a>Tilbagesendelsesmeddelelse
Tilbagesendelsesmeddelelsen er den meddelelse, der modtages fra leverandøren, når brugeren tjekker ud fra det eksterne websted og vender tilbage til Finance and Operations. Tilbagesendelsesmeddelelser kan ikke konfigureres. Meddelelserne er baseret på definitionen af cXML-protokollen. Her er de oplysninger, der kan være en del af tilbagesendelsesmeddelelsen, der modtages på en rekvisitionslinje:

| Meddelelse modtaget fra leverandør | Kopieret til rekvisitionslinje i Finance and Operations|
|------------------------------|----------------------------------------------------------|
|< ItemIn quantity=”” > |Mængde|
|< ItemIn>< ItemID >< SupplierPartID >< /SupplierPartID >|Eksternt vare-id|
|< ItemDetail>< UnitPrice >< Money currency=”” >| Valuta|
|< ItemDetail >< UnitPrice >< Money >< /Money >| Enhedspris|
|< ItemDetail >< Description ShortName=”” >|Produktnavn|
|< ItemDetail >< Description >< /Description >|Inkluderet i beskrivelsen af varen. Produktnavn, hvis ShortName ikke er angivet.|
|< ItemDetail >< UnitOfMeasure >< /UnitOfMeasure >|Enhed|
|< ItemDetail >< Classification >< /Classification >|Inkluderet i varebeskrivelse|
|< ItemDetail >< Classification domain=”” >|Inkluderet i varebeskrivelse|

## <a name="delete-an-external-catalog"></a>Slette et eksternt katalog
Slet et eksternt katalog med handlingen Slet på siden.

Hvis der er anmodet om et produkt fra det eksterne kreditorkatalog, kan det eksterne kreditorkatalog ikke slettes. I stedet er status for det eksterne leverandørkatalog sat til inaktiv. Hvis du vil fjerne adgangen til webstedet for det eksterne leverandørkatalog uden at slette det, kan du ændre status for det eksterne katalog til Inaktiv.


