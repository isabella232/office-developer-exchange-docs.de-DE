---
title: GetDiscoverySearchConfigurationResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1b84a4c6-cb0a-4bca-85b2-fec32227930b
description: Das GetDiscoverySearchConfigurationResponseMessage-Element gibt die Antwortnachricht für eine Anforderung GetDiscoverySearchConfiguration.
ms.openlocfilehash: a6cf09753031a7fd2eb46132e8bfb0729140d6c3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758635"
---
# <a name="getdiscoverysearchconfigurationresponsemessage"></a><span data-ttu-id="f49a1-103">GetDiscoverySearchConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f49a1-103">GetDiscoverySearchConfigurationResponseMessage</span></span>

<span data-ttu-id="f49a1-104">Das **GetDiscoverySearchConfigurationResponseMessage** -Element gibt die Antwortnachricht für eine Anforderung **GetDiscoverySearchConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="f49a1-104">The **GetDiscoverySearchConfigurationResponseMessage** element specifies the response message for a **GetDiscoverySearchConfiguration** request.</span></span> 
  
```XML
<GetDiscoverySearchConfigurationResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DiscoverySearchConfigurations/>
</GetDiscoverySearchConfigurationResponseMessage>
```

 <span data-ttu-id="f49a1-105">**GetDiscoverySearchConfigurationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f49a1-105">**GetDiscoverySearchConfigurationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f49a1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f49a1-106">Attributes and elements</span></span>

<span data-ttu-id="f49a1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f49a1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f49a1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f49a1-108">Attributes</span></span>

<span data-ttu-id="f49a1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f49a1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f49a1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f49a1-110">Child elements</span></span>

<span data-ttu-id="f49a1-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [DiscoverySearchConfigurations](discoverysearchconfigurations.md)</span><span class="sxs-lookup"><span data-stu-id="f49a1-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [DiscoverySearchConfigurations](discoverysearchconfigurations.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f49a1-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f49a1-112">Parent elements</span></span>

[<span data-ttu-id="f49a1-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f49a1-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="f49a1-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f49a1-114">Remarks</span></span>

<span data-ttu-id="f49a1-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f49a1-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f49a1-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f49a1-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f49a1-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f49a1-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f49a1-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="f49a1-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f49a1-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f49a1-119">Schema name</span></span>  <br/> |<span data-ttu-id="f49a1-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f49a1-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f49a1-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f49a1-121">Validation file</span></span>  <br/> |<span data-ttu-id="f49a1-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f49a1-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f49a1-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f49a1-123">Can be empty</span></span>  <br/> |<span data-ttu-id="f49a1-124">false</span><span class="sxs-lookup"><span data-stu-id="f49a1-124">false</span></span>  <br/> |
   

