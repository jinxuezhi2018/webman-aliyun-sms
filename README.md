##使用
use xuezhitech\aliyunsms\SendSms;
use OSS\OssClient;
use OSS\Core\OssException;

//短信配置
$this->sms_config = [
'accessKeyId' => Env::get('sms.access_key_id'),
'accessKeySecret' => Env::get('sms.access_key_secret'),
'SignName' => Env::get('sms.sign_name'),
'TemplateCode' => Env::get('sms.template_code')
];
$this->sms = new SendSms($this->sms_config);

//data为数组，不传默认为短信验证码
$res = $this->sms->sendSms($phone,$data);



