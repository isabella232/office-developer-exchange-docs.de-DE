---
title: GetDiscoverySearchConfigurationResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9d963e6c-e94d-462b-8c44-95d55c848fb2
description: Das GetDiscoverySearchConfigurationResponse-Element gibt die Antwort auf eine GetDiscoverySearchConfiguration an.
ms.openlocfilehash: 6f4bbc05da0c2883f78b31cb46108e993b8b8fdd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758636"
---
# <a name="getdiscoverysearchconfigurationresponse"></a><span data-ttu-id="d96bb-103">GetDiscoverySearchConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="d96bb-103">GetDiscoverySearchConfigurationResponse</span></span>

<span data-ttu-id="d96bb-104">Das **GetDiscoverySearchConfigurationResponse** -Element gibt die Antwort auf eine **GetDiscoverySearchConfiguration** an.</span><span class="sxs-lookup"><span data-stu-id="d96bb-104">The **GetDiscoverySearchConfigurationResponse** element specifies the response to a **GetDiscoverySearchConfiguration** request.</span></span> 
  
```XML
<GetDiscoverySearchConfigurationResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DiscoverySearchConfigurations/>
</GetDiscoverySearchConfigurationResponse>
```

 <span data-ttu-id="d96bb-105">**GetDiscoverySearchConfigurationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="d96bb-105">**GetDiscoverySearchConfigurationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d96bb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d96bb-106">Attributes and elements</span></span>

<span data-ttu-id="d96bb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d96bb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d96bb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d96bb-108">Attributes</span></span>

<span data-ttu-id="d96bb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d96bb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d96bb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d96bb-110">Child elements</span></span>

<span data-ttu-id="d96bb-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [DiscoverySearchConfigurations](discoverysearchconfigurations.md)</span><span class="sxs-lookup"><span data-stu-id="d96bb-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [DiscoverySearchConfigurations](discoverysearchconfigurations.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d96bb-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d96bb-112">Parent elements</span></span>

[<span data-ttu-id="d96bb-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d96bb-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="d96bb-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d96bb-114">Remarks</span></span>

<span data-ttu-id="d96bb-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d96bb-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d96bb-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d96bb-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d96bb-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d96bb-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d96bb-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="d96bb-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d96bb-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d96bb-119">Schema name</span></span>  <br/> |<span data-ttu-id="d96bb-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d96bb-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d96bb-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d96bb-121">Validation file</span></span>  <br/> |<span data-ttu-id="d96bb-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d96bb-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d96bb-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d96bb-123">Can be empty</span></span>  <br/> |<span data-ttu-id="d96bb-124">false</span><span class="sxs-lookup"><span data-stu-id="d96bb-124">false</span></span>  <br/> |
   
