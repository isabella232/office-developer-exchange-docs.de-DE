---
title: ID (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Id
api_type:
- schema
ms.assetid: 3e1e37b5-5469-4447-ad1f-c2c6d4e0482f
description: Das Id-Element identifiziert einen Besprechungsraum innerhalb der Exchange Server-Organisation.
ms.openlocfilehash: 5cd62f6f4e5912d2ecccda352be15c6a3b24e06c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829847"
---
# <a name="id-emailaddresstype"></a><span data-ttu-id="cda8a-103">ID (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="cda8a-103">Id (EmailAddressType)</span></span>

<span data-ttu-id="cda8a-104">Das **Id** -Element identifiziert einen Besprechungsraum innerhalb der Exchange Server-Organisation.</span><span class="sxs-lookup"><span data-stu-id="cda8a-104">The **Id** element identifies a meeting room within the Exchange server organization.</span></span> 
  
[<span data-ttu-id="cda8a-105">Raum</span><span class="sxs-lookup"><span data-stu-id="cda8a-105">Room</span></span>](room.md)
  
[<span data-ttu-id="cda8a-106">ID (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="cda8a-106">Id (EmailAddressType)</span></span>](id-emailaddresstype.md)
  
```xml
<Id>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Id>
```

 <span data-ttu-id="cda8a-107">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="cda8a-107">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cda8a-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cda8a-108">Attributes and elements</span></span>

<span data-ttu-id="cda8a-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cda8a-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cda8a-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="cda8a-110">Attributes</span></span>

<span data-ttu-id="cda8a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="cda8a-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cda8a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cda8a-112">Child elements</span></span>

|<span data-ttu-id="cda8a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="cda8a-113">**Element**</span></span>|<span data-ttu-id="cda8a-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cda8a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cda8a-115">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="cda8a-115">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="cda8a-116">Der Name der Besprechungsraum definiert.</span><span class="sxs-lookup"><span data-stu-id="cda8a-116">Defines the name of the meeting room.</span></span> <span data-ttu-id="cda8a-117">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="cda8a-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="cda8a-118">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="cda8a-118">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="cda8a-119">Definiert die Adresse Simple Mail Transfer Protocol (SMTP), der einen Besprechungsraum.</span><span class="sxs-lookup"><span data-stu-id="cda8a-119">Defines the Simple Mail Transfer Protocol (SMTP) address of a meeting room.</span></span> <span data-ttu-id="cda8a-120">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="cda8a-120">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="cda8a-121">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="cda8a-121">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="cda8a-p103">Definiert die Weiterleitung, die für das Postfach verwendet wird. Der Standard lautet SMTP. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="cda8a-p103">Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="cda8a-125">MailboxType</span><span class="sxs-lookup"><span data-stu-id="cda8a-125">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="cda8a-p104">Definiert den Postfachtyp eines Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="cda8a-p104">Defines the mailbox type of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="cda8a-128">ItemId</span><span class="sxs-lookup"><span data-stu-id="cda8a-128">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="cda8a-p105">Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="cda8a-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cda8a-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cda8a-131">Parent elements</span></span>

|<span data-ttu-id="cda8a-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="cda8a-132">**Element**</span></span>|<span data-ttu-id="cda8a-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cda8a-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cda8a-134">Raum</span><span class="sxs-lookup"><span data-stu-id="cda8a-134">Room</span></span>](room.md) <br/> |<span data-ttu-id="cda8a-135">Definiert einen Besprechungsraum in Exchange Server-Organisation.</span><span class="sxs-lookup"><span data-stu-id="cda8a-135">Defines a meeting room in the Exchange server organization.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cda8a-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cda8a-136">Remarks</span></span>

<span data-ttu-id="cda8a-137">Das Schema, das dieses Element beschreibt befindet sich in die EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="cda8a-137">The schema that describes this element is located in the EWS directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cda8a-138">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="cda8a-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cda8a-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="cda8a-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cda8a-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cda8a-140">Schema Name</span></span>  <br/> |<span data-ttu-id="cda8a-141">Schematypen</span><span class="sxs-lookup"><span data-stu-id="cda8a-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="cda8a-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cda8a-142">Validation File</span></span>  <br/> |<span data-ttu-id="cda8a-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cda8a-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cda8a-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cda8a-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="cda8a-145">False</span><span class="sxs-lookup"><span data-stu-id="cda8a-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cda8a-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cda8a-146">See also</span></span>



[<span data-ttu-id="cda8a-147">GetRooms-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cda8a-147">GetRooms operation</span></span>](getrooms-operation.md)


- [<span data-ttu-id="cda8a-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cda8a-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

