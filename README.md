# yii2-unifonic-sms-integration
Yii2 component to integrate unifonic sms gateway. 
This SDK is to enable the PHP developer to integrate his/her php project with our APIs to take advantages of all features we offer like send SMS , voice call and get reports

How to use the SDK :

Configuration:

A- Edit the config file as below :
```
return array(

'AppSid' => [Your Rest AppSid],

'ApiURL' => 'http://api.unifonic.com/rest/',);
B- Add These Lines to your PHP file:
```
```
<?php



use \common\components\Unifonic\API\Client;

$client = new Client();

?>
```
Text Massages: Examples :
```
$response = $client->Messages->Send(966505050505,'Hello','UNIFONIC'); // send regular massage

$response = $client->Messages  >SendBulkMessages('966505050505,966555655555','Hello','UNIFONIC');  // send bulk massages
Handling Exceptions :
```

For errors and http status you may refer to the following link : http://docs.unifonic.apiary.io/
