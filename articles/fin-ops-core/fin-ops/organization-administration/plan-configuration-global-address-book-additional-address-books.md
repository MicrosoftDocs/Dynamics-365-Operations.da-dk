---
title: Plan for at det globale adressekartotek og andre adressekartoteker
description: I dette emne beskrives de overvejelser og de beslutninger, du skal foretage i planlægningsprocessen.
author: msftbrking
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1d3a476a183453f170dae9b812949822ea60edd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747603"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a><span data-ttu-id="61bcf-103">Planen for det globale adressekartotek og andre adressekartoteker</span><span class="sxs-lookup"><span data-stu-id="61bcf-103">Plan for the global address book and other address books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61bcf-104">I dette emne beskrives de overvejelser og de beslutninger, du skal foretage i planlægningsprocessen, før du opsætter og konfigurerer det globale adressekartotek og eventuelle supplerende adressekartoteker.</span><span class="sxs-lookup"><span data-stu-id="61bcf-104">This topic describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books.</span></span> <span data-ttu-id="61bcf-105">Nogle af afgørelser kræver, at du bekræfter de beslutninger, der er foretaget på andre områder for produktet, f.eks. organisationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="61bcf-105">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

## <a name="global-address-book"></a><span data-ttu-id="61bcf-106">Globalt adressekartotek</span><span class="sxs-lookup"><span data-stu-id="61bcf-106">Global address book</span></span>

<span data-ttu-id="61bcf-107">Før du begynder at arbejde med det globale adressekartotek, skal du bestemme standardværdierne for det.</span><span class="sxs-lookup"><span data-stu-id="61bcf-107">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="61bcf-108">Disse værdier bruges derefter til eventuelle yderligere adressekartoteker, du opretter.</span><span class="sxs-lookup"><span data-stu-id="61bcf-108">These default values are then used for any additional address books that you create.</span></span>

<span data-ttu-id="61bcf-109">**Beslutninger**</span><span class="sxs-lookup"><span data-stu-id="61bcf-109">**Decisions**</span></span>

- <span data-ttu-id="61bcf-110">I hvilken rækkefølge skal navne vises i, for partposter af typen **Person**?</span><span class="sxs-lookup"><span data-stu-id="61bcf-110">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="61bcf-111">Én sekvens er f.eks. efternavn, mellemnavn, fornavn.</span><span class="sxs-lookup"><span data-stu-id="61bcf-111">For example, one sequence is last name, middle name, first name.</span></span>
- <span data-ttu-id="61bcf-112">Skal partposter slettes fra adressekartoteket, når rolleposten slettes?</span><span class="sxs-lookup"><span data-stu-id="61bcf-112">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="61bcf-113">Hvis f.eks. en kundepost slettes, skal partposten også slettes?</span><span class="sxs-lookup"><span data-stu-id="61bcf-113">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
- <span data-ttu-id="61bcf-114">Når der oprettes en ny post, skal brugerne så have besked, hvis der findes en dubletpost i det globale adressekartotek?</span><span class="sxs-lookup"><span data-stu-id="61bcf-114">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
- <span data-ttu-id="61bcf-115">Skal DUNS-nummeret (Data Universal Numbering System) inkluderes i oplysningerne om en partpost?</span><span class="sxs-lookup"><span data-stu-id="61bcf-115">Should the Data Universal Numbering System (DUNS) number be included in a party record's information?</span></span>
- <span data-ttu-id="61bcf-116">Hvis DUNS-nummeret er medtaget i en partpost, bør tallets entydighed så kontrolleres?</span><span class="sxs-lookup"><span data-stu-id="61bcf-116">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
- <span data-ttu-id="61bcf-117">Når en partpost oprettes i det globale adressekartotek, vil du så have en standard for parttype, person eller organisation?</span><span class="sxs-lookup"><span data-stu-id="61bcf-117">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
- <span data-ttu-id="61bcf-118">Hvilke brugerroller skal have adgang til private adresser og kontaktoplysninger for partposten?</span><span class="sxs-lookup"><span data-stu-id="61bcf-118">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="61bcf-119">Yderligere adressekartoteker</span><span class="sxs-lookup"><span data-stu-id="61bcf-119">Additional address books</span></span>

<span data-ttu-id="61bcf-120">Når du opretter det globale adressekartotek, kan du oprette yderligere adressekartoteker, du ønsker, som et separat adressekartotek for hvert firma i organisationen eller for hvert forretningsområde.</span><span class="sxs-lookup"><span data-stu-id="61bcf-120">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="61bcf-121">Fabrikam er f.eks. en international organisation, der har flere firmaer og flere forretningsområder.</span><span class="sxs-lookup"><span data-stu-id="61bcf-121">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="61bcf-122">Fabrikam planlægger at oprette et adressekartotek for hvert forretningsområde.</span><span class="sxs-lookup"><span data-stu-id="61bcf-122">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="61bcf-123">Til forretningsområder, der findes på mere end én lokalitet, f.eks. trykluftsværktøj, planlægger Fabrikam at oprette et adressekartotek for hver enkelt lokalitet.</span><span class="sxs-lookup"><span data-stu-id="61bcf-123">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="61bcf-124">Chris, it-leder hos Fabrikam, har oprettet følgende liste over adressekartoteker, der kræves.</span><span class="sxs-lookup"><span data-stu-id="61bcf-124">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="61bcf-125">Denne liste beskriver også de partposter, som hver enkelt adressekartotek skal indeholde.</span><span class="sxs-lookup"><span data-stu-id="61bcf-125">This list also describes the party records that each address book must include.</span></span>

- <span data-ttu-id="61bcf-126">**Offentlig sektor-kontrakter (OffSK)** – partposter for alle parter, der er involveret i de kontrakter med den offentlige sektor, som Fabrikam har.</span><span class="sxs-lookup"><span data-stu-id="61bcf-126">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="61bcf-127">**Privat sektor-kontrakter (PriSK)** – partposter for alle parter, der er involveret i de kontrakter med den private sektor, som Fabrikam har.</span><span class="sxs-lookup"><span data-stu-id="61bcf-127">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="61bcf-128">**Elektroniske værktøjer (EV)** – partposter for alle parter, der er involveret i køb eller salg af elektroniske værktøjer, eller som på anden måde har noget at gøre med de elektroniske værktøjer, der stilles til rådighed af eller købes til Fabrikam i Fabrikams firma i Japan.</span><span class="sxs-lookup"><span data-stu-id="61bcf-128">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="61bcf-129">**Trykluftsværktøj (TVJPN)** – partposter for alle parter, der er involveret i køb eller salg af trykluftsværktøj, eller som på anden måde har noget at gøre med det trykluftsværktøj, der stilles til rådighed af eller købes til Fabrikam i Fabrikams firma i Japan.</span><span class="sxs-lookup"><span data-stu-id="61bcf-129">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="61bcf-130">**Trykluftsværktøj (TVUSA)** – partposter for alle parter, der er involveret i køb eller salg af trykluftsværktøj, eller som på anden måde har noget at gøre med det trykluftsværktøj, der stilles til rådighed af eller købes til Fabrikam i Fabrikams firma i USA.</span><span class="sxs-lookup"><span data-stu-id="61bcf-130">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="61bcf-131">**Beslutning:**</span><span class="sxs-lookup"><span data-stu-id="61bcf-131">**Decision:**</span></span>

- <span data-ttu-id="61bcf-132">Hvor mange yderligere adressekartoteker vil du oprette?</span><span class="sxs-lookup"><span data-stu-id="61bcf-132">How many additional address books will you create?</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]