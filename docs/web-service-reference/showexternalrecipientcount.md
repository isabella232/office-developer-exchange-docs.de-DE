---
title: ShowExternalRecipientCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ShowExternalRecipientCount
api_type:
- schema
ms.assetid: db28dbcb-d051-4e5c-a9c2-4b8d5149b4e1
description: Das ShowExternalRecipientCount-Element gibt an, ob Consumer des Vorgangs GetMailTips müssen e-Mail-Infos anzeigen, die die Anzahl der externe Empfänger angeben, zu denen eine Nachricht adressiert ist.
ms.openlocfilehash: 1fd3ceb629689c560dc60afe01f0413602f79a0d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831491"
---
# <a name="showexternalrecipientcount"></a><span data-ttu-id="050d4-103">ShowExternalRecipientCount</span><span class="sxs-lookup"><span data-stu-id="050d4-103">ShowExternalRecipientCount</span></span>

<span data-ttu-id="050d4-104">Das **ShowExternalRecipientCount** -Element gibt an, ob Consumer der [GetMailTips Vorgang](getmailtips-operation.md) müssen e-Mail-Infos anzeigen, die die Anzahl der externe Empfänger angeben, zu denen eine Nachricht adressiert ist.</span><span class="sxs-lookup"><span data-stu-id="050d4-104">The **ShowExternalRecipientCount** element indicates whether consumers of the [GetMailTips operation](getmailtips-operation.md) have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> 
  
```XML
<ShowExternalRecipientCount>true | false</ShowExternalRecipientCount>
```

 <span data-ttu-id="050d4-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="050d4-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="050d4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="050d4-106">Attributes and elements</span></span>

<span data-ttu-id="050d4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="050d4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="050d4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="050d4-108">Attributes</span></span>

<span data-ttu-id="050d4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="050d4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="050d4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="050d4-110">Child elements</span></span>

<span data-ttu-id="050d4-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="050d4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="050d4-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="050d4-112">Parent elements</span></span>

|<span data-ttu-id="050d4-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="050d4-113">**Element**</span></span>|<span data-ttu-id="050d4-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="050d4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="050d4-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="050d4-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="050d4-116">Enthält Konfigurationsinformationen für den e-Mail-Dienst Tipps Service.</span><span class="sxs-lookup"><span data-stu-id="050d4-116">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="050d4-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="050d4-117">Text value</span></span>

<span data-ttu-id="050d4-118">Der Textwert der dieses Element ist **true** , wenn die Consumer der [GetMailTips Vorgang](getmailtips-operation.md) müssen e-Mail-Infos anzeigen, die die Anzahl der externe Empfänger angeben, zu denen eine Nachricht adressiert ist.</span><span class="sxs-lookup"><span data-stu-id="050d4-118">The text value of this element is **true** if consumers of the [GetMailTips operation](getmailtips-operation.md) have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> <span data-ttu-id="050d4-119">Der Wert ist **false** , wenn Consumer der [GetMailTips Vorgang](getmailtips-operation.md) keinen e-Mail-Infos anzeigen, die die Anzahl der externe Empfänger angeben, zu denen eine Nachricht adressiert ist.</span><span class="sxs-lookup"><span data-stu-id="050d4-119">The value is **false** if consumers of the [GetMailTips operation](getmailtips-operation.md) do not have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="050d4-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="050d4-120">Remarks</span></span>

<span data-ttu-id="050d4-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="050d4-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="050d4-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="050d4-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="050d4-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="050d4-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="050d4-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="050d4-124">Schema Name</span></span>  <br/> |<span data-ttu-id="050d4-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="050d4-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="050d4-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="050d4-126">Validation File</span></span>  <br/> |<span data-ttu-id="050d4-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="050d4-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="050d4-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="050d4-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="050d4-129">False</span><span class="sxs-lookup"><span data-stu-id="050d4-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="050d4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="050d4-130">See also</span></span>



[<span data-ttu-id="050d4-131">GetMailTips-Vorgang</span><span class="sxs-lookup"><span data-stu-id="050d4-131">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="050d4-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="050d4-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

