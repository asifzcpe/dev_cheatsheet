# H1 Cordova Plugin Camera build issue and image upload
## H2 Cordova Plugin Camera and Phonegap push plugin (v 1.11.1) conflict with each other. So you have to update the push plugin version to build successfully in phonegap
## H2 To Upload image by camera plugin, you have to set "destinationType: Camera.DestinationType.DATA_URL" . This option returns base64 image so that it can easy to uplaod on server
