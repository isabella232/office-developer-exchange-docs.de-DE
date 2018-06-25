---
title: RoomList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RoomList
api_type:
- schema
ms.assetid: cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2
description: Das RoomList-Element darstellt, eine e-Mail-Adresse, die eine Liste von Besprechungsräumen identifiziert.
ms.openlocfilehash: 7de2c67f8001387abf463186933f0b81ee45a58a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831262"
---
# <a name="roomlist"></a><span data-ttu-id="ffd5e-103">RoomList</span><span class="sxs-lookup"><span data-stu-id="ffd5e-103">RoomList</span></span>

<span data-ttu-id="ffd5e-104">Das **RoomList** -Element darstellt, eine e-Mail-Adresse, die eine Liste von Besprechungsräumen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ffd5e-104">The **RoomList** element represents an e-mail address that identifies a list of meeting rooms.</span></span> 
  
[<span data-ttu-id="ffd5e-105">GetRooms</span><span class="sxs-lookup"><span data-stu-id="ffd5e-105">GetRooms</span></span>](getrooms.md)
  
[<span data-ttu-id="ffd5e-106">RoomList</span><span class="sxs-lookup"><span data-stu-id="ffd5e-106">RoomList</span></span>](roomlist.md)
  
```XML
<RoomList>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</RoomList>
```

 <span data-ttu-id="ffd5e-107">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="ffd5e-107">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ffd5e-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ffd5e-108">Attributes and elements</span></span>

<span data-ttu-id="ffd5e-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ffd5e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ffd5e-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ffd5e-110">Attributes</span></span>

<span data-ttu-id="ffd5e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ffd5e-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ffd5e-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ffd5e-112">Child elements</span></span>

|<span data-ttu-id="ffd5e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ffd5e-113">**Element**</span></span>|<span data-ttu-id="ffd5e-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffd5e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ffd5e-115">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="ffd5e-115">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="ffd5e-116">Der Anzeigename der Raumliste definiert.</span><span class="sxs-lookup"><span data-stu-id="ffd5e-116">Defines the display name of the room list.</span></span> <span data-ttu-id="ffd5e-117">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="ffd5e-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="ffd5e-118">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="ffd5e-118">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="ffd5e-119">Definiert die Adresse Simple Mail Transfer Protocol (SMTP), der eine Raumliste.</span><span class="sxs-lookup"><span data-stu-id="ffd5e-119">Defines the Simple Mail Transfer Protocol (SMTP) address of a room list.</span></span> <span data-ttu-id="ffd5e-120">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="ffd5e-120">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="ffd5e-121">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="ffd5e-121">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="ffd5e-p103">Definiert die Weiterleitung, die für das Postfach verwendet wird. Der Standard lautet SMTP. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="ffd5e-p103">Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="ffd5e-125">MailboxType</span><span class="sxs-lookup"><span data-stu-id="ffd5e-125">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="ffd5e-p104">Definiert den Postfachtyp eines Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="ffd5e-p104">Defines the mailbox type of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="ffd5e-128">ItemId</span><span class="sxs-lookup"><span data-stu-id="ffd5e-128">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="ffd5e-p105">Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="ffd5e-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's Contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ffd5e-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ffd5e-131">Parent elements</span></span>

|<span data-ttu-id="ffd5e-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="ffd5e-132">**Element**</span></span>|<span data-ttu-id="ffd5e-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffd5e-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ffd5e-134">GetRooms</span><span class="sxs-lookup"><span data-stu-id="ffd5e-134">GetRooms</span></span>](getrooms.md) <br/> |<span data-ttu-id="ffd5e-135">Das Stammelement im eine Anforderung an eine Liste der Räume innerhalb einer bestimmten Raumliste abrufen.</span><span class="sxs-lookup"><span data-stu-id="ffd5e-135">The root element in a request to get a list of rooms within a particular room list.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ffd5e-136">Textwert</span><span class="sxs-lookup"><span data-stu-id="ffd5e-136">Text value</span></span>

<span data-ttu-id="ffd5e-137">Keine.</span><span class="sxs-lookup"><span data-stu-id="ffd5e-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ffd5e-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ffd5e-138">Remarks</span></span>

<span data-ttu-id="ffd5e-139">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ffd5e-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ffd5e-140">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ffd5e-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ffd5e-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="ffd5e-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ffd5e-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ffd5e-142">Schema Name</span></span>  <br/> |<span data-ttu-id="ffd5e-143">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ffd5e-143">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ffd5e-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ffd5e-144">Validation File</span></span>  <br/> |<span data-ttu-id="ffd5e-145">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ffd5e-145">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ffd5e-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ffd5e-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="ffd5e-147">False</span><span class="sxs-lookup"><span data-stu-id="ffd5e-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ffd5e-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffd5e-148">See also</span></span>



[<span data-ttu-id="ffd5e-149">GetRooms-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ffd5e-149">GetRooms operation</span></span>](getrooms-operation.md)


- [<span data-ttu-id="ffd5e-150">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ffd5e-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

