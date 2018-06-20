---
title: IsModerated
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsModerated
api_type:
- schema
ms.assetid: a7562256-feb9-41a1-857e-b5d41cbed680
description: Das IsModerated-Element gibt an, ob das Postfach des Empfängers ist moderiert wird.
ms.openlocfilehash: 8db234f9706bb8187978a76f745323749d7a640a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830055"
---
# <a name="ismoderated"></a><span data-ttu-id="0da2c-103">IsModerated</span><span class="sxs-lookup"><span data-stu-id="0da2c-103">IsModerated</span></span>

<span data-ttu-id="0da2c-104">Das **IsModerated** -Element gibt an, ob das Postfach des Empfängers ist moderiert wird.</span><span class="sxs-lookup"><span data-stu-id="0da2c-104">The **IsModerated** element indicates whether the recipient's mailbox is being moderated.</span></span> 
  
```XML
<IsModerated>true | false</IsModerated>
```

 <span data-ttu-id="0da2c-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0da2c-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0da2c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0da2c-106">Attributes and elements</span></span>

<span data-ttu-id="0da2c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0da2c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0da2c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0da2c-108">Attributes</span></span>

<span data-ttu-id="0da2c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0da2c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0da2c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0da2c-110">Child elements</span></span>

<span data-ttu-id="0da2c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0da2c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0da2c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0da2c-112">Parent elements</span></span>

|<span data-ttu-id="0da2c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0da2c-113">**Element**</span></span>|<span data-ttu-id="0da2c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0da2c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0da2c-115">E-Mail-Infos</span><span class="sxs-lookup"><span data-stu-id="0da2c-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="0da2c-116">Stellt Werte für verschiedene Arten von e-Mail-Infos.</span><span class="sxs-lookup"><span data-stu-id="0da2c-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0da2c-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="0da2c-117">Text value</span></span>

<span data-ttu-id="0da2c-118">Der Textwert für dieses Element ist **true** , wenn das Postfach des Empfängers ist moderiert wird.</span><span class="sxs-lookup"><span data-stu-id="0da2c-118">The text value for this element is **true** if the recipient's mailbox is being moderated.</span></span> <span data-ttu-id="0da2c-119">Der Wert ist **false** , wenn das Postfach des Empfängers ist nicht moderiert wird.</span><span class="sxs-lookup"><span data-stu-id="0da2c-119">The value is **false** if the recipient's mailbox is not being moderated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0da2c-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0da2c-120">Remarks</span></span>

<span data-ttu-id="0da2c-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0da2c-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0da2c-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0da2c-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0da2c-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="0da2c-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0da2c-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0da2c-124">Schema Name</span></span>  <br/> |<span data-ttu-id="0da2c-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0da2c-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="0da2c-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0da2c-126">Validation File</span></span>  <br/> |<span data-ttu-id="0da2c-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0da2c-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0da2c-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0da2c-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="0da2c-129">False</span><span class="sxs-lookup"><span data-stu-id="0da2c-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0da2c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0da2c-130">See also</span></span>



- [<span data-ttu-id="0da2c-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0da2c-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

