---
title: ID (e-mailemailtype)
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
description: Das ID-Element identifiziert einen Besprechungsraum in der Exchange Server-Organisation.
ms.openlocfilehash: aa09e7764746ac6bc283de2d13248d769aba75b7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460778"
---
# <a name="id-emailaddresstype"></a><span data-ttu-id="51655-103">ID (e-mailemailtype)</span><span class="sxs-lookup"><span data-stu-id="51655-103">Id (EmailAddressType)</span></span>

<span data-ttu-id="51655-104">Das **ID-** Element identifiziert einen Besprechungsraum in der Exchange Server-Organisation.</span><span class="sxs-lookup"><span data-stu-id="51655-104">The **Id** element identifies a meeting room within the Exchange server organization.</span></span> 
  
[<span data-ttu-id="51655-105">Raum</span><span class="sxs-lookup"><span data-stu-id="51655-105">Room</span></span>](room.md)
  
[<span data-ttu-id="51655-106">ID (e-mailemailtype)</span><span class="sxs-lookup"><span data-stu-id="51655-106">Id (EmailAddressType)</span></span>](id-emailaddresstype.md)
  
```xml
<Id>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Id>
```

 <span data-ttu-id="51655-107">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="51655-107">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="51655-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="51655-108">Attributes and elements</span></span>

<span data-ttu-id="51655-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="51655-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="51655-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="51655-110">Attributes</span></span>

<span data-ttu-id="51655-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="51655-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="51655-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="51655-112">Child elements</span></span>

|<span data-ttu-id="51655-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="51655-113">**Element**</span></span>|<span data-ttu-id="51655-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="51655-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="51655-115">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="51655-115">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="51655-116">Definiert den Namen des Besprechungsraums.</span><span class="sxs-lookup"><span data-stu-id="51655-116">Defines the name of the meeting room.</span></span> <span data-ttu-id="51655-117">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="51655-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="51655-118">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="51655-118">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="51655-119">Definiert die Simple Mail Transfer Protocol (SMTP) Adresse eines Besprechungsraums.</span><span class="sxs-lookup"><span data-stu-id="51655-119">Defines the Simple Mail Transfer Protocol (SMTP) address of a meeting room.</span></span> <span data-ttu-id="51655-120">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="51655-120">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="51655-121">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="51655-121">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="51655-p103">Definiert die Weiterleitung, die für das Postfach verwendet wird. Der Standard lautet SMTP. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="51655-p103">Defines the routing that is used for the mailbox. The default is SMTP. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="51655-125">MailboxType</span><span class="sxs-lookup"><span data-stu-id="51655-125">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="51655-p104">Definiert den Postfachtyp eines Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="51655-p104">Defines the mailbox type of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="51655-128">ItemId</span><span class="sxs-lookup"><span data-stu-id="51655-128">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="51655-p105">Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="51655-p105">Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="51655-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="51655-131">Parent elements</span></span>

|<span data-ttu-id="51655-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="51655-132">**Element**</span></span>|<span data-ttu-id="51655-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="51655-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="51655-134">Raum</span><span class="sxs-lookup"><span data-stu-id="51655-134">Room</span></span>](room.md) <br/> |<span data-ttu-id="51655-135">Definiert einen Besprechungsraum in der Exchange Server-Organisation.</span><span class="sxs-lookup"><span data-stu-id="51655-135">Defines a meeting room in the Exchange server organization.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51655-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51655-136">Remarks</span></span>

<span data-ttu-id="51655-137">Das Schema, das dieses Element beschreibt, befindet sich im EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="51655-137">The schema that describes this element is located in the EWS directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="51655-138">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="51655-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="51655-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="51655-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="51655-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="51655-140">Schema Name</span></span>  <br/> |<span data-ttu-id="51655-141">Schematypen</span><span class="sxs-lookup"><span data-stu-id="51655-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="51655-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="51655-142">Validation File</span></span>  <br/> |<span data-ttu-id="51655-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="51655-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="51655-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="51655-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="51655-145">False</span><span class="sxs-lookup"><span data-stu-id="51655-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="51655-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51655-146">See also</span></span>



[<span data-ttu-id="51655-147">GetRooms-Vorgang</span><span class="sxs-lookup"><span data-stu-id="51655-147">GetRooms operation</span></span>](getrooms-operation.md)


- [<span data-ttu-id="51655-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="51655-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

