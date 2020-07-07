text

## Install
`$ npm i --save Sova-Dialog-Language-Module`   

## Quick start
```
import ckModuleInit from 'Sova-Dialog-Language-Module'   
const dlModule = ckModuleInit(dlConfig)   
 ```
 
 # Description
 ## API methods
 Используемые методы:
* [chatInit](https://github.com/sovaai/chatKit-dl-module/blob/master/APImethods/chatInit.md "Read more");   
* [chatRequest](https://github.com/sovaai/chatKit-dl-module/blob/master/APImethods/chatRequest.md "Read more");   
* [setInfo](https://github.com/sovaai/chatKit-dl-module/blob/master/APImethods/setInfo.md "Read more");   
* [chatEvent](https://github.com/sovaai/chatKit-dl-module/blob/master/APImethods/chatEvent.md "Read more");   
* [chatRate](https://github.com/sovaai/chatKit-dl-module/blob/master/APImethods/chatRate.md "Read more");   
* [chatTimerAnnouncementsRequest](https://github.com/sovaai/chatKit-dl-module/blob/master/APImethods/chatTimerAnnouncementsRequest%09.md "Read more");   
* [chatUpdate](https://github.com/sovaai/chatKit-dl-module/blob/master/APImethods/chatUpdate.md "Read more");   
* [notificationDisplay](https://github.com/sovaai/chatKit-dl-module/blob/master/APImethods/notificationDisplay.md "Read more");   
* [notificationRequest](https://github.com/sovaai/chatKit-dl-module/blob/master/APImethods/notificationRequest.md "Read more");   
* [liveChatOperatorsCheckRequest](https://github.com/sovaai/chatKit-dl-module/blob/master/APImethods/liveChatOperatorsCheckRequest.md "Read more");   
* [geoLocationRequest](https://github.com/sovaai/chatKit-dl-module/blob/master/APImethods/geoLocationRequest.md "Read more");   
* [chatTrack](https://github.com/sovaai/chatKit-dl-module/blob/master/APImethods/chatTrack.md "Read more");   
* [reset](https://github.com/sovaai/chatKit-dl-module/blob/master/APImethods/reset.md "Read more").   
 
 ##
The function that calls the methods of the DL module.   
For example:   
```
import moduleInit from 'SOVA-dlModule'   
const dlModule = moduleInit(dlConfig)   
dlModule.moduleDispatcher('chatInit', { clientConfig: { siteLang: 'ru' } })
```
 
 ## dlConfig
 ```
 const dlConfig = {
  info: {
    uuid: string,
  },
  api?: {
    infApiUrl?: string,
    geoLocationApiUrl?: string,
    liveChatOperatorsApiUrl?: string,
    notificationsApiUrl?: string,
    chatTimerAnnouncementsApiUrl?: string,
    chatUpdateApiUrl?: string,
  },
  moduleEvents?: {
  chatInit: (module: DialogLanguageModule, data: ChatInitData) => void,
  chatRequest: (module: DialogLanguageModule, data: ChatRequestData) => void,
  chatEvent: (module: DialogLanguageModule, data: ChatEventData) => void,
  setInfo: (module: DialogLanguageModule, data: SetInfoData) => void,
  chatRate: (module: DialogLanguageModule, data: ChatRateData) => void,
  chatTrack: (module: DialogLanguageModule, data: ChatTrackData) => void,
  geoLocationRequest: (module: DialogLanguageModule) => void,
  liveChatOperatorsCheckRequest: (module: DialogLanguageModule) => void,
  notificationRequest: (module: DialogLanguageModule) => void,
  notificationDisplay: (module: DialogLanguageModule, data: NotificationDisplayData) => void,
  chatUpdate: (module: DialogLanguageModule) => void,
  chatTimerAnnouncementsRequest: (module: DialogLanguageModule, data: ChatTimerAnnouncementsRequestData) => void,
  reset: (module: DialogLanguageModule, data: ChatInitData) => void,
  },
  uiEvents?: {
    sendMessage?: (data: SendMessageData) => void,
    uiManagment?: (uiManagmentEvent: UIManagmentEvents, data: UIManagmentData) => void,
    notifications?: (notificationsEvent: NotificationsEvents, data: NotificationsData) => void,
    modules?: (modulesEvent: ModulesEvents , data: ModulesData)=> void,
  }
}
```
