---
title: IncludeMimeContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IncludeMimeContent
api_type:
- schema
ms.assetid: 3f3c2300-55cd-41c0-900e-b470b290d52f
description: Das IncludeMimeContent-Element gibt an, ob der Inhalt Multipurpose Internet Mail Extensions (MIME) eines Elements oder die Anlage in der Antwort zurückgegeben wird.
ms.openlocfilehash: ddd6988be93231ac7c574a2e19c9ba4b562c7d0e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829903"
---
# <a name="includemimecontent"></a><span data-ttu-id="76885-103">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="76885-103">IncludeMimeContent</span></span>

<span data-ttu-id="76885-104">Das **IncludeMimeContent** -Element gibt an, ob der Inhalt Multipurpose Internet Mail Extensions (MIME) eines Elements oder die Anlage in der Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="76885-104">The **IncludeMimeContent** element specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item or attachment is returned in the response.</span></span> 
  
```xml
<IncludeMimeContent>true or false</IncludeMimeContent>
```

 <span data-ttu-id="76885-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="76885-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="76885-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="76885-106">Attributes and elements</span></span>

<span data-ttu-id="76885-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="76885-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76885-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="76885-108">Attributes</span></span>

<span data-ttu-id="76885-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="76885-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="76885-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="76885-110">Child elements</span></span>

<span data-ttu-id="76885-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="76885-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="76885-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="76885-112">Parent elements</span></span>

|<span data-ttu-id="76885-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="76885-113">**Element**</span></span>|<span data-ttu-id="76885-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76885-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76885-115">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="76885-115">AttachmentShape</span></span>](attachmentshape.md) <br/> | <span data-ttu-id="76885-116">Bezeichnet die zusätzliche Eigenschaften in einer Antwort auf eine Anforderung [GetAttachment](getattachment.md) zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="76885-116">Identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/> <br/> <span data-ttu-id="76885-117">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="76885-117">The following is the XPath expression to this element:</span></span>  <br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
|[<span data-ttu-id="76885-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="76885-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="76885-119">Identifiziert die Elementeigenschaften und den Inhalt in einer Antwort GetItem, FindItem oder SyncFolderItems aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="76885-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/> <br/> <span data-ttu-id="76885-120">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="76885-120">The following are the XPath expressions to this element:</span></span><br/>  <br/>  `/GetItem/ItemShape` <br/><br/>  `/FindItem/ItemShape` <br/><br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="76885-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="76885-121">Text value</span></span>

<span data-ttu-id="76885-122">Dieses Element kann **true** oder **false**sein.</span><span class="sxs-lookup"><span data-stu-id="76885-122">This element can be either **true** or **false**.</span></span> <span data-ttu-id="76885-123">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="76885-123">The default value is **false**.</span></span> <span data-ttu-id="76885-124">Dies ist ein Boolean-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="76885-124">This is a Boolean data type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="76885-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="76885-125">Remarks</span></span>

<span data-ttu-id="76885-126">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="76885-126">This element is optional.</span></span>
  
<span data-ttu-id="76885-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="76885-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="76885-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="76885-128">Example</span></span>

<span data-ttu-id="76885-129">Im folgenden Beispiel wird eine Anforderung gezeigt, wie das **IncludeMimeContent** -Element festlegen.</span><span class="sxs-lookup"><span data-stu-id="76885-129">The following example of a request demonstrates a how to set the **IncludeMimeContent** element.</span></span> 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape>
        <t:IncludeMimeContent>true</t:IncludeMimeContent>
        <t:BodyType>Best</t:BodyType>
      </AttachmentShape>
      <AttachmentIds>
        <t:AttachmentId Id="ASkAS="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="76885-130">Das Anlage-Id-Attribut werden abgeschnitten, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="76885-130">The attachment Id attribute is truncated to preserve readability.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="76885-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="76885-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76885-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="76885-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="76885-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="76885-133">Schema Name</span></span>  <br/> |<span data-ttu-id="76885-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="76885-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="76885-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="76885-135">Validation File</span></span>  <br/> |<span data-ttu-id="76885-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="76885-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="76885-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="76885-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="76885-138">False</span><span class="sxs-lookup"><span data-stu-id="76885-138">False</span></span>  <br/> |
   

