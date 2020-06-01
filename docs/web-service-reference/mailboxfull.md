---
title: MailboxFull
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxFull
api_type:
- schema
ms.assetid: 38b28c9b-9da2-4d6a-9cda-9c393986575b
description: Das MailboxFull-Element gibt an, ob das Postfach für den Empfänger voll ist.
ms.openlocfilehash: f336f1eda122bb170aafb22a028e3faf84f4d782
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465975"
---
# <a name="mailboxfull"></a><span data-ttu-id="688d7-103">MailboxFull</span><span class="sxs-lookup"><span data-stu-id="688d7-103">MailboxFull</span></span>

<span data-ttu-id="688d7-104">Das **MailboxFull** -Element gibt an, ob das Postfach für den Empfänger voll ist.</span><span class="sxs-lookup"><span data-stu-id="688d7-104">The **MailboxFull** element indicates whether the mailbox for the recipient is full.</span></span> 
  
```XML
<MailboxFull>true | false</MailboxFull>
```

<span data-ttu-id="688d7-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="688d7-105">**Boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="688d7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="688d7-106">Attributes and elements</span></span>

<span data-ttu-id="688d7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="688d7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="688d7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="688d7-108">Attributes</span></span>

<span data-ttu-id="688d7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="688d7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="688d7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="688d7-110">Child elements</span></span>

<span data-ttu-id="688d7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="688d7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="688d7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="688d7-112">Parent elements</span></span>

|<span data-ttu-id="688d7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="688d7-113">**Element**</span></span>|<span data-ttu-id="688d7-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="688d7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="688d7-115">E-Mail-Info</span><span class="sxs-lookup"><span data-stu-id="688d7-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="688d7-116">Stellt Werte für verschiedene Arten von e-Mail-Tipps dar.</span><span class="sxs-lookup"><span data-stu-id="688d7-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="688d7-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="688d7-117">Text value</span></span>

<span data-ttu-id="688d7-118">Dieses Element kann entweder **true** oder **false**sein.</span><span class="sxs-lookup"><span data-stu-id="688d7-118">This element can be either **true** or **false**.</span></span> <span data-ttu-id="688d7-119">Der Wert **true** gibt an, dass das Postfach seine Kapazität erreicht hat; der Wert **false** gibt an, dass die Kapazität nicht erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="688d7-119">A value of **true** indicates that the mailbox has reached its capacity; a value of **false** indicates that it has not reached capacity.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="688d7-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="688d7-120">Remarks</span></span>

<span data-ttu-id="688d7-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="688d7-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="688d7-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="688d7-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="688d7-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="688d7-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="688d7-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="688d7-124">Schema Name</span></span>  <br/> |<span data-ttu-id="688d7-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="688d7-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="688d7-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="688d7-126">Validation File</span></span>  <br/> |<span data-ttu-id="688d7-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="688d7-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="688d7-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="688d7-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="688d7-129">False</span><span class="sxs-lookup"><span data-stu-id="688d7-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="688d7-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="688d7-130">See also</span></span>

- [<span data-ttu-id="688d7-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="688d7-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

