---

copyright:
  years: 2015, 2016
lastupdated: "2016-11-15"

---

# Introdução ao
{{site.data.keyword.amashort}}
{: #gettingstarted}

Inclua segurança em seu app móvel com o serviço {{site.data.keyword.amafull}}. É possível configurar a autorização do cliente para acessar recursos de
backend protegidos em execução no {{site.data.keyword.Bluemix_notm}}. Use provedores de identidade (Google e Facebook) ou identidades
customizadas para autenticar usuários e conceder acesso a
recursos backend protegidos e apps da web.
{:shortdesc}

**Nota:** O serviço {{site.data.keyword.amashort}} era
conhecido anteriormente como Advanced Mobile Access.


Para fazer com que o serviço {{site.data.keyword.amashort}} funcione:

1. Use uma das opções a seguir para criar um limite ou um
serviço desvinculado:
 * Crie um aplicativo usando o modelo do
{{site.data.keyword.Bluemix_notm}}
**MobileFirst Services Starter** no catálogo. Isso cria um limite de serviço
{{site.data.keyword.amashort}}
para um aplicativo backend
{{site.data.keyword.Bluemix_notm}}.
 * Crie um serviço {{site.data.keyword.amashort}}
usando o painel {{site.data.keyword.amashort}}.  É
possível ligar o serviço a um aplicativo backend existente e
configurá-lo no painel {{site.data.keyword.amashort}}.

   Ao usar o MobileFirst Services Starter, você obtém uma instância de um tempo de execução do Node.js que é executada no IBM {{site.data.keyword.Bluemix_notm}} para implementar sua lógica de backend customizada. 
Um conjunto de serviços móveis principais que fornece segurança, dados, push e funções de
monitoramento está vinculado a esse app Node.js. Após o app Node.js do {{site.data.keyword.Bluemix_notm}} ser criado, será possível configurar seu ambiente de desenvolvimento e iniciar o uso dos SDKs do {{site.data.keyword.Bluemix_notm}} Mobile Services. É possível usar os SDKs para acessar os serviços que estão ligados ao seu app em nuvem com chamadas API simples.

	Para obter mais informações sobre como criar e trabalhar com projetos, aplicativos
e serviços, veja [painel do
IBM Bluemix Mobile](https://console.{DomainName}/docs/mobile/index.html).

2. Recursos seguros do lado do servidor.

   Proteja seus recursos de backend móveis que estejam em execução nos tempos de execução Node.js ou Liberty for Java&trade; com a segurança OAuth ativada para dispositivo móvel. Para obter mais informações, veja [Protegendo recursos](protecting-resources.html).
   Para aprender mais sobre o aplicativo backend móvel padrão, consulte o aplicativo de amostra [bms-hellotodo-strongloop](https://github.com/ibm-bluemix-mobile-services/bms-hellotodo-strongloop).

3. Configure seu ambiente de desenvolvimento principal do {{site.data.keyword.amashort}}.

	####Desenvolvimento do Cliente
   {: #client-development}

	É possível incluir o {{site.data.keyword.amashort}} SDK no app Android, iOS ou Cordova existente, como a seguir:
   * Android: ([Configurando o Android SDK](getting-started-android.html)) ([Amostra](https://github.com/ibm-bluemix-mobile-services/bms-samples-android-helloauthentication))

   * iOS (Swift SDK): ([Configurando o iOS Swift SDK](getting-started-ios-swift-sdk.html))
      ([Amostra](https://github.com/ibm-bluemix-mobile-services/bms-samples-swift-helloauthentication))

   * iOS (Objective-C SDK): ([Configurando o iOS Object-C SDK](getting-started-ios.html)) ([Amostra](https://github.com/ibm-bluemix-mobile-services/bms-samples-ios-helloauthentication))

   * Cordova: ([Configurando o plug-in do Cordova](getting-started-cordova.html)) ([Amostra](https://github.com/ibm-bluemix-mobile-services/bms-samples-cordova-helloauthentication))

   **Nota:** embora o Objective-C SDK permaneça totalmente suportado e ainda considerado o SDK primário para o
{{site.data.keyword.amashort}}, há planos para descontinuar esse SDK posteriormente este ano em favor do novo Swift SDK. Se você está criando um aplicativo, é altamente recomendável usar o SDK do Swift (veja
[Configurando o SDK do Swift iOS](getting-started-ios-swift-sdk.html)).

	####Desenvolvimento da Web
   {: #web-development}

   O serviço {{site.data.keyword.amashort}} pode
proteger seu aplicativo da web, não requerendo SDK especial. É possível alavancar diferentes provedores de identidade, além da proteção fornecida pelo serviço {{site.data.keyword.amashort}}. A integração do {{site.data.keyword.amashort}} permite que qualquer aplicativo da web, independentemente da tecnologia que ele implementa, aproveite o protocolo OAuth2. Para obter informações sobre como configurar seu
{{site.data.keyword.amashort}} aplicativo da web para
acessar o serviço {{site.data.keyword.amashort}} usando
diferentes provedores de identidade, consulte:

    * [Ativando a
autenticação do Facebook para aplicativos da web](facebook-auth-web.html)

    * [Ativando a
autenticação do Google para aplicativos da web](google-auth-web.html)

    * [Ativando a
autenticação customizada para aplicativos da web](custom-auth-web.html)

4. **Opcional:** configure um provedor de identidade para seu aplicativo. É possível configurar um provedor de identidade por aplicativo. A configuração de um provedor de identidade permite que os usuários do seu app móvel efetuem login com suas contas existentes do Facebook ou Google+. Ou é possível definir como os usuários efetuam login criando uma autenticação customizada.
   * [Autenticando usuários com as credenciais do Facebook](facebook-auth-overview.html)
   * [Autenticando usuários com as credenciais do Google](google-auth-overview.html)
   * [Autenticando usuários com um provedor de identidade customizado](custom-auth.html)


# Links relacionados
{: #rellinks}

## Tutoriais e amostras
{: #samples}
* [Amostra android-helloauthentication](https://github.com/ibm-bluemix-mobile-services/bms-samples-android-helloauthentication){: new_window}
* [Amostra ios-helloauthentication (Swift SDK)](https://github.com/ibm-bluemix-mobile-services/bms-samples-swift-helloauthentication){: new_window}
* [Amostra ios-helloauthentication (Objective-C SDK)](https://github.com/ibm-bluemix-mobile-services/bms-samples-ios-helloauthentication){: new_window}

## SDK
{: #sdk}
* [Core SDK (Android)](https://github.com/ibm-bluemix-mobile-services/bms-clientsdk-android-core){: new_window}
* [Core SDK (Cordova plug-in)](https://github.com/ibm-bluemix-mobile-services/bms-clientsdk-cordova-plugin-core){: new_window}
* [Core SDK (iOS - Swift) ](https://github.com/ibm-bluemix-mobile-services/bms-clientsdk-swift-core){: new_window}
* [Core SDK (iOS - Objective-C - Deprecated) ](https://hub.jazz.net/git/bluemixmobilesdk/imf-ios-sdk/archive?revstr=master){: new_window}
* [Autenticação customizada - amostra simples](https://github.com/ibm-bluemix-mobile-services/bms-mca-custom-identity-provider-sample){: new_window}
* [Autenticação customizada - amostra avançada](https://github.com/ibm-bluemix-mobile-services/bms-mca-custom-identity-provider-with-user-management){: new_window}

## Referência de API
{: api}
* [Android](https://console.{DomainName}/docs/api/content/api/mobilefirst/android/core-api-doc/overview-summary.html){: new_window}
* [iOS (Objective-C SDK) - descontinuado](https://console.{DomainName}/docs/api/content/api/mobilefirst/ios/IMFCore_api-doc/html/index.html){: new_window}


## Links relacionados
{: #general}
* [Visão geral](overview.html){: new_window}
