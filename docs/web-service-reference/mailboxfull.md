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
description: Das MailboxFull-Element gibt an, ob das Postfach des Empfängers voll ist.
ms.openlocfilehash: 8e2c9e01b93af03e875834724a942cd9b17a73f3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830286"
---
# <a name="mailboxfull"></a><span data-ttu-id="3d270-103">MailboxFull</span><span class="sxs-lookup"><span data-stu-id="3d270-103">MailboxFull</span></span>

<span data-ttu-id="3d270-104">Das **MailboxFull** -Element gibt an, ob das Postfach des Empfängers voll ist.</span><span class="sxs-lookup"><span data-stu-id="3d270-104">The **MailboxFull** element indicates whether the mailbox for the recipient is full.</span></span> 
  
```XML
<MailboxFull>true | false</MailboxFull>
```

<span data-ttu-id="3d270-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3d270-105">**Boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3d270-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3d270-106">Attributes and elements</span></span>

<span data-ttu-id="3d270-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3d270-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3d270-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3d270-108">Attributes</span></span>

<span data-ttu-id="3d270-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3d270-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3d270-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3d270-110">Child elements</span></span>

<span data-ttu-id="3d270-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3d270-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3d270-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3d270-112">Parent elements</span></span>

|<span data-ttu-id="3d270-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3d270-113">**Element**</span></span>|<span data-ttu-id="3d270-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3d270-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3d270-115">E-Mail-Infos</span><span class="sxs-lookup"><span data-stu-id="3d270-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="3d270-116">Stellt Werte für verschiedene Arten von e-Mail-Infos.</span><span class="sxs-lookup"><span data-stu-id="3d270-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3d270-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="3d270-117">Text value</span></span>

<span data-ttu-id="3d270-118">Dieses Element kann **true** oder **false**sein.</span><span class="sxs-lookup"><span data-stu-id="3d270-118">This element can be either **true** or **false**.</span></span> <span data-ttu-id="3d270-119">Der Wert **true** gibt an, dass das Postfach seine Kapazität erreicht hat. der Wert **false** gibt an, dass sie nicht die Kapazität erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="3d270-119">A value of **true** indicates that the mailbox has reached its capacity; a value of **false** indicates that it has not reached capacity.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3d270-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3d270-120">Remarks</span></span>

<span data-ttu-id="3d270-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3d270-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3d270-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3d270-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3d270-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="3d270-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3d270-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3d270-124">Schema Name</span></span>  <br/> |<span data-ttu-id="3d270-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3d270-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="3d270-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3d270-126">Validation File</span></span>  <br/> |<span data-ttu-id="3d270-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3d270-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3d270-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3d270-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="3d270-129">False</span><span class="sxs-lookup"><span data-stu-id="3d270-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3d270-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d270-130">See also</span></span>

- [<span data-ttu-id="3d270-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3d270-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

