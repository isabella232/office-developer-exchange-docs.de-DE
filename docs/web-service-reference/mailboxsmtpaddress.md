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
description: Das MailboxSmtpAddress-Element darstellt, die SMTP-Adresse des Benutzers, dessen Posteingangsregeln abgerufen oder aktualisiert werden sollen; oder, deren Ablaufdatum Kennwort abgerufen werden sollen.
ms.openlocfilehash: 60b2c018f2a05e9630e92e28de1054a421b41e52
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830303"
---
# <a name="mailboxsmtpaddress"></a><span data-ttu-id="a81ef-103">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="a81ef-103">MailboxSmtpAddress</span></span>

<span data-ttu-id="a81ef-104">Das **MailboxSmtpAddress** -Element darstellt, die SMTP-Adresse des Benutzers, dessen Posteingangsregeln abgerufen oder aktualisiert werden sollen; oder, deren Ablaufdatum Kennwort abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a81ef-104">The **MailboxSmtpAddress** element represents the SMTP address of the user whose Inbox rules are to be retrieved or updated; or whose password expiration date is to be retrieved.</span></span> 
  
```XML
<MailboxSmtpAddress/>
```

<span data-ttu-id="a81ef-105">**string**</span><span class="sxs-lookup"><span data-stu-id="a81ef-105">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a81ef-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a81ef-106">Attributes and elements</span></span>

<span data-ttu-id="a81ef-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a81ef-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a81ef-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a81ef-108">Attributes</span></span>

<span data-ttu-id="a81ef-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a81ef-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a81ef-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a81ef-110">Child elements</span></span>

<span data-ttu-id="a81ef-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="a81ef-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a81ef-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a81ef-112">Parent elements</span></span>

|<span data-ttu-id="a81ef-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a81ef-113">**Element**</span></span>|<span data-ttu-id="a81ef-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a81ef-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a81ef-115">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="a81ef-115">GetInboxRules</span></span>](getinboxrules.md) <br/> |<span data-ttu-id="a81ef-116">Definiert eine Anforderung zum Abrufen der Posteingangsregeln für ein Postfach im Serverspeicher.</span><span class="sxs-lookup"><span data-stu-id="a81ef-116">Defines a request to get the Inbox rules on a mailbox in the server store.</span></span>  <br/> |
|[<span data-ttu-id="a81ef-117">GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="a81ef-117">GetPasswordExpirationDate</span></span>](getpasswordexpirationdate.md) <br/> |<span data-ttu-id="a81ef-118">Definiert eine Anforderung an das Kennwort Ablaufdatum ein e-Mail-Konto zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a81ef-118">Defines a request to get the password expiration date of an email account.</span></span>  <br/> |
|[<span data-ttu-id="a81ef-119">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="a81ef-119">UpdateInboxRules</span></span>](updateinboxrules.md) <br/> |<span data-ttu-id="a81ef-120">Definiert eine Anforderung zum Aktualisieren der Posteingangsregeln in einem Postfach im Serverspeicher.</span><span class="sxs-lookup"><span data-stu-id="a81ef-120">Defines a request to update the Inbox rules in a mailbox in the server store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a81ef-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="a81ef-121">Text value</span></span>

<span data-ttu-id="a81ef-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="a81ef-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a81ef-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a81ef-123">Remarks</span></span>

<span data-ttu-id="a81ef-124">Das **MailboxSmtpAddress** -Element ist ein optionales Element.</span><span class="sxs-lookup"><span data-stu-id="a81ef-124">The **MailboxSmtpAddress** element is an optional element.</span></span> <span data-ttu-id="a81ef-125">Wenn das Element **MailboxSmtpAddress** ausgelassen wird, wird die Adresse des angemeldeten Benutzers verwendet.</span><span class="sxs-lookup"><span data-stu-id="a81ef-125">If the **MailboxSmtpAddress** element is omitted, the address of the logged on user is used.</span></span> 
  
<span data-ttu-id="a81ef-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a81ef-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a81ef-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a81ef-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a81ef-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="a81ef-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a81ef-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a81ef-129">Schema Name</span></span>  <br/> |<span data-ttu-id="a81ef-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a81ef-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="a81ef-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a81ef-131">Validation File</span></span>  <br/> |<span data-ttu-id="a81ef-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a81ef-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a81ef-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a81ef-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="a81ef-134">True</span><span class="sxs-lookup"><span data-stu-id="a81ef-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a81ef-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a81ef-135">See also</span></span>

- [<span data-ttu-id="a81ef-136">GetInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a81ef-136">GetInboxRules operation</span></span>](getinboxrules-operation.md)
- [<span data-ttu-id="a81ef-137">GetPasswordExpirationDate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a81ef-137">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md)
- [<span data-ttu-id="a81ef-138">UpdateInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a81ef-138">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)
- [<span data-ttu-id="a81ef-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a81ef-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

