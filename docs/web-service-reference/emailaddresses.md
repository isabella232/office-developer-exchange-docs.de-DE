---
title: EmailAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EmailAddresses
api_type:
- schema
ms.assetid: fd4d773c-f7dc-4a04-9025-e772d7a45fdf
description: Das Element EmailAddresses stellt eine Sammlung von E-mail-Adressen für einen Kontakt.
ms.openlocfilehash: 2eddb68ecffd8f61a2fbb775d8013433d715db1a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758177"
---
# <a name="emailaddresses"></a><span data-ttu-id="69b61-103">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="69b61-103">EmailAddresses</span></span>

<span data-ttu-id="69b61-104">Das Element **EmailAddresses** stellt eine Sammlung von E-mail-Adressen für einen Kontakt.</span><span class="sxs-lookup"><span data-stu-id="69b61-104">The **EmailAddresses** element represents a collection of e-mail addresses for a contact.</span></span> 
  
```xml
<EmailAddresses>
   <Entry/>
</EmailAddresses>
```

 <span data-ttu-id="69b61-105">**EmailAddressDictionaryType**</span><span class="sxs-lookup"><span data-stu-id="69b61-105">**EmailAddressDictionaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="69b61-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="69b61-106">Attributes and elements</span></span>

<span data-ttu-id="69b61-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="69b61-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69b61-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="69b61-108">Attributes</span></span>

<span data-ttu-id="69b61-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="69b61-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="69b61-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="69b61-110">Child elements</span></span>

|<span data-ttu-id="69b61-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="69b61-111">**Element**</span></span>|<span data-ttu-id="69b61-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="69b61-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69b61-113">Eintrag (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="69b61-113">Entry (EmailAddress)</span></span>](entry-emailaddress.md) <br/> |<span data-ttu-id="69b61-114">Stellt eine einzelne e-Mail-Adresse für einen Kontakt.</span><span class="sxs-lookup"><span data-stu-id="69b61-114">Represents a single e-mail address for a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="69b61-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="69b61-115">Parent elements</span></span>

|<span data-ttu-id="69b61-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="69b61-116">**Element**</span></span>|<span data-ttu-id="69b61-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="69b61-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69b61-118">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="69b61-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="69b61-119">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="69b61-119">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69b61-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69b61-120">Remarks</span></span>

<span data-ttu-id="69b61-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="69b61-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69b61-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="69b61-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69b61-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="69b61-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="69b61-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="69b61-124">Schema name</span></span>  <br/> |<span data-ttu-id="69b61-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="69b61-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="69b61-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="69b61-126">Validation file</span></span>  <br/> |<span data-ttu-id="69b61-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="69b61-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="69b61-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="69b61-128">Can be empty</span></span>  <br/> |<span data-ttu-id="69b61-129">False</span><span class="sxs-lookup"><span data-stu-id="69b61-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69b61-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69b61-130">See also</span></span>

- [<span data-ttu-id="69b61-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="69b61-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="69b61-132">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="69b61-132">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx) 
- [<span data-ttu-id="69b61-133">Aktualisierung von Kontakten</span><span class="sxs-lookup"><span data-stu-id="69b61-133">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx) 
- [<span data-ttu-id="69b61-134">Deleting Contacts</span><span class="sxs-lookup"><span data-stu-id="69b61-134">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

