---
title: ContactsView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContactsView
api_type:
- schema
ms.assetid: 8534f44b-a5af-4a9f-9621-23a3eff5f9d8
description: Das ContactsView-Element definiert eine Suche nach Kontaktelementen basierend auf alphabetischen Anzeigenamen.
ms.openlocfilehash: 23c3fe13c44cdd0e5a054ecb3378bc3d633e55aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463818"
---
# <a name="contactsview"></a><span data-ttu-id="0e091-103">ContactsView</span><span class="sxs-lookup"><span data-stu-id="0e091-103">ContactsView</span></span>

<span data-ttu-id="0e091-104">Das **ContactsView** -Element definiert eine Suche nach Kontaktelementen basierend auf alphabetischen Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="0e091-104">The **ContactsView** element defines a search for contact items based on alphabetical display names.</span></span> 
  
[<span data-ttu-id="0e091-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="0e091-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="0e091-106">ContactsView</span><span class="sxs-lookup"><span data-stu-id="0e091-106">ContactsView</span></span>](contactsview.md)
  
```xml
<ContactsView MaxEntriesReturned="" InitialName="" FinalName="" />
```

<span data-ttu-id="0e091-107">**ContactsViewType**</span><span class="sxs-lookup"><span data-stu-id="0e091-107">**ContactsViewType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="0e091-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0e091-108">Attributes and elements</span></span>

<span data-ttu-id="0e091-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0e091-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0e091-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0e091-110">Attributes</span></span>

|<span data-ttu-id="0e091-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0e091-111">**Attribute**</span></span>|<span data-ttu-id="0e091-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0e091-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0e091-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="0e091-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="0e091-114">Beschreibt die maximale Anzahl von Ergebnissen, die in der [FindItem](finditem.md) -Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0e091-114">Describes the maximum number of results to return in the [FindItem](finditem.md) response.</span></span>  <br/> |
|<span data-ttu-id="0e091-115">**Initialname**</span><span class="sxs-lookup"><span data-stu-id="0e091-115">**InitialName**</span></span> <br/> |<span data-ttu-id="0e091-116">Definiert den ersten Namen in der Kontaktliste, der in der Antwort zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e091-116">Defines the first name in the contacts list to return in the response.</span></span> <span data-ttu-id="0e091-117">Wenn sich der angegebene ursprüngliche Name nicht in der Kontaktliste befindet, wird der nächste alphabetische Name im Kultur Kontext zurückgegeben, außer wenn der nächste Name nach **finalname**kommt.</span><span class="sxs-lookup"><span data-stu-id="0e091-117">If the specified initial name is not in the contacts list, the next alphabetical name as defined by the cultural context will be returned, except if the next name comes after **FinalName**.</span></span> <span data-ttu-id="0e091-118">Wenn das **Initial** Name-Attribut nicht angegeben wird, enthält die Antwort eine Liste von Kontakten, die mit dem ersten Namen in der Kontaktliste beginnt.</span><span class="sxs-lookup"><span data-stu-id="0e091-118">If the **InitialName** attribute is omitted, the response will contain a list of contacts that starts with the first name in the contact list.</span></span> <span data-ttu-id="0e091-119">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="0e091-119">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="0e091-120">**Finalname**</span><span class="sxs-lookup"><span data-stu-id="0e091-120">**FinalName**</span></span> <br/> |<span data-ttu-id="0e091-121">Definiert den letzten Namen in der Kontaktliste, der in der Antwort zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e091-121">Defines the last name in the contacts list to return in the response.</span></span> <span data-ttu-id="0e091-122">Wenn das **finalname** -Attribut nicht angegeben wird, enthält die Antwort alle nachfolgenden Kontakte in der angegebenen Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="0e091-122">If the **FinalName** attribute is omitted, the response will contain all subsequent contacts in the specified sort order.</span></span> <span data-ttu-id="0e091-123">Wenn sich der angegebene endgültige Name nicht in der Kontaktliste befindet, wird der nächste alphabetische Name im Kultur Kontext ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="0e091-123">If the specified final name is not in the contacts list, the next alphabetical name as defined by the cultural context will be excluded.</span></span>  <br/><br/><span data-ttu-id="0e091-124">Wenn beispielsweise finalname = "Name", aber Name nicht in der Kontaktliste enthalten ist, werden Kontakte mit Anzeigenamen von Name1 oder Name nicht einbezogen.</span><span class="sxs-lookup"><span data-stu-id="0e091-124">For example, if FinalName="Name", but Name is not in the contacts list, contacts that have display names of Name1 or NAME will not be included.</span></span>  <br/><br/><span data-ttu-id="0e091-125">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="0e091-125">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0e091-126">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0e091-126">Child elements</span></span>

<span data-ttu-id="0e091-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="0e091-127">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0e091-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0e091-128">Parent elements</span></span>

|<span data-ttu-id="0e091-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="0e091-129">**Element**</span></span>|<span data-ttu-id="0e091-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0e091-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0e091-131">FindItem</span><span class="sxs-lookup"><span data-stu-id="0e091-131">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="0e091-132">Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="0e091-132">Defines a request to find items in a mailbox.</span></span><br/><br/> <span data-ttu-id="0e091-133">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="0e091-133">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e091-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e091-134">Remarks</span></span>

<span data-ttu-id="0e091-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="0e091-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="0e091-136">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0e091-136">Example</span></span>

<span data-ttu-id="0e091-137">Im folgenden Beispiel einer Anforderung wird veranschaulicht, wie die ersten drei Kontakte, beginnend mit dem Kontakt mit dem Anzeigenamen von Kelly Rollin, gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="0e091-137">The following example of a request demonstrates how to find the first three contacts starting with the contact that has the display name of Kelly Rollin.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="contacts:DisplayName"/>
        </t:AdditionalProperties>
      </ItemShape>
      <ContactsView MaxEntriesReturned="3" InitialName="Kelly Rollin" />
      <SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="contacts:DisplayName"/>
        </t:FieldOrder>
        </SortOrder>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="contacts"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="0e091-138">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0e091-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e091-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="0e091-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0e091-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0e091-140">Schema Name</span></span>  <br/> |<span data-ttu-id="0e091-141">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="0e091-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0e091-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0e091-142">Validation File</span></span>  <br/> |<span data-ttu-id="0e091-143">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0e091-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0e091-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0e091-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="0e091-145">False</span><span class="sxs-lookup"><span data-stu-id="0e091-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e091-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e091-146">See also</span></span>

- [<span data-ttu-id="0e091-147">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0e091-147">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="0e091-148">Finding Items</span><span class="sxs-lookup"><span data-stu-id="0e091-148">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

