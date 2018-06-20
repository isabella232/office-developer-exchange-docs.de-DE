---
title: Postfach (PreviewItemMailboxType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e898d737-b6e4-4403-9c2c-aec52a48a83d
description: Das Postfach-Element enthält die Postfach-ID und primäre Simple Mail Transfer Protocol (SMTP)-Adresse des Benutzers.
ms.openlocfilehash: 1b6669928015bc880806479d294a4063034a559f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830255"
---
# <a name="mailbox-previewitemmailboxtype"></a><span data-ttu-id="6af9f-103">Postfach (PreviewItemMailboxType)</span><span class="sxs-lookup"><span data-stu-id="6af9f-103">Mailbox (PreviewItemMailboxType)</span></span>

<span data-ttu-id="6af9f-104">Das **Postfach** -Element enthält die Postfach-ID und primäre Simple Mail Transfer Protocol (SMTP)-Adresse des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="6af9f-104">The **Mailbox** element contains the mailbox identifier and the user's primary Simple Mail Transfer Protocol (SMTP) address.</span></span> 
  
```XML
<Mailbox>
   <MailboxId/>
   <PrimarySmtpAddress/>
</Mailbox>
```

<span data-ttu-id="6af9f-105">**PreviewItemMailboxType**</span><span class="sxs-lookup"><span data-stu-id="6af9f-105">**PreviewItemMailboxType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6af9f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6af9f-106">Attributes and elements</span></span>

<span data-ttu-id="6af9f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6af9f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6af9f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6af9f-108">Attributes</span></span>

<span data-ttu-id="6af9f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6af9f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6af9f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6af9f-110">Child elements</span></span>

<span data-ttu-id="6af9f-111">[MailboxId](mailboxid.md) | [PrimarySmtpAddress (Zeichenfolge)](primarysmtpaddress-string.md)</span><span class="sxs-lookup"><span data-stu-id="6af9f-111">[MailboxId](mailboxid.md) | [PrimarySmtpAddress (string)](primarysmtpaddress-string.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6af9f-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6af9f-112">Parent elements</span></span>

[<span data-ttu-id="6af9f-113">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="6af9f-113">SearchPreviewItem</span></span>](searchpreviewitem.md)
  
## <a name="remarks"></a><span data-ttu-id="6af9f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6af9f-114">Remarks</span></span>

<span data-ttu-id="6af9f-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6af9f-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6af9f-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6af9f-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6af9f-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6af9f-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6af9f-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="6af9f-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6af9f-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6af9f-119">Schema name</span></span>  <br/> |<span data-ttu-id="6af9f-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6af9f-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="6af9f-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6af9f-121">Validation file</span></span>  <br/> |<span data-ttu-id="6af9f-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6af9f-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6af9f-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="6af9f-123">Can be empty</span></span>  <br/> |<span data-ttu-id="6af9f-124">false</span><span class="sxs-lookup"><span data-stu-id="6af9f-124">false</span></span>  <br/> |
   

