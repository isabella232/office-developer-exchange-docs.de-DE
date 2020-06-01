---
title: Eintrag (e-mailemail)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Entry
api_type:
- schema
ms.assetid: b028c5c7-3494-4ecd-96d1-78783daa660f
description: Das Entry-Element stellt eine einzelne e-Mail-Adresse für einen Kontakt dar.
ms.openlocfilehash: 766d67cda10b02c07a7677e541fddfc38a4285cf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459644"
---
# <a name="entry-emailaddress"></a><span data-ttu-id="216b7-103">Eintrag (e-mailemail)</span><span class="sxs-lookup"><span data-stu-id="216b7-103">Entry (EmailAddress)</span></span>

<span data-ttu-id="216b7-104">Das **Entry** -Element stellt eine einzelne e-Mail-Adresse für einen Kontakt dar.</span><span class="sxs-lookup"><span data-stu-id="216b7-104">The **Entry** element represents a single e-mail address for a contact.</span></span> 
  
```XML
<Entry Key="" Name="" RoutingType="" MailboxType="" />
```

<span data-ttu-id="216b7-105">**EmailAddressDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="216b7-105">**EmailAddressDictionaryEntryType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="216b7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="216b7-106">Attributes and elements</span></span>

<span data-ttu-id="216b7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="216b7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="216b7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="216b7-108">Attributes</span></span>

|<span data-ttu-id="216b7-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="216b7-109">**Attribute**</span></span>|<span data-ttu-id="216b7-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="216b7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="216b7-111">**Key**</span><span class="sxs-lookup"><span data-stu-id="216b7-111">**Key**</span></span> <br/> | <span data-ttu-id="216b7-112">Identifiziert die e-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="216b7-112">Identifies the e-mail address.</span></span><br/><br/><span data-ttu-id="216b7-113">Es folgen die möglichen Werte für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="216b7-113">The following are the possible values for this attribute:</span></span><br/><br/><span data-ttu-id="216b7-114">-EmailAddress1</span><span class="sxs-lookup"><span data-stu-id="216b7-114">-  EmailAddress1</span></span>  <br/><span data-ttu-id="216b7-115">-EmailAddress2</span><span class="sxs-lookup"><span data-stu-id="216b7-115">-  EmailAddress2</span></span>  <br/><span data-ttu-id="216b7-116">- EmailAddress3</span><span class="sxs-lookup"><span data-stu-id="216b7-116">-  EmailAddress3</span></span> <br/><br/>  <span data-ttu-id="216b7-117">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="216b7-117">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="216b7-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="216b7-118">**Name**</span></span> <br/> |<span data-ttu-id="216b7-119">Definiert den Namen des Postfachbenutzers.</span><span class="sxs-lookup"><span data-stu-id="216b7-119">Defines the name of the mailbox user.</span></span> <span data-ttu-id="216b7-120">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="216b7-120">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="216b7-121">**Routing Type**</span><span class="sxs-lookup"><span data-stu-id="216b7-121">**RoutingType**</span></span> <br/> |<span data-ttu-id="216b7-122">Definiert die Weiterleitung, die für das Postfach verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="216b7-122">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="216b7-123">Der Standard lautet SMTP.</span><span class="sxs-lookup"><span data-stu-id="216b7-123">The default is SMTP.</span></span> <span data-ttu-id="216b7-124">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="216b7-124">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="216b7-125">**MailboxType**</span><span class="sxs-lookup"><span data-stu-id="216b7-125">**MailboxType**</span></span> <br/> |<span data-ttu-id="216b7-126">Definiert den Postfachtyp eines Postfachbenutzers.</span><span class="sxs-lookup"><span data-stu-id="216b7-126">Defines the mailbox type of a mailbox user.</span></span> <span data-ttu-id="216b7-127">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="216b7-127">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="216b7-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="216b7-128">Child elements</span></span>

<span data-ttu-id="216b7-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="216b7-129">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="216b7-130">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="216b7-130">Parent elements</span></span>

|<span data-ttu-id="216b7-131">**Element**</span><span class="sxs-lookup"><span data-stu-id="216b7-131">**Element**</span></span>|<span data-ttu-id="216b7-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="216b7-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="216b7-133">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="216b7-133">EmailAddresses</span></span>](emailaddresses.md) <br/> |<span data-ttu-id="216b7-134">Stellt eine Auflistung von e-Mail-Adressen für einen Kontakt dar.</span><span class="sxs-lookup"><span data-stu-id="216b7-134">Represents a collection of e-mail addresses for a contact.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="216b7-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="216b7-135">Remarks</span></span>

<span data-ttu-id="216b7-136">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="216b7-136">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="216b7-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="216b7-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="216b7-138">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="216b7-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="216b7-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="216b7-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="216b7-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="216b7-140">Schema name</span></span>  <br/> |<span data-ttu-id="216b7-141">Schematypen</span><span class="sxs-lookup"><span data-stu-id="216b7-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="216b7-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="216b7-142">Validation file</span></span>  <br/> |<span data-ttu-id="216b7-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="216b7-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="216b7-144">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="216b7-144">Can be empty</span></span>  <br/> |<span data-ttu-id="216b7-145">False</span><span class="sxs-lookup"><span data-stu-id="216b7-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="216b7-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="216b7-146">See also</span></span>

- [<span data-ttu-id="216b7-147">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="216b7-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

