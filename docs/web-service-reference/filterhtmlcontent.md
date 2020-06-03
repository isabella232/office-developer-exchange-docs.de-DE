---
title: FilterHtmlContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FilterHtmlContent
api_type:
- schema
ms.assetid: 2f9358a0-de1d-4544-9aa0-d9f6519f3b5f
description: Das FilterHtmlContent-Element gibt an, ob potenziell unsicherer HTML-Inhalt von einem Element oder einer Anlage gefiltert wird.
ms.openlocfilehash: 28e3be86b550c3f330fbb6846b64732b5674304d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462675"
---
# <a name="filterhtmlcontent"></a><span data-ttu-id="31763-103">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="31763-103">FilterHtmlContent</span></span>

<span data-ttu-id="31763-104">Das **FilterHtmlContent** -Element gibt an, ob potenziell unsicherer HTML-Inhalt von einem Element oder einer Anlage gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="31763-104">The **FilterHtmlContent** element specifies whether potentially unsafe HTML content is filtered from an item or attachment.</span></span> 
  
```xml
<FilterHtmlContent>true or false</FilterHtmlContent>
```

 <span data-ttu-id="31763-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="31763-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="31763-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="31763-106">Attributes and elements</span></span>

<span data-ttu-id="31763-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="31763-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31763-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="31763-108">Attributes</span></span>

<span data-ttu-id="31763-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="31763-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="31763-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="31763-110">Child elements</span></span>

<span data-ttu-id="31763-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="31763-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="31763-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="31763-112">Parent elements</span></span>

|<span data-ttu-id="31763-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="31763-113">**Element**</span></span>|<span data-ttu-id="31763-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="31763-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31763-115">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="31763-115">AttachmentShape</span></span>](attachmentshape.md) <br/> | <span data-ttu-id="31763-116">Identifiziert zusätzliche Eigenschaften, die in einer Antwort auf eine [GetAttachment](getattachment.md) -Anforderung zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="31763-116">Identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/><br/>  <span data-ttu-id="31763-117">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="31763-117">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/GetAttachment/AttachmentShape` <br/> |
|[<span data-ttu-id="31763-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="31763-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="31763-119">Identifiziert die Elementeigenschaften und Inhalte, die in einer GetItem-, FindItem-oder SyncFolderItems-Antwort enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="31763-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/> <br/> <span data-ttu-id="31763-120">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="31763-120">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/GetItem/ItemShape`<br/> <br/>  `/FindItem/ItemShape`<br/> <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="31763-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="31763-121">Text value</span></span>

<span data-ttu-id="31763-122">Dieses Element kann entweder **true** oder **false**sein.</span><span class="sxs-lookup"><span data-stu-id="31763-122">This element can be either **true** or **false**.</span></span> <span data-ttu-id="31763-123">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="31763-123">The default value is **false**.</span></span> <span data-ttu-id="31763-124">Dies ist ein boolescher Datentyp.</span><span class="sxs-lookup"><span data-stu-id="31763-124">This is a Boolean data type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31763-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31763-125">Remarks</span></span>

<span data-ttu-id="31763-126">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="31763-126">This element is optional.</span></span>
  
<span data-ttu-id="31763-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server mit installierter Client Zugriffs-Server Rolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="31763-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31763-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="31763-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31763-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="31763-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="31763-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="31763-130">Schema Name</span></span>  <br/> |<span data-ttu-id="31763-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="31763-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="31763-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="31763-132">Validation File</span></span>  <br/> |<span data-ttu-id="31763-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="31763-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="31763-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="31763-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="31763-135">False</span><span class="sxs-lookup"><span data-stu-id="31763-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31763-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31763-136">See also</span></span>

- [<span data-ttu-id="31763-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="31763-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

