---
title: ItemShape
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemShape
api_type:
- schema
ms.assetid: c5604161-bbc0-40bc-ad75-ff7e837d745f
description: Das ItemShape-Element identifiziert eine Reihe von Eigenschaften in einem GetItem Operation, FindItem Vorgang oder SyncFolderItems Vorgangsantwort zurückgegeben werden sollen.
ms.openlocfilehash: 95174a85a8fa05cb2612e1289d46c8db32b6e052
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830191"
---
# <a name="itemshape"></a><span data-ttu-id="329eb-103">ItemShape</span><span class="sxs-lookup"><span data-stu-id="329eb-103">ItemShape</span></span>

<span data-ttu-id="329eb-104">Das **ItemShape** -Element identifiziert eine Reihe von Eigenschaften in einer Antwort [GetItem Operation](getitem-operation.md), [FindItem Vorgang](finditem-operation.md)oder [SyncFolderItems Vorgang](syncfolderitems-operation.md) zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="329eb-104">The **ItemShape** element identifies a set of properties to return in a [GetItem operation](getitem-operation.md), [FindItem operation](finditem-operation.md), or [SyncFolderItems operation](syncfolderitems-operation.md) response.</span></span> 
  
```XML
<ItemShape>
   <BaseShape/>
   <IncludeMimeContent/>
   <BodyType/>
   <FilterHtmlContent/>
   <ConvertHtmlCodePageToUTF8/>
   <AdditionalProperties/>
</ItemShape>
```

 <span data-ttu-id="329eb-105">**ItemResponseShapeType**</span><span class="sxs-lookup"><span data-stu-id="329eb-105">**ItemResponseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="329eb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="329eb-106">Attributes and elements</span></span>

<span data-ttu-id="329eb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="329eb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="329eb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="329eb-108">Attributes</span></span>

<span data-ttu-id="329eb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="329eb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="329eb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="329eb-110">Child elements</span></span>

|<span data-ttu-id="329eb-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="329eb-111">**Element**</span></span>|<span data-ttu-id="329eb-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="329eb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="329eb-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="329eb-113">BaseShape</span></span>](baseshape.md) <br/> |<span data-ttu-id="329eb-114">Identifiziert die grundlegende Konfiguration von Eigenschaften in einer Antwort Elements oder Ordners zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="329eb-114">Identifies the basic configuration of properties to return in an item or folder response.</span></span>  <br/> |
|[<span data-ttu-id="329eb-115">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="329eb-115">IncludeMimeContent</span></span>](includemimecontent.md) <br/> |<span data-ttu-id="329eb-116">Gibt an, ob der Inhalt Multipurpose Internet Mail Extensions (MIME) eines Elements in der Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="329eb-116">Specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item is returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="329eb-117">BodyType</span><span class="sxs-lookup"><span data-stu-id="329eb-117">BodyType</span></span>](bodytype.md) <br/> |<span data-ttu-id="329eb-118">Gibt an, wie der Textkörper in der Antwort formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="329eb-118">Identifies how the body text is formatted in the response.</span></span>  <br/> |
|[<span data-ttu-id="329eb-119">ConvertHtmlCodePageToUTF8</span><span class="sxs-lookup"><span data-stu-id="329eb-119">ConvertHtmlCodePageToUTF8</span></span>](converthtmlcodepagetoutf8.md) <br/> |<span data-ttu-id="329eb-120">Gibt an, ob das Element HTML-Textkörper in UTF8 konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="329eb-120">Indicates whether the item HTML body is converted to UTF8.</span></span>  <br/> |
|[<span data-ttu-id="329eb-121">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="329eb-121">FilterHtmlContent</span></span>](filterhtmlcontent.md) <br/> |<span data-ttu-id="329eb-122">Gibt an, ob HTML-Content-Filterung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="329eb-122">Specifies whether HTML content filtering is enabled.</span></span>  <br/> |
|[<span data-ttu-id="329eb-123">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="329eb-123">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="329eb-124">Bezeichnet die zusätzliche Eigenschaften, die in eine Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="329eb-124">Identifies additional properties to return in a response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="329eb-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="329eb-125">Parent elements</span></span>

|<span data-ttu-id="329eb-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="329eb-126">**Element**</span></span>|<span data-ttu-id="329eb-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="329eb-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="329eb-128">GetItem</span><span class="sxs-lookup"><span data-stu-id="329eb-128">GetItem</span></span>](getitem.md) <br/> |<span data-ttu-id="329eb-129">Definiert eine Anforderung zum Abrufen von Elementen aus einem Postfach im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="329eb-129">Defines a request to retrieve items from a mailbox in the Exchange store.</span></span>  <br/> <span data-ttu-id="329eb-130">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="329eb-130">The following is the XPath expression to this element:</span></span>  <br/>  `/GetItem` <br/> |
|[<span data-ttu-id="329eb-131">FindItem</span><span class="sxs-lookup"><span data-stu-id="329eb-131">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="329eb-132">Definiert eine Anforderung an allen Elementen gesucht, die in einem Ordner enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="329eb-132">Defines a request to find all items that are contained in a folder.</span></span>  <br/> <span data-ttu-id="329eb-133">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="329eb-133">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
|[<span data-ttu-id="329eb-134">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="329eb-134">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="329eb-135">Definiert eine Anforderung zum Synchronisieren von Elementen in einem Ordner von Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="329eb-135">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> <span data-ttu-id="329eb-136">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="329eb-136">The following is the XPath expression to this element:</span></span>  <br/>  `/SyncFolderItems` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="329eb-137">Textwert</span><span class="sxs-lookup"><span data-stu-id="329eb-137">Text value</span></span>

<span data-ttu-id="329eb-138">Keine.</span><span class="sxs-lookup"><span data-stu-id="329eb-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="329eb-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="329eb-139">Remarks</span></span>

<span data-ttu-id="329eb-140">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="329eb-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="329eb-141">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="329eb-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="329eb-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="329eb-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="329eb-143">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="329eb-143">Schema Name</span></span>  <br/> |<span data-ttu-id="329eb-144">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="329eb-144">Messages schema</span></span>  <br/> |
|<span data-ttu-id="329eb-145">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="329eb-145">Validation File</span></span>  <br/> |<span data-ttu-id="329eb-146">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="329eb-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="329eb-147">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="329eb-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="329eb-148">False</span><span class="sxs-lookup"><span data-stu-id="329eb-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="329eb-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="329eb-149">See also</span></span>



[<span data-ttu-id="329eb-150">GetItem Operation</span><span class="sxs-lookup"><span data-stu-id="329eb-150">GetItem operation</span></span>](getitem-operation.md)
  
[<span data-ttu-id="329eb-151">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="329eb-151">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="329eb-152">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="329eb-152">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="329eb-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="329eb-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

