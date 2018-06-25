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
description: Das ContactsView-Element definiert eine Suche für Kontaktelemente basierend auf alphabetische Anzeigenamen.
ms.openlocfilehash: e578eb4dd0042b8c478e883c7fa54d7f2e984229
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757636"
---
# <a name="contactsview"></a><span data-ttu-id="f2573-103">ContactsView</span><span class="sxs-lookup"><span data-stu-id="f2573-103">ContactsView</span></span>

<span data-ttu-id="f2573-104">Das **ContactsView** -Element definiert eine Suche für Kontaktelemente basierend auf alphabetische Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="f2573-104">The **ContactsView** element defines a search for contact items based on alphabetical display names.</span></span> 
  
[<span data-ttu-id="f2573-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="f2573-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="f2573-106">ContactsView</span><span class="sxs-lookup"><span data-stu-id="f2573-106">ContactsView</span></span>](contactsview.md)
  
```xml
<ContactsView MaxEntriesReturned="" InitialName="" FinalName="" />
```

<span data-ttu-id="f2573-107">**ContactsViewType**</span><span class="sxs-lookup"><span data-stu-id="f2573-107">**ContactsViewType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f2573-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f2573-108">Attributes and elements</span></span>

<span data-ttu-id="f2573-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f2573-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2573-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="f2573-110">Attributes</span></span>

|<span data-ttu-id="f2573-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f2573-111">**Attribute**</span></span>|<span data-ttu-id="f2573-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2573-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f2573-113">**"MaxEntriesReturned"**</span><span class="sxs-lookup"><span data-stu-id="f2573-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="f2573-114">Beschreibt die maximale Anzahl der in der Antwort [FindItem](finditem.md) zurückzugebender Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="f2573-114">Describes the maximum number of results to return in the [FindItem](finditem.md) response.</span></span>  <br/> |
|<span data-ttu-id="f2573-115">**InitialName**</span><span class="sxs-lookup"><span data-stu-id="f2573-115">**InitialName**</span></span> <br/> |<span data-ttu-id="f2573-116">Definiert den ersten Namen in der Kontaktliste in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f2573-116">Defines the first name in the contacts list to return in the response.</span></span> <span data-ttu-id="f2573-117">Wenn der angegebene anfänglichen Name nicht in der Kontaktliste auf den Namen des nächsten alphabetische ist, wie durch die kulturellen Kontext definiert werden zurückgegeben außer, wenn der nächste Name nach **FinalName wird**.</span><span class="sxs-lookup"><span data-stu-id="f2573-117">If the specified initial name is not in the contacts list, the next alphabetical name as defined by the cultural context will be returned, except if the next name comes after **FinalName**.</span></span> <span data-ttu-id="f2573-118">Wenn das Attribut **InitialName** ausgelassen wird, enthält die Antwort eine Liste von Kontakten, die mit der erste Name in der Kontaktliste beginnt.</span><span class="sxs-lookup"><span data-stu-id="f2573-118">If the **InitialName** attribute is omitted, the response will contain a list of contacts that starts with the first name in the contact list.</span></span> <span data-ttu-id="f2573-119">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="f2573-119">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="f2573-120">**FinalName**</span><span class="sxs-lookup"><span data-stu-id="f2573-120">**FinalName**</span></span> <br/> |<span data-ttu-id="f2573-121">Definiert den Nachnamen in der Kontaktliste in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f2573-121">Defines the last name in the contacts list to return in the response.</span></span> <span data-ttu-id="f2573-122">Wenn das Attribut **FinalName** ausgelassen wird, enthält die Antwort alle nachfolgenden Kontakte in der angegebenen Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="f2573-122">If the **FinalName** attribute is omitted, the response will contain all subsequent contacts in the specified sort order.</span></span> <span data-ttu-id="f2573-123">Ist der angegebene endgültige Name nicht in der Kontaktliste, wird der Name des nächsten alphabetische gemäß Definition durch die kulturellen Kontext ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="f2573-123">If the specified final name is not in the contacts list, the next alphabetical name as defined by the cultural context will be excluded.</span></span>  <br/><br/><span data-ttu-id="f2573-124">Beispielsweise wenn FinalName = "Name", aber Name ist nicht in der Kontaktliste, Kontakte, die Anzeigenamen der Name1 oder NAME nicht enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="f2573-124">For example, if FinalName="Name", but Name is not in the contacts list, contacts that have display names of Name1 or NAME will not be included.</span></span>  <br/><br/><span data-ttu-id="f2573-125">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="f2573-125">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f2573-126">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f2573-126">Child elements</span></span>

<span data-ttu-id="f2573-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="f2573-127">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f2573-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f2573-128">Parent elements</span></span>

|<span data-ttu-id="f2573-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="f2573-129">**Element**</span></span>|<span data-ttu-id="f2573-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2573-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2573-131">FindItem</span><span class="sxs-lookup"><span data-stu-id="f2573-131">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="f2573-132">Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="f2573-132">Defines a request to find items in a mailbox.</span></span><br/><br/> <span data-ttu-id="f2573-133">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="f2573-133">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2573-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f2573-134">Remarks</span></span>

<span data-ttu-id="f2573-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f2573-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="f2573-136">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f2573-136">Example</span></span>

<span data-ttu-id="f2573-137">Im folgenden Beispiel wird eine Anforderung veranschaulicht, wie die ersten drei Kontakte, beginnend mit der Kontakt den Anzeigenamen des Kelly Rollin auf Suchen.</span><span class="sxs-lookup"><span data-stu-id="f2573-137">The following example of a request demonstrates how to find the first three contacts starting with the contact that has the display name of Kelly Rollin.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a><span data-ttu-id="f2573-138">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f2573-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2573-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2573-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f2573-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f2573-140">Schema Name</span></span>  <br/> |<span data-ttu-id="f2573-141">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f2573-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f2573-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f2573-142">Validation File</span></span>  <br/> |<span data-ttu-id="f2573-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f2573-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f2573-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f2573-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="f2573-145">False</span><span class="sxs-lookup"><span data-stu-id="f2573-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2573-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2573-146">See also</span></span>

- [<span data-ttu-id="f2573-147">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f2573-147">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="f2573-148">Finding Items</span><span class="sxs-lookup"><span data-stu-id="f2573-148">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

