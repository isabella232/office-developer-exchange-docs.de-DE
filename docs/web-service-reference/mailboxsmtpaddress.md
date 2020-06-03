---
title: MailboxSmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxSmtpAddress
api_type:
- schema
ms.assetid: de7c9035-ebbc-4473-ac14-3b22ce62768c
description: Das MailboxSmtpAddress-Element stellt die SMTP-Adresse des Benutzers dar, dessen Posteingangsregeln abgerufen oder aktualisiert werden sollen. oder deren Kennwort-Ablaufdatum abgerufen werden soll.
ms.openlocfilehash: 613e8098210257280bec47f2b22a2d29d04fa07c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530544"
---
# <a name="mailboxsmtpaddress"></a><span data-ttu-id="83b0b-103">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="83b0b-103">MailboxSmtpAddress</span></span>

<span data-ttu-id="83b0b-104">Das **MailboxSmtpAddress** -Element stellt die SMTP-Adresse des Benutzers dar, dessen Posteingangsregeln abgerufen oder aktualisiert werden sollen. oder deren Kennwort-Ablaufdatum abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="83b0b-104">The **MailboxSmtpAddress** element represents the SMTP address of the user whose Inbox rules are to be retrieved or updated; or whose password expiration date is to be retrieved.</span></span> 
  
```XML
<MailboxSmtpAddress/>
```

<span data-ttu-id="83b0b-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83b0b-105">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="83b0b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="83b0b-106">Attributes and elements</span></span>

<span data-ttu-id="83b0b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="83b0b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83b0b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="83b0b-108">Attributes</span></span>

<span data-ttu-id="83b0b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="83b0b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83b0b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83b0b-110">Child elements</span></span>

<span data-ttu-id="83b0b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="83b0b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="83b0b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="83b0b-112">Parent elements</span></span>

|<span data-ttu-id="83b0b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="83b0b-113">**Element**</span></span>|<span data-ttu-id="83b0b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="83b0b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83b0b-115">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="83b0b-115">GetInboxRules</span></span>](getinboxrules.md) <br/> |<span data-ttu-id="83b0b-116">Definiert eine Anforderung zum Abrufen der Posteingangsregeln für ein Postfach im Server Speicher.</span><span class="sxs-lookup"><span data-stu-id="83b0b-116">Defines a request to get the Inbox rules on a mailbox in the server store.</span></span>  <br/> |
|[<span data-ttu-id="83b0b-117">GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="83b0b-117">GetPasswordExpirationDate</span></span>](getpasswordexpirationdate.md) <br/> |<span data-ttu-id="83b0b-118">Definiert eine Anforderung zum Abrufen des Kennwortablauf Datums eines e-Mail-Kontos.</span><span class="sxs-lookup"><span data-stu-id="83b0b-118">Defines a request to get the password expiration date of an email account.</span></span>  <br/> |
|[<span data-ttu-id="83b0b-119">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="83b0b-119">UpdateInboxRules</span></span>](updateinboxrules.md) <br/> |<span data-ttu-id="83b0b-120">Definiert eine Anforderung zum Aktualisieren der Posteingangsregeln in einem Postfach im Server Speicher.</span><span class="sxs-lookup"><span data-stu-id="83b0b-120">Defines a request to update the Inbox rules in a mailbox in the server store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="83b0b-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="83b0b-121">Text value</span></span>

<span data-ttu-id="83b0b-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="83b0b-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="83b0b-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83b0b-123">Remarks</span></span>

<span data-ttu-id="83b0b-124">Das **MailboxSmtpAddress** -Element ist ein optionales Element.</span><span class="sxs-lookup"><span data-stu-id="83b0b-124">The **MailboxSmtpAddress** element is an optional element.</span></span> <span data-ttu-id="83b0b-125">Wenn das **MailboxSmtpAddress** -Element ausgelassen wird, wird die Adresse des angemeldeten Benutzers verwendet.</span><span class="sxs-lookup"><span data-stu-id="83b0b-125">If the **MailboxSmtpAddress** element is omitted, the address of the logged on user is used.</span></span> 
  
<span data-ttu-id="83b0b-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="83b0b-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83b0b-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="83b0b-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83b0b-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="83b0b-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="83b0b-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="83b0b-129">Schema Name</span></span>  <br/> |<span data-ttu-id="83b0b-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="83b0b-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="83b0b-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="83b0b-131">Validation File</span></span>  <br/> |<span data-ttu-id="83b0b-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="83b0b-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="83b0b-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="83b0b-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="83b0b-134">True</span><span class="sxs-lookup"><span data-stu-id="83b0b-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83b0b-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83b0b-135">See also</span></span>

- [<span data-ttu-id="83b0b-136">GetInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="83b0b-136">GetInboxRules operation</span></span>](getinboxrules-operation.md)
- [<span data-ttu-id="83b0b-137">GetPasswordExpirationDate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="83b0b-137">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md)
- [<span data-ttu-id="83b0b-138">UpdateInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="83b0b-138">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)
- [<span data-ttu-id="83b0b-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="83b0b-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

