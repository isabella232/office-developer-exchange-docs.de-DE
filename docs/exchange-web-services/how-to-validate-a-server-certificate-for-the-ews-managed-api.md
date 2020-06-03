---
title: Überprüfen ein Serverzertifikats für die verwaltete EWS-API
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 1fe0b215-8340-4bc8-a6ce-4f591ca9e353
description: Hier erfahren Sie, wie Sie eine Rückrufmethode für die Zertifikatüberprüfung erstellen und referenzieren, sodass Sie verwaltete EWS-API Anforderungen an einen Exchange-Server stellen können.
localization_priority: Priority
ms.openlocfilehash: 195c51ca71890d6092e4182d23990bb528d37095
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456780"
---
# <a name="validate-a-server-certificate-for-the-ews-managed-api"></a>Überprüfen ein Serverzertifikats für die verwaltete EWS-API

Hier erfahren Sie, wie Sie eine Rückrufmethode für die Zertifikatüberprüfung erstellen und referenzieren, sodass Sie verwaltete EWS-API Anforderungen an einen Exchange-Server stellen können.
  
Standardmäßig verwenden Versionen von Exchange, die mit Exchange 2007 SP1 beginnen, selbstsignierte X509-Zertifikate, um Anrufe von EWS zu authentifizieren. Wenn Sie die verwaltete EWS-API verwenden, müssen Sie eine Rückrufmethode für die Zertifikatüberprüfung erstellen. Andernfalls tritt für verwaltete EWS-API-Anforderungen ein Fehler auf. Wenn Sie den AutoErmittlungsdienst verwenden, schlägt der Aufruf der verwaltete EWS-API Auto Ermittlungsmethode mit einem **AutodiscoverLocalException** -Fehler fehl. Wenn Sie einen von Webdiensten generierten Webdienstproxy verwenden, müssen Sie möglicherweise auch eine Validierungsrückruf Methode erstellen, je nachdem, wie der Proxy erstellt wird. 
  
## <a name="prerequisites-for-creating-a-validation-callback-method"></a>Voraussetzungen für das Erstellen einer Validierungsrückruf Methode
<a name="bk_prereq"> </a>

Um die Überprüfung eines Serverzertifikats einzurichten, stellen Sie sicher, dass Folgendes zutrifft: 
  
- Ihr Exchange-Server verwendet ein selbstsigniertes Zertifikat für EWS. Wenn der Administrator ein gültiges Zertifikat installiert hat, das auf ein Stammzertifikat ablauft, müssen Sie keine Validierungsrückruf Methode erstellen. 
    
- Sie erstellen eine verwaltete Anwendung, die einen Verweis auf die folgenden erforderlichen .NET Framework Namespaces enthält: 
    
  - **System.Net**
  - **System .net. Security**  
  - **System. Security. Cryptography. X509Certificates**
    
## <a name="example-callback-method-to-validate-a-server-certificate-for-the-ews-managed-api"></a>Beispiel: Callback-Methode zum Überprüfen eines Serverzertifikats für den verwaltete EWS-API
<a name="bk_example"> </a>

Das folgende Codebeispiel zeigt, wie Sie eine X509-Zertifikat Validierungsrückruf Methode für die verwaltete EWS-API erstellen. Diese Methode überprüft ein X509-Zertifikat und gibt nur dann true zurück, wenn eines der folgenden Kriterien erfüllt wird: 
  
- Das Zertifikat ist gültig und verfolgt wieder ein gültiges Stammzertifikat.    
- Das Zertifikat ist gültig und wird von dem Server selbst signiert, von dem es zurückgegeben wurde. 
    
> [!IMPORTANT]
> Die Rückrufmethode für die Zertifikatüberprüfung in diesem Beispiel bietet ausreichende Sicherheit für die Entwicklung und das Testen von verwaltete EWS-API Anwendungen. Es stellt jedoch möglicherweise keine ausreichende Sicherheit für die bereitgestellte Anwendung bereit. Sie sollten immer sicherstellen, dass die von Ihnen verwendete Rückrufmethode für die Zertifikatüberprüfung die Sicherheitsanforderungen Ihrer Organisation erfüllt. 
  
```cs
      private static bool CertificateValidationCallBack(
         object sender,
         System.Security.Cryptography.X509Certificates.X509Certificate certificate,
         System.Security.Cryptography.X509Certificates.X509Chain chain,
         System.Net.Security.SslPolicyErrors sslPolicyErrors)
    {
      // If the certificate is a valid, signed certificate, return true.
      if (sslPolicyErrors == System.Net.Security.SslPolicyErrors.None)
      {
        return true;
      }
      // If there are errors in the certificate chain, look at each error to determine the cause.
      if ((sslPolicyErrors &amp; System.Net.Security.SslPolicyErrors.RemoteCertificateChainErrors) != 0)
      {
        if (chain != null &amp;&amp; chain.ChainStatus != null)
        {
          foreach (System.Security.Cryptography.X509Certificates.X509ChainStatus status in chain.ChainStatus)
          {
            if ((certificate.Subject == certificate.Issuer) &amp;&amp;
               (status.Status == System.Security.Cryptography.X509Certificates.X509ChainStatusFlags.UntrustedRoot))
            {
              // Self-signed certificates with an untrusted root are valid. 
              continue;
            }
            else
            {
              if (status.Status != System.Security.Cryptography.X509Certificates.X509ChainStatusFlags.NoError)
              {
                // If there are any other errors in the certificate chain, the certificate is invalid,
             // so the method returns false.
                return false;
              }
            }
          }
        }
        // When processing reaches this line, the only errors in the certificate chain are 
    // untrusted root errors for self-signed certificates. These certificates are valid
    // for default Exchange server installations, so return true.
        return true;
      }
      else
      {
     // In all other cases, return false.
        return false;
      }
    }

```

Sie verwenden die **ServicePointManager** -Klasse im .net **System.net** -Namespace, um eine Validierungsrückruf Methode einzubinden, indem Sie die **ServerCertificateValidationCallback** -Eigenschaft festlegen. Sie können Code wie im folgenden Codebeispiel verwenden, um die **ServerCertificateValidationCallback** -Eigenschaft festzulegen. 
  
```cs
ServicePointManager.ServerCertificateValidationCallback = CertificateValidationCallBack;

```

## <a name="next-steps"></a>Nächste Schritte
<a name="bk_example"> </a>

Nachdem Sie die Validierungsrückruf Methode für die verwaltete EWS-API erstellt haben, können Sie den AutoErmittlungsdienst verwenden, um Verbindungspunkte und Benutzer-und Domäneneinstellungen von einem Exchange-Server abzurufen. Weitere Informationen finden Sie in den folgenden Artikeln:
  
- [Verwenden der AutoErmittlung für die Suche nach Verbindungspunkten](how-to-use-autodiscover-to-find-connection-points.md)
    
- [Abrufen von Benutzereinstellungen von Exchange mithilfe der AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [Abrufen von Domäneneinstellungen von einem Exchange-Server](how-to-get-domain-settings-from-an-exchange-server.md)
    
## <a name="see-also"></a>Siehe auch

- [Einrichten Ihrer EWS-Anwendung](setting-up-your-ews-application.md)  
- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)
    

