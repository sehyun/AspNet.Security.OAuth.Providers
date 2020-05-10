# AspNet.Security.OAuth.Providers

**AspNet.Security.OAuth.Providers** is a **collection of security middleware** that you can use in your **ASP.NET Core** application to support social authentication providers like **[GitHub](https://github.com/)**, **[Foursquare](https://foursquare.com/)** or **[Dropbox](https://www.dropbox.com/)**. It is directly inspired by **[Jerrie Pelser](https://github.com/jerriep)**'s initiative, **[Owin.Security.Providers](https://github.com/RockstarLabs/OwinOAuthProviders)**.

**The latest official release can be found on [NuGet](https://www.nuget.org/profiles/aspnet-contrib) and the nightly builds on [MyGet](https://www.myget.org/gallery/aspnet-contrib)**.

[![Build status](https://github.com/aspnet-contrib/AspNet.Security.OAuth.Providers/workflows/build/badge.svg?branch=rel/2.2.x&event=push)](https://github.com/aspnet-contrib/AspNet.Security.OAuth.Providers/actions?query=workflow%3Abuild+branch%3A2.2.x+event%3Apush)

## Getting started

**Adding social authentication to your application is a breeze** and just requires a few lines in your `Startup` class:

```csharp
public void ConfigureServices(IServiceCollection services)
{
    services.AddAuthentication(options => { /* Authentication options */ })
            .AddGitHub(options =>
            {
                options.ClientId = "49e302895d8b09ea5656";
                options.ClientSecret = "98f1bf028608901e9df91d64ee61536fe562064b";
            });
}

public void Configure(IApplicationBuilder app)
{
    app.UseAuthentication();
}
```

See the [/samples](https://github.com/aspnet-contrib/AspNet.Security.OAuth.Providers/tree/dev/samples) directory for a complete sample **using ASP.NET Core MVC and supporting multiple social providers**.

## Contributing

**AspNet.Security.OAuth.Providers** is actively maintained by:

  * **[Kévin Chalet](https://github.com/PinpointTownes)** ([@PinpointTownes](https://twitter.com/PinpointTownes)).
  * **[Martin Costello](https://github.com/martincostello)** ([@martin_costello](https://twitter.com/martin_costello)).
  * **[Patrick Westerhoff](https://github.com/poke)** ([@poke](https://twitter.com/poke)).

We would love it if you could help contributing to this repository.

**Special thanks to our contributors:**

* [Abhinav Nigam](https://github.com/abhinavnigam)
* [Adam Reisinger](https://github.com/Res42)
* [Albert Zakiev](https://github.com/serber)
* [Albireo](https://github.com/kappa7194)
* [Anders Blankholm](https://github.com/ablankholm)
* [Andrew Lock](https://github.com/andrewlock)
* [Andrew Mattie](https://github.com/amattie)
* [Andrii Chebukin](https://github.com/xperiandri)
* [Chino Chang](https://github.com/kinosang)
* [Dave Timmins](https://github.com/davetimmins)
* [Dmitry Popov](https://github.com/justdmitry)
* [Eric Green](https://github.com/ericgreenmix)
* [Ethan Celletti](https://github.com/Gekctek)
* [Galo](https://github.com/asiffermann)
* [Igor Simovic](https://github.com/igorsimovic)
* [James Holcomb](https://github.com/jamesholcomb)
* [Jason Loeffler](https://github.com/jmloeffler)
* [Jerrie Pelser](https://github.com/jerriep)
* [Jesse Mandel](https://github.com/supergibbs)
* [Jordan Knight](https://github.com/jakkaj)
* [Kévin Chalet](https://github.com/PinpointTownes)
* [Konstantin Mamaev](https://github.com/MrMeison)
* [Mariusz Zieliński](https://github.com/mariozski)
* [Martin Costello](https://github.com/martincostello)
* [Maxime Roussin-Bélanger](https://github.com/Lorac)
* [Michael Knowles](https://github.com/mjknowles)
* [Patrick Westerhoff](https://github.com/poke)
* [Robert Shade](https://github.com/robert-shade)
* [saber-wang](https://github.com/saber-wang)
* [Sinan](https://github.com/SH2015)
* [Stefan](https://github.com/Schlurcher)
* [Steffen Wenz](https://github.com/swenz)
* [Tathagata Chakraborty](https://github.com/tatx)
* [TheUltimateC0der](https://github.com/TheUltimateC0der)
* [Tommy Parnell](https://github.com/tparnell8)
* [twsl](https://github.com/twsI)
* [Yannic Smeets](https://github.com/yannicsmeets)
* [zAfLu](https://github.com/zAfLu)
* [zhengchun](https://github.com/zhengchun)
* [Volodymyr Baydalka](https://github.com/zVolodymyr)

## Support

**Need help or wanna share your thoughts?** Don't hesitate to join us on Gitter or ask your question on StackOverflow:

- **Gitter: [https://gitter.im/aspnet-contrib/AspNet.Security.OAuth.Providers](https://gitter.im/aspnet-contrib/AspNet.Security.OAuth.Providers)**
- **StackOverflow: [https://stackoverflow.com/questions/tagged/aspnet-contrib](https://stackoverflow.com/questions/tagged/aspnet-contrib)**

## License

This project is licensed under the **Apache License**. This means that you can use, modify and distribute it freely. See [https://www.apache.org/licenses/LICENSE-2.0.html](https://www.apache.org/licenses/LICENSE-2.0.html) for more details.

## Providers

Links to the latest stable and nightly NuGet packages for each provider, as well as a link to their integration documentation are listed in the table below.

If a provider you're looking for does not exist, consider making a PR to add one.

| Provider | Stable | Nightly | Documentation |
|:-:|:-:|:-:|:-:|
| Amazon | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Amazon?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Amazon/ "Download AspNet.Security.OAuth.Amazon from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Amazon?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Amazon "Download AspNet.Security.OAuth.Amazon from MyGet.org") | [Documentation](https://developer.amazon.com/docs/login-with-amazon/documentation-overview.html "Amazon developer documentation") |
| Apple | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Apple?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Apple/ "Download AspNet.Security.OAuth.Apple from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Apple?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Apple "Download AspNet.Security.OAuth.Apple from MyGet.org") | [Documentation](https://developer.apple.com/documentation/signinwithapplerestapi "Apple developer documentation") |
| ArcGIS | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.ArcGIS?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.ArcGIS/ "Download AspNet.Security.OAuth.ArcGIS from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.ArcGIS?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.ArcGIS "Download AspNet.Security.OAuth.ArcGIS from MyGet.org") | [Documentation](https://developers.arcgis.com/documentation/core-concepts/security-and-authentication/what-is-oauth-2/ "ArcGIS developer documentation") |
| Asana | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Asana?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Asana/ "Download AspNet.Security.OAuth.Asana from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Asana?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Asana "Download AspNet.Security.OAuth.Asana from MyGet.org") | [Documentation](https://asana.com/developers/documentation/getting-started/auth "Asana developer documentation") |
| Autodesk | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Autodesk?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Autodesk/ "Download AspNet.Security.OAuth.Autodesk from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Autodesk?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Autodesk "Download AspNet.Security.OAuth.Autodesk from MyGet.org") | [Documentation](https://forge.autodesk.com/en/docs/oauth/v2/developers_guide/overview/ "Autodesk developer documentation") |
| Automatic | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Automatic?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Automatic/ "Download AspNet.Security.OAuth.Automatic from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Automatic?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Automatic "Download AspNet.Security.OAuth.Automatic from MyGet.org") | [Documentation](https://developer.automatic.com/documentation/ "Automatic developer documentation") |
| Baidu | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Baidu?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Baidu/ "Download AspNet.Security.OAuth.Baidu from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Baidu?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Baidu "Download AspNet.Security.OAuth.Baidu from MyGet.org") | [Documentation](https://developer.baidu.com/ "Baidu developer documentation") |
| BattleNet | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.BattleNet?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.BattleNet/ "Download AspNet.Security.OAuth.BattleNet from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.BattleNet?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.BattleNet "Download AspNet.Security.OAuth.BattleNet from MyGet.org") | [Documentation](https://develop.battle.net/documentation/guides/using-oauth "BattleNet developer documentation") |
| Beam (Mixer) | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Beam?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Beam/ "Download AspNet.Security.OAuth.Beam from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Beam?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Beam "Download AspNet.Security.OAuth.Beam from MyGet.org") | [Documentation](https://dev.mixer.com/reference/oauth "Mixer developer documentation") |
| Bitbucket | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Bitbucket?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Bitbucket/ "Download AspNet.Security.OAuth.Bitbucket from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Bitbucket?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Bitbucket "Download AspNet.Security.OAuth.Bitbucket from MyGet.org") | [Documentation](https://developer.atlassian.com/bitbucket/api/2/reference/meta/authentication "Bitbucket developer documentation") |
| Buffer | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Buffer?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Buffer/ "Download AspNet.Security.OAuth.Buffer from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Buffer?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Buffer "Download AspNet.Security.OAuth.Buffer from MyGet.org") | [Documentation](https://buffer.com/developers/api/oauth "Buffer developer documentation") |
| CiscoSpark (Webex Teams) | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.CiscoSpark?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.CiscoSpark/ "Download AspNet.Security.OAuth.CiscoSpark from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.CiscoSpark?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.CiscoSpark "Download AspNet.Security.OAuth.CiscoSpark from MyGet.org") | [Documentation](https://developer.webex.com/docs/api/getting-started/accounts-and-authentication "Webex Teams developer documentation") |
| DeviantArt | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.DeviantArt?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.DeviantArt/ "Download AspNet.Security.OAuth.DeviantArt from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.DeviantArt?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.DeviantArt "Download AspNet.Security.OAuth.DeviantArt from MyGet.org") | [Documentation](https://www.deviantart.com/developers/ "DeviantArt developer documentation") |
| Discord | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Discord?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Discord/ "Download AspNet.Security.OAuth.Discord from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Discord?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Discord "Download AspNet.Security.OAuth.Discord from MyGet.org") | [Documentation](https://discordapp.com/developers/docs/topics/oauth2 "Discord developer documentation") |
| Dropbox | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Dropbox?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Dropbox/ "Download AspNet.Security.OAuth.Dropbox from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Dropbox?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Dropbox "Download AspNet.Security.OAuth.Dropbox from MyGet.org") | [Documentation](https://www.dropbox.com/developers/reference/oauth-guide?_tk=guides_lp&_ad=deepdive2&_camp=oauth "Dropbox developer documentation") |
| EVEOnline | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.EVEOnline?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.EVEOnline/ "Download AspNet.Security.OAuth.EVEOnline from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.EVEOnline?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.EVEOnline "Download AspNet.Security.OAuth.EVEOnline from MyGet.org") | [Documentation](https://github.com/esi/esi-docs/blob/master/docs/sso/web_based_sso_flow.md "EVEOnline developer documentation") |
| Fitbit | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Fitbit?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Fitbit/ "Download AspNet.Security.OAuth.Fitbit from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Fitbit?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Fitbit "Download AspNet.Security.OAuth.Fitbit from MyGet.org") | [Documentation](https://dev.fitbit.com/build/reference/web-api/oauth2/ "Fitbit developer documentation") |
| Foursquare | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Foursquare?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Foursquare/ "Download AspNet.Security.OAuth.Foursquare from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Foursquare?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Foursquare "Download AspNet.Security.OAuth.Foursquare from MyGet.org") | [Documentation](https://developer.foursquare.com/docs/api/configuration/authentication "Foursquare developer documentation") |
| GitHub | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.GitHub?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.GitHub/ "Download AspNet.Security.OAuth.GitHub from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.GitHub?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.GitHub "Download AspNet.Security.OAuth.GitHub from MyGet.org") | [Documentation](https://developer.github.com/apps/building-oauth-apps/ "GitHub developer documentation") |
| GitLab | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.GitLab?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.GitLab/ "Download AspNet.Security.OAuth.GitLab from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.GitLab?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.GitLab "Download AspNet.Security.OAuth.GitLab from MyGet.org") | [Documentation](https://docs.gitlab.com/ee/api/oauth2.html "GitLab developer documentation") |
| Gitter | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Gitter?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Gitter/ "Download AspNet.Security.OAuth.Gitter from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Gitter?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Gitter "Download AspNet.Security.OAuth.Gitter from MyGet.org") | [Documentation](https://developer.gitter.im/docs/authentication "Gitter developer documentation") |
| Harvest | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Harvest?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Harvest/ "Download AspNet.Security.OAuth.Harvest from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Harvest?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Harvest "Download AspNet.Security.OAuth.Harvest from MyGet.org") | [Documentation](https://help.getharvest.com/api-v1/authentication/authentication/oauth/ "Harvest developer documentation") |
| HealthGraph (Runkeeper) | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.HealthGraph?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.HealthGraph/ "Download AspNet.Security.OAuth.HealthGraph from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.HealthGraph?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.HealthGraph "Download AspNet.Security.OAuth.HealthGraph from MyGet.org") | N/A |
| Imgur | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Imgur?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Imgur/ "Download AspNet.Security.OAuth.Imgur from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Imgur?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Imgur "Download AspNet.Security.OAuth.Imgur from MyGet.org") | [Documentation](https://apidocs.imgur.com/?version=latest#authorization-and-oauth "Imgur developer documentation") |
| Instagram | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Instagram?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Instagram/ "Download AspNet.Security.OAuth.Instagram from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Instagram?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Instagram "Download AspNet.Security.OAuth.Instagram from MyGet.org") | [Documentation](https://www.instagram.com/developer/authentication/ "Instagram developer documentation") |
| LinkedIn | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.LinkedIn?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.LinkedIn/ "Download AspNet.Security.OAuth.LinkedIn from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.LinkedIn?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.LinkedIn "Download AspNet.Security.OAuth.LinkedIn from MyGet.org") | [Documentation](https://docs.microsoft.com/en-us/linkedin/shared/authentication/authentication "LinkedIn developer documentation") |
| MailChimp | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.MailChimp?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.MailChimp/ "Download AspNet.Security.OAuth.MailChimp from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.MailChimp?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.MailChimp "Download AspNet.Security.OAuth.MailChimp from MyGet.org") | [Documentation](https://developer.mailchimp.com/documentation/mailchimp/guides/how-to-use-oauth2/ "MailChimp developer documentation") |
| MailRu | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.MailRu?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.MailRu/ "Download AspNet.Security.OAuth.MailRu from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.MailRu?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.MailRu "Download AspNet.Security.OAuth.MailRu from MyGet.org") | [Documentation](https://o2.mail.ru/docs#web "MailRu developer documentation") |
| Myob | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Myob?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Myob/ "Download AspNet.Security.OAuth.Myob from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Myob?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Myob "Download AspNet.Security.OAuth.Myob from MyGet.org") | [Documentation](https://developer.myob.com/api/accountright/api-overview/authentication/ "Myob developer documentation") |
| Nextcloud | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Nextcloud?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Nextcloud/ "Download AspNet.Security.OAuth.Nextcloud from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Nextcloud?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Nextcloud "Download AspNet.Security.OAuth.Nextcloud from MyGet.org") | [Documentation](https://docs.nextcloud.com/server/14/admin_manual/configuration_server/oauth2.html "Nextcloud developer documentation")  [User EndPoint Documentation](https://docs.nextcloud.com/server/15/developer_manual/client_apis/OCS/index.html#user-metadata "Nextcloud developer documentation") |
| Odnoklassniki | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Odnoklassniki?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Odnoklassniki/ "Download AspNet.Security.OAuth.Odnoklassniki from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Odnoklassniki?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Odnoklassniki "Download AspNet.Security.OAuth.Odnoklassniki from MyGet.org") | [Documentation](https://apiok.ru/ext/oauth/server "Odnoklassniki developer documentation") |
| Onshape | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Onshape?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Onshape/ "Download AspNet.Security.OAuth.Onshape from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Onshape?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Onshape "Download AspNet.Security.OAuth.Onshape from MyGet.org") | N/A |
| Patreon | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Patreon?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Patreon/ "Download AspNet.Security.OAuth.Patreon from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Patreon?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Patreon "Download AspNet.Security.OAuth.Patreon from MyGet.org") | [Documentation](https://docs.patreon.com/#oauth "Patreon developer documentation") |
| Paypal | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Paypal?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Paypal/ "Download AspNet.Security.OAuth.Paypal from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Paypal?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Paypal "Download AspNet.Security.OAuth.Paypal from MyGet.org") | [Documentation](https://developer.paypal.com/docs/api-basics/#oauth-20-authorization-protocol "Paypal developer documentation") |
| QQ | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.QQ?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.QQ/ "Download AspNet.Security.OAuth.QQ from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.QQ?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.QQ "Download AspNet.Security.OAuth.QQ from MyGet.org") | [Documentation](https://developers.e.qq.com/docs/apilist/auth/oauth2 "QQ developer documentation") |
| Reddit | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Reddit?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Reddit/ "Download AspNet.Security.OAuth.Reddit from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Reddit?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Reddit "Download AspNet.Security.OAuth.Reddit from MyGet.org") | [Documentation](https://github.com/reddit-archive/reddit/wiki/oauth2 "Reddit developer documentation") |
| Salesforce | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Salesforce?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Salesforce/ "Download AspNet.Security.OAuth.Salesforce from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Salesforce?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Salesforce "Download AspNet.Security.OAuth.Salesforce from MyGet.org") | [Documentation](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/intro_understanding_web_server_oauth_flow.htm "Salesforce developer documentation") |
| Shopify | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Shopify?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Shopify/ "Download AspNet.Security.OAuth.Shopify from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Shopify?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Shopify "Download AspNet.Security.OAuth.Shopify from MyGet.org") | [Documentation](https://help.shopify.com/en/api/getting-started/authentication/oauth "Shopify developer documentation") |
| Slack | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Slack?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Slack/ "Download AspNet.Security.OAuth.Slack from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Slack?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Slack "Download AspNet.Security.OAuth.Slack from MyGet.org") | [Documentation](https://api.slack.com/docs/oauth "Slack developer documentation") |
| SoundCloud | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.SoundCloud?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.SoundCloud/ "Download AspNet.Security.OAuth.SoundCloud from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.SoundCloud?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.SoundCloud "Download AspNet.Security.OAuth.SoundCloud from MyGet.org") | [Documentation](https://developers.soundcloud.com/docs#authentication "SoundCloud developer documentation") |
| Spotify | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Spotify?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Spotify/ "Download AspNet.Security.OAuth.Spotify from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Spotify?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Spotify "Download AspNet.Security.OAuth.Spotify from MyGet.org") | [Documentation](https://developer.spotify.com/documentation/general/guides/authorization-guide/ "Spotify developer documentation") |
| Stack Exchange | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.StackExchange?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.StackExchange/ "Download AspNet.Security.OAuth.StackExchange from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.StackExchange?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.StackExchange "Download AspNet.Security.OAuth.StackExchange from MyGet.org") | [Documentation](https://api.stackexchange.com/docs/authentication "Stack Exchange developer documentation") |
| Strava | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Strava?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Strava/ "Download AspNet.Security.OAuth.Strava from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Strava?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Strava "Download AspNet.Security.OAuth.Strava from MyGet.org") | [Documentation](https://developers.strava.com/docs/authentication/ "Strava developer documentation") |
| Trakt | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Trakt?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Trakt/ "Download AspNet.Security.OAuth.Trakt from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Trakt?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Trakt "Download AspNet.Security.OAuth.Trakt from MyGet.org") | [Documentation](https://trakt.docs.apiary.io/ "Trakt developer documentation") |
| Twitch | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Twitch?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Twitch/ "Download AspNet.Security.OAuth.Twitch from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Twitch?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Twitch "Download AspNet.Security.OAuth.Twitch from MyGet.org") | [Documentation](https://dev.twitch.tv/docs/authentication/ "Twitch developer documentation") |
| Untappd | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Untappd?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Untappd/ "Download AspNet.Security.OAuth.Untappd from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Untappd?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Untappd "Download AspNet.Security.OAuth.Untappd from MyGet.org") | [Documentation](https://untappd.com/api/docs#authentication "Untappd developer documentation") |
| Vimeo | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Vimeo?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Vimeo/ "Download AspNet.Security.OAuth.Vimeo from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Vimeo?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Vimeo "Download AspNet.Security.OAuth.Vimeo from MyGet.org") | [Documentation](https://developer.vimeo.com/api/authentication "Vimeo developer documentation") |
| Visual Studio (Azure DevOps) | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.VisualStudio?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.VisualStudio/ "Download AspNet.Security.OAuth.VisualStudio from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.VisualStudio?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.VisualStudio "Download AspNet.Security.OAuth.VisualStudio from MyGet.org") | [Documentation](https://docs.microsoft.com/en-us/azure/devops/integrate/get-started/authentication/oauth?view=azure-devops "Azure DevOps developer documentation") |
| Vkontakte | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Vkontakte?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Vkontakte/ "Download AspNet.Security.OAuth.Vkontakte from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Vkontakte?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Vkontakte "Download AspNet.Security.OAuth.Vkontakte from MyGet.org") | [Documentation](https://vk.com/dev/authentication "Vkontakte developer documentation") |
| Weibo | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Weibo?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Weibo/ "Download AspNet.Security.OAuth.Weibo from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Weibo?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Weibo "Download AspNet.Security.OAuth.Weibo from MyGet.org") | [Documentation](https://open.weibo.com/wiki/Oauth/en "Weibo developer documentation") |
| Weixin (WeChat) | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Weixin?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Weixin/ "Download AspNet.Security.OAuth.Weixin from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Weixin?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Weixin "Download AspNet.Security.OAuth.Weixin from MyGet.org") | [Documentation](https://open.wechat.com/cgi-bin/newreadtemplate?t=overseas_open/docs/web/login/login "WeChat developer documentation") |
| WordPress | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.WordPress?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.WordPress/ "Download AspNet.Security.OAuth.WordPress from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.WordPress?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.WordPress "Download AspNet.Security.OAuth.WordPress from MyGet.org") | [Documentation](https://developer.wordpress.com/docs/oauth2/ "WordPress developer documentation") |
| Yahoo | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Yahoo?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Yahoo/ "Download AspNet.Security.OAuth.Yahoo from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Yahoo?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Yahoo "Download AspNet.Security.OAuth.Yahoo from MyGet.org") | [Documentation](https://developer.yahoo.com/oauth2/guide/ "Yahoo developer documentation") |
| Yammer | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Yammer?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Yammer/ "Download AspNet.Security.OAuth.Yammer from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Yammer?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Yammer "Download AspNet.Security.OAuth.Yammer from MyGet.org") | [Documentation](https://developer.yammer.com/docs/oauth-2 "Yammer developer documentation") |
| Yandex | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Yandex?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Yandex/ "Download AspNet.Security.OAuth.Yandex from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Yandex?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Yandex "Download AspNet.Security.OAuth.Yandex from MyGet.org") | [Documentation](https://tech.yandex.com/oauth/ "Yandex developer documentation") |
| Zalo | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.Zalo?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.Zalo/ "Download AspNet.Security.OAuth.Zalo from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.Zalo?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.Zalo "Download AspNet.Security.OAuth.Zalo from MyGet.org") | [Documentation](https://developers.zalo.me/docs/api/social-api-4 "Zalo developer documentation") |

<!--
| CHANGEME | [![NuGet](https://buildstats.info/nuget/AspNet.Security.OAuth.CHANGEME?includePreReleases=false)](https://www.nuget.org/packages/AspNet.Security.OAuth.CHANGEME/ "Download AspNet.Security.OAuth.CHANGEME from NuGet.org") | [![MyGet](https://buildstats.info/myget/aspnet-contrib/AspNet.Security.OAuth.CHANGEME?includePreReleases=false)](https://www.myget.org/feed/aspnet-contrib/package/nuget/AspNet.Security.OAuth.CHANGEME "Download AspNet.Security.OAuth.CHANGEME from MyGet.org") | [Documentation](CHANGEME "CHANGEME developer documentation") |
-->
