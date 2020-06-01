---
title: UpdateInboxRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateInboxRules
api_type:
- schema
ms.assetid: d220064f-ff4d-4537-8077-adf94f2cbdbd
description: Das UpdateInboxRules -Element definiert eine Anforderung zum Aktualisieren der Posteingangsregeln in einem Postfach im Serverspeicher.
ms.openlocfilehash: d604604d582d28c07eaa75d3239082d1b6735e65
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456360"
---
# <a name="updateinboxrules"></a><span data-ttu-id="45f75-103">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="45f75-103">UpdateInboxRules</span></span>

<span data-ttu-id="45f75-104">Das **UpdateInboxRules** -Element definiert eine Anforderung zum Aktualisieren der Posteingangsregeln in einem Postfach im Serverspeicher.</span><span class="sxs-lookup"><span data-stu-id="45f75-104">The **UpdateInboxRules** element defines a request to update the Inbox rules in a mailbox in the server store.</span></span> 
  
```XML
<UpdateInboxRules>
   <MailboxSmtpAddress/>
   <RemoveOutlookRuleBlob/>
   <Operations/>
</UpdateInboxRules>
```

 <span data-ttu-id="45f75-105">**UpdateInboxRulesRequestType**</span><span class="sxs-lookup"><span data-stu-id="45f75-105">**UpdateInboxRulesRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="45f75-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="45f75-106">Attributes and elements</span></span>

<span data-ttu-id="45f75-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="45f75-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="45f75-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="45f75-108">Attributes</span></span>

<span data-ttu-id="45f75-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="45f75-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="45f75-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="45f75-110">Child elements</span></span>

|<span data-ttu-id="45f75-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="45f75-111">**Element**</span></span>|<span data-ttu-id="45f75-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="45f75-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="45f75-113">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="45f75-113">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md) <br/> |<span data-ttu-id="45f75-114">Stellt die SMTP-Adresse des Benutzers, dessen Posteingangsregeln erstellt, geändert oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="45f75-114">Represents the SMTP address of the user whose Inbox rules are to be created, modified, or deleted.</span></span>  <br/> |
|[<span data-ttu-id="45f75-115">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="45f75-115">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md) <br/> |<span data-ttu-id="45f75-116">Gibt an, ob das Microsoft Outlook-Regel Blob entfernt.</span><span class="sxs-lookup"><span data-stu-id="45f75-116">Indicates whether to remove the Microsoft Outlook rule blob.</span></span>  <br/> |
|[<span data-ttu-id="45f75-117">Betrieb</span><span class="sxs-lookup"><span data-stu-id="45f75-117">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="45f75-118">Enthält ein Array der Regelvorgänge, die für ein Postfach ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="45f75-118">Contains an array of rule operations that can be performed on an Inbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="45f75-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="45f75-119">Parent elements</span></span>

<span data-ttu-id="45f75-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="45f75-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="45f75-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="45f75-121">Text value</span></span>

<span data-ttu-id="45f75-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="45f75-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="45f75-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45f75-123">Remarks</span></span>

<span data-ttu-id="45f75-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="45f75-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="45f75-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="45f75-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45f75-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="45f75-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="45f75-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="45f75-127">Schema Name</span></span>  <br/> |<span data-ttu-id="45f75-128">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="45f75-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="45f75-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="45f75-129">Validation File</span></span>  <br/> |<span data-ttu-id="45f75-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="45f75-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="45f75-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="45f75-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="45f75-132">True</span><span class="sxs-lookup"><span data-stu-id="45f75-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="45f75-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45f75-133">See also</span></span>



[<span data-ttu-id="45f75-134">UpdateInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="45f75-134">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)


- [<span data-ttu-id="45f75-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="45f75-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

