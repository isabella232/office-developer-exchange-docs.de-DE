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
description: Das addresses-Element stellt eine Auflistung von e-Mail-Adressen für einen Kontakt dar.
ms.openlocfilehash: 9d247f6159d621124ecdd9968ee468ed2b4fe84b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456178"
---
# <a name="emailaddresses"></a><span data-ttu-id="90dcd-103">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="90dcd-103">EmailAddresses</span></span>

<span data-ttu-id="90dcd-104">Das **EmailAddresses** addresses-Element stellt eine Auflistung von e-Mail-Adressen für einen Kontakt dar.</span><span class="sxs-lookup"><span data-stu-id="90dcd-104">The **EmailAddresses** element represents a collection of e-mail addresses for a contact.</span></span> 
  
```xml
<EmailAddresses>
   <Entry/>
</EmailAddresses>
```

 <span data-ttu-id="90dcd-105">**EmailAddressDictionaryType**</span><span class="sxs-lookup"><span data-stu-id="90dcd-105">**EmailAddressDictionaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="90dcd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="90dcd-106">Attributes and elements</span></span>

<span data-ttu-id="90dcd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="90dcd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="90dcd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="90dcd-108">Attributes</span></span>

<span data-ttu-id="90dcd-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="90dcd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="90dcd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="90dcd-110">Child elements</span></span>

|<span data-ttu-id="90dcd-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="90dcd-111">**Element**</span></span>|<span data-ttu-id="90dcd-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="90dcd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90dcd-113">Eintrag (e-mailemail)</span><span class="sxs-lookup"><span data-stu-id="90dcd-113">Entry (EmailAddress)</span></span>](entry-emailaddress.md) <br/> |<span data-ttu-id="90dcd-114">Stellt eine einzelne e-Mail-Adresse für einen Kontakt dar.</span><span class="sxs-lookup"><span data-stu-id="90dcd-114">Represents a single e-mail address for a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="90dcd-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="90dcd-115">Parent elements</span></span>

|<span data-ttu-id="90dcd-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="90dcd-116">**Element**</span></span>|<span data-ttu-id="90dcd-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="90dcd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90dcd-118">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="90dcd-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="90dcd-119">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="90dcd-119">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90dcd-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90dcd-120">Remarks</span></span>

<span data-ttu-id="90dcd-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="90dcd-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="90dcd-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="90dcd-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="90dcd-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="90dcd-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="90dcd-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="90dcd-124">Schema name</span></span>  <br/> |<span data-ttu-id="90dcd-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="90dcd-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="90dcd-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="90dcd-126">Validation file</span></span>  <br/> |<span data-ttu-id="90dcd-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="90dcd-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="90dcd-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="90dcd-128">Can be empty</span></span>  <br/> |<span data-ttu-id="90dcd-129">False</span><span class="sxs-lookup"><span data-stu-id="90dcd-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="90dcd-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90dcd-130">See also</span></span>

- [<span data-ttu-id="90dcd-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="90dcd-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="90dcd-132">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="90dcd-132">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx) 
- [<span data-ttu-id="90dcd-133">Aktualisieren von Kontakten</span><span class="sxs-lookup"><span data-stu-id="90dcd-133">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx) 
- [<span data-ttu-id="90dcd-134">Deleting Contacts</span><span class="sxs-lookup"><span data-stu-id="90dcd-134">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

