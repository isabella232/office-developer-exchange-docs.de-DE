---
title: RecipientAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecipientAddress
api_type:
- schema
ms.assetid: 9ae6351a-2c60-4715-a489-5681a13641f9
description: RecipientAddress-Element darstellt, das Postfach des Empfängers.
ms.openlocfilehash: 10928ac206227cfc21bd83ab5bfa9a55aad354e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830974"
---
# <a name="recipientaddress"></a><span data-ttu-id="e848d-103">RecipientAddress</span><span class="sxs-lookup"><span data-stu-id="e848d-103">RecipientAddress</span></span>

<span data-ttu-id="e848d-104">**RecipientAddress** -Element darstellt, das Postfach des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="e848d-104">The **RecipientAddress** element represents the mailbox of the recipient.</span></span> 
  
```xml
<RecipientAddress>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</RecipientAddress>
```

 <span data-ttu-id="e848d-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="e848d-105">**EmailAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e848d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e848d-106">Attributes and elements</span></span>

<span data-ttu-id="e848d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e848d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e848d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e848d-108">Attributes</span></span>

<span data-ttu-id="e848d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e848d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e848d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e848d-110">Child elements</span></span>

|<span data-ttu-id="e848d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e848d-111">**Element**</span></span>|<span data-ttu-id="e848d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e848d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e848d-113">Name (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="e848d-113">Name (EmailAddressType)</span></span>](name-emailaddresstype.md) <br/> |<span data-ttu-id="e848d-114">Stellt den Namen des Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="e848d-114">Represents the name of the mailbox user.</span></span> <span data-ttu-id="e848d-115">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="e848d-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="e848d-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="e848d-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="e848d-p102">Definiert die Simple Mail Transfer Protocol (SMTP)-Adresse eines Postfachbenutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="e848d-p102">Defines the Simple Mail Transfer Protocol (SMTP) address of a mailbox user. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="e848d-119">RoutingType (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="e848d-119">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="e848d-120">Stellt das routing-Protokoll für den Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="e848d-120">Represents the routing protocol for the recipient.</span></span> <span data-ttu-id="e848d-121">Der Standard lautet SMTP.</span><span class="sxs-lookup"><span data-stu-id="e848d-121">The default is SMTP.</span></span> <span data-ttu-id="e848d-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="e848d-122">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="e848d-123">MailboxType</span><span class="sxs-lookup"><span data-stu-id="e848d-123">MailboxType</span></span>](mailboxtype.md) <br/> |<span data-ttu-id="e848d-124">Stellt den Typ des Postfachs an, das die e-Mail-Adresse dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e848d-124">Represents the type of mailbox that is represented by the e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="e848d-125">ItemId</span><span class="sxs-lookup"><span data-stu-id="e848d-125">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="e848d-p104">Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="e848d-p104">Defines the item identifier of a contact or private distribution list for recipients from a user's contacts folder. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e848d-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e848d-128">Parent elements</span></span>

|<span data-ttu-id="e848d-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="e848d-129">**Element**</span></span>|<span data-ttu-id="e848d-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e848d-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e848d-131">E-Mail-Infos</span><span class="sxs-lookup"><span data-stu-id="e848d-131">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="e848d-132">Stellt Werte für verschiedene Arten von e-Mail-Infos.</span><span class="sxs-lookup"><span data-stu-id="e848d-132">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e848d-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e848d-133">Remarks</span></span>

<span data-ttu-id="e848d-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e848d-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e848d-135">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e848d-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e848d-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="e848d-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e848d-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e848d-137">Schema Name</span></span>  <br/> |<span data-ttu-id="e848d-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e848d-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="e848d-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e848d-139">Validation File</span></span>  <br/> |<span data-ttu-id="e848d-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e848d-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e848d-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e848d-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="e848d-142">False</span><span class="sxs-lookup"><span data-stu-id="e848d-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e848d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e848d-143">See also</span></span>



- [<span data-ttu-id="e848d-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e848d-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

