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
description: Das FilterHtmlContent-Element gibt an, ob potenziell unsichere HTML-Inhalte aus eines Elements oder einer Anlage gefiltert wird.
ms.openlocfilehash: db181eff9586061d728a5e4ef55a78f4955b5713
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758427"
---
# <a name="filterhtmlcontent"></a><span data-ttu-id="b3261-103">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="b3261-103">FilterHtmlContent</span></span>

<span data-ttu-id="b3261-104">Das **FilterHtmlContent** -Element gibt an, ob potenziell unsichere HTML-Inhalte aus eines Elements oder einer Anlage gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="b3261-104">The **FilterHtmlContent** element specifies whether potentially unsafe HTML content is filtered from an item or attachment.</span></span> 
  
```xml
<FilterHtmlContent>true or false</FilterHtmlContent>
```

 <span data-ttu-id="b3261-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="b3261-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b3261-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b3261-106">Attributes and elements</span></span>

<span data-ttu-id="b3261-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b3261-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b3261-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b3261-108">Attributes</span></span>

<span data-ttu-id="b3261-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b3261-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b3261-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b3261-110">Child elements</span></span>

<span data-ttu-id="b3261-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b3261-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b3261-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b3261-112">Parent elements</span></span>

|<span data-ttu-id="b3261-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b3261-113">**Element**</span></span>|<span data-ttu-id="b3261-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b3261-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3261-115">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="b3261-115">AttachmentShape</span></span>](attachmentshape.md) <br/> | <span data-ttu-id="b3261-116">Bezeichnet die zusätzliche Eigenschaften in einer Antwort auf eine Anforderung [GetAttachment](getattachment.md) zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b3261-116">Identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/><br/>  <span data-ttu-id="b3261-117">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="b3261-117">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/GetAttachment/AttachmentShape` <br/> |
|[<span data-ttu-id="b3261-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="b3261-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="b3261-119">Identifiziert die Elementeigenschaften und den Inhalt in einer Antwort GetItem, FindItem oder SyncFolderItems aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="b3261-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/> <br/> <span data-ttu-id="b3261-120">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="b3261-120">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/GetItem/ItemShape`<br/> <br/>  `/FindItem/ItemShape`<br/> <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b3261-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="b3261-121">Text value</span></span>

<span data-ttu-id="b3261-122">Dieses Element kann **true** oder **false**sein.</span><span class="sxs-lookup"><span data-stu-id="b3261-122">This element can be either **true** or **false**.</span></span> <span data-ttu-id="b3261-123">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="b3261-123">The default value is **false**.</span></span> <span data-ttu-id="b3261-124">Dies ist ein Boolean-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="b3261-124">This is a Boolean data type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b3261-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b3261-125">Remarks</span></span>

<span data-ttu-id="b3261-126">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="b3261-126">This element is optional.</span></span>
  
<span data-ttu-id="b3261-127">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, der Exchange-Server, mit die Clientzugriffs-Serverrolle installiert ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3261-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b3261-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b3261-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3261-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="b3261-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b3261-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b3261-130">Schema Name</span></span>  <br/> |<span data-ttu-id="b3261-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b3261-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="b3261-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b3261-132">Validation File</span></span>  <br/> |<span data-ttu-id="b3261-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b3261-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b3261-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b3261-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="b3261-135">False</span><span class="sxs-lookup"><span data-stu-id="b3261-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b3261-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3261-136">See also</span></span>

- [<span data-ttu-id="b3261-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b3261-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

