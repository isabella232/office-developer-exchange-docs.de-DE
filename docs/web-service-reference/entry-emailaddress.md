---
title: Eintrag (EmailAddress)
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
description: Entry-Element stellt eine einzelne e-Mail-Adresse für einen Kontakt.
ms.openlocfilehash: 1852584e507c38da030815c37f85f7c4af4e2ba4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758250"
---
# <a name="entry-emailaddress"></a><span data-ttu-id="8dbb2-103">Eintrag (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="8dbb2-103">Entry (EmailAddress)</span></span>

<span data-ttu-id="8dbb2-104">**Entry** -Element stellt eine einzelne e-Mail-Adresse für einen Kontakt.</span><span class="sxs-lookup"><span data-stu-id="8dbb2-104">The **Entry** element represents a single e-mail address for a contact.</span></span> 
  
```XML
<Entry Key="" Name="" RoutingType="" MailboxType="" />
```

<span data-ttu-id="8dbb2-105">**EmailAddressDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="8dbb2-105">**EmailAddressDictionaryEntryType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="8dbb2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8dbb2-106">Attributes and elements</span></span>

<span data-ttu-id="8dbb2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8dbb2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8dbb2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8dbb2-108">Attributes</span></span>

|<span data-ttu-id="8dbb2-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8dbb2-109">**Attribute**</span></span>|<span data-ttu-id="8dbb2-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8dbb2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8dbb2-111">**Key**</span><span class="sxs-lookup"><span data-stu-id="8dbb2-111">**Key**</span></span> <br/> | <span data-ttu-id="8dbb2-112">Gibt die e-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="8dbb2-112">Identifies the e-mail address.</span></span><br/><br/><span data-ttu-id="8dbb2-113">Es folgen die möglichen Werte für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="8dbb2-113">The following are the possible values for this attribute:</span></span><br/><br/><span data-ttu-id="8dbb2-114">-EmailAddress1</span><span class="sxs-lookup"><span data-stu-id="8dbb2-114">-  EmailAddress1</span></span>  <br/><span data-ttu-id="8dbb2-115">-EmailAddress2</span><span class="sxs-lookup"><span data-stu-id="8dbb2-115">-  EmailAddress2</span></span>  <br/><span data-ttu-id="8dbb2-116">-EmailAddress3</span><span class="sxs-lookup"><span data-stu-id="8dbb2-116">-  EmailAddress3</span></span> <br/><br/>  <span data-ttu-id="8dbb2-117">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8dbb2-117">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="8dbb2-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="8dbb2-118">**Name**</span></span> <br/> |<span data-ttu-id="8dbb2-119">Definiert den Namen des Postfachbenutzers.</span><span class="sxs-lookup"><span data-stu-id="8dbb2-119">Defines the name of the mailbox user.</span></span> <span data-ttu-id="8dbb2-120">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="8dbb2-120">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="8dbb2-121">**RoutingType**</span><span class="sxs-lookup"><span data-stu-id="8dbb2-121">**RoutingType**</span></span> <br/> |<span data-ttu-id="8dbb2-122">Definiert die Weiterleitung, die für das Postfach verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8dbb2-122">Defines the routing that is used for the mailbox.</span></span> <span data-ttu-id="8dbb2-123">Der Standard lautet SMTP.</span><span class="sxs-lookup"><span data-stu-id="8dbb2-123">The default is SMTP.</span></span> <span data-ttu-id="8dbb2-124">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="8dbb2-124">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="8dbb2-125">**MailboxType**</span><span class="sxs-lookup"><span data-stu-id="8dbb2-125">**MailboxType**</span></span> <br/> |<span data-ttu-id="8dbb2-126">Definiert den Postfachtyp eines Postfachbenutzers.</span><span class="sxs-lookup"><span data-stu-id="8dbb2-126">Defines the mailbox type of a mailbox user.</span></span> <span data-ttu-id="8dbb2-127">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="8dbb2-127">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8dbb2-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8dbb2-128">Child elements</span></span>

<span data-ttu-id="8dbb2-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="8dbb2-129">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8dbb2-130">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8dbb2-130">Parent elements</span></span>

|<span data-ttu-id="8dbb2-131">**Element**</span><span class="sxs-lookup"><span data-stu-id="8dbb2-131">**Element**</span></span>|<span data-ttu-id="8dbb2-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8dbb2-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8dbb2-133">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="8dbb2-133">EmailAddresses</span></span>](emailaddresses.md) <br/> |<span data-ttu-id="8dbb2-134">Stellt eine Auflistung von E-mail-Adressen für einen Kontakt.</span><span class="sxs-lookup"><span data-stu-id="8dbb2-134">Represents a collection of e-mail addresses for a contact.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8dbb2-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8dbb2-135">Remarks</span></span>

<span data-ttu-id="8dbb2-136">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8dbb2-136">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8dbb2-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="8dbb2-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8dbb2-138">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8dbb2-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8dbb2-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="8dbb2-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8dbb2-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8dbb2-140">Schema name</span></span>  <br/> |<span data-ttu-id="8dbb2-141">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8dbb2-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="8dbb2-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8dbb2-142">Validation file</span></span>  <br/> |<span data-ttu-id="8dbb2-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8dbb2-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8dbb2-144">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8dbb2-144">Can be empty</span></span>  <br/> |<span data-ttu-id="8dbb2-145">False</span><span class="sxs-lookup"><span data-stu-id="8dbb2-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8dbb2-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8dbb2-146">See also</span></span>

- [<span data-ttu-id="8dbb2-147">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8dbb2-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

